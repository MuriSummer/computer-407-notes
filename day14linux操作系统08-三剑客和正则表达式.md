# 三剑客和正则表达式

来源 PDF：三剑客和正则表达式.pdf（原文件位于课程目录，本文件夹不包含 PDF）

<a id="page-1"></a>

> 第 1 页

三剑客和正则表达式(守夜人 Jaden（吴老板）)

三剑客就是三个强大的命令。后期讲应急溯源的时候会用到。grep用的最多，所以我们重点讲解这个指令。三剑客配合正则表达式可以发挥重要作用。

## grep

#擅长过滤，或者说查找，按行来过滤

例子：/var/log/secure是记录用户登录系统的行为的，登录成功还是失败，系统都会自动记录这次登录动

作。

[root@localhost ~]# grep 'Failed password' /var/log/secure

Mar 25 18:20:48 localhost sshd[16905]: Failed password for root from

192.168.61.1 port 55577 ssh2

...

\# 如果我们想将所有登录失败的ip地址找出来，可以再次过滤

\# 比如查看某个ip地址登录了多少次

[root@localhost ~]# grep 'Failed password' /var/log/secure|grep

'192.168.61.1'|wc -l

3

\# 可以借助正则表达式来进行过滤，可以将内容过滤的很精确，有些在线的网站也可以帮我们生成一些常用的

正则表达式，比如https://www.hake.cc/tools/regexcode/

[root@localhost ~]# grep 'Failed password' /var/log/secure|grep --color -P "

(25[0-5]|2[0-4]\d|[0-1]\d{2}|[1-9]?\d)\.(25[0-5]|2[0-4]\d|[0-1]\d{2}|[1-9]?\d)\.

(25[0-5]|2[0-4]\d|[0-1]\d{2}|[1-9]?\d)\.(25[0-5]|2[0-4]\d|[0-1]\d{2}|[1-9]?\d)"

Mar 25 18:20:48 localhost sshd[16905]: Failed password for root from

192.168.61.1 port 55577 ssh2

\# ip地址都标红色了，表示匹配出来了。

\# 如果只要ip地址-Po

[root@localhost ~]# grep 'Failed password' /var/log/secure|grep --color -Po "

(25[0-5]|2[0-4]\d|[0-1]\d{2}|[1-9]?\d)\.(25[0-5]|2[0-4]\d|[0-1]\d{2}|[1-9]?\d)\.

(25[0-5]|2[0-4]\d|[0-1]\d{2}|[1-9]?\d)\.(25[0-5]|2[0-4]\d|[0-1]\d{2}|[1-9]?\d)"

192.168.61.1

\# 有些ip地址是重复的，因为尝试登录了很多次，那么可以先排序，再去重，来查看ip地址

[root@localhost ~]# grep 'Failed password' /var/log/secure|grep --color -Po "

(25[0-5]|2[0-4]\d|[0-1]\d{2}|[1-9]?\d)\.(25[0-5]|2[0-4]\d|[0-1]\d{2}|[1-9]?\d)\.

(25[0-5]|2[0-4]\d|[0-1]\d{2}|[1-9]?\d)\.(25[0-5]|2[0-4]\d|[0-1]\d{2}|[1-9]?

\d)"|sort -n |uniq -c

      2 192.168.2.113

      3 192.168.2.116

      1 192.168.61.1

\# 比如，如果看到了这么个ip地址164.90.232.121、164.90.232.241等尝试登录了你上千上万次，就是

在爆破攻击我们，百度一查，德国的

\# 我们可以直接拉黑这个ip地址，也叫做加黑，加入黑名单的意思，这个等后面我再教大家。

\# 为了演示下面的参数，我们先创建一个示例环境，也就是一个练习文件：

[root@localhost log]# cd /root/

[root@localhost ~]# head -50 /etc/services > test.txt

[root@localhost ~]# ls

<a id="page-2"></a>

> 第 2 页

2.txt  anaconda-ks.cfg  jaden  jaden17:52:30.txt  jaden.txt  test.txt  xx.txt

#grep参数

-n 显示行号

    [root@localhost ~]# grep -n 'tcp' test.txt

\    # vi test.txt +48，表示进入vi的时候，光标直接定位的48行起始位置。

-c 对结果行计数

    [root@localhost ~]# grep -c 'tcp' test.txt

    14

-i 不区分大小写

    [root@localhost ~]# grep -n 'tcp' test.txt -i

-v 反向搜索，取反

    [root@localhost ~]# grep -n 'udp' test.txt -v # 将不含有udp的行全部过滤出来

-w 精准匹配

    [root@localhost ~]# grep -w 'tcp' test.txt

-o 只显示匹配的结果，前面的第一个示例中我们用过-o参数

    [root@localhost ~]# grep -o -n 'tcp' test.txt

-A1 同时打印搜索结果行的后一行 ，A是after的简写

    [root@localhost ~]# grep -A2 'ftp' test.txt

    [root@localhost ~]# grep -A 2 'ftp' test.txt

-B3 同时打印搜索结果行的前三行，B是before的简写

    [root@localhost ~]# grep -B2 'ftp' test.txt

-C2 同时打印搜索结果行的上下各两行

    [root@localhost ~]# grep -C2 'ftp' test.txt

-E  扩展正则表达式

\    # 正则我们下面会细讲，先简单了解一下。

    [root@localhost ~]# grep -E '.tp' test.txt  # .就是正则表达式，表示任意的一个字符

    [root@localhost ~]# grep -E 'ftp|ssh' test.txt # 查找ftp或者ssh，|是或者的意思，

可以用多个ftp|ssh|telnet...

-P  使用perl正则

\    # perl语言中设计的正则表达式写法规则，很强大，很多领域都支持perl正则的语法结构。

    [root@localhost ~]# grep -P "\d+" test.txt # 匹配所有的数字

    [root@localhost ~]# grep -P "\d{4,}" test.txt  #匹配4位的数字

## sed

这个我们用的其实很少，所以大家简单学习一下即可。

#擅长取行和修改替换

用法：sed [-nri] [动作]  目标文件文件

选项与参数：

-n ：使用安静(silent)模式。在一般 sed 的用法中，所有来自 STDIN 的数据一般都会被列出到终端

上。但如果加上 -n 参数后，则只有经过sed 特殊处理的那一行(或者动作)才会被列出来。

-r ：sed 的动作支持的是延伸型正则表示法的语法。(默认是基础正则表示法语法)

-i ：直接修改读取的文件内容，而不是输出到终端。

动作说明： [n1[,n2]]function

n1, n2一般表示为行号，[,n2]表示这个参数可选，可有可无。

function：

a ：指定行后面插入一行

d ：删除

i ：指定行前面插入一行

p ：打印，#一般和前面的-n参数一起用

<a id="page-3"></a>

> 第 3 页

s ：替换 需要I忽略大小写，全局替换需要g

sed过滤

\    # sed也可以进行过滤，如下简单示例

    [root@localhost ~]# seq 5 > 1.txt

    [root@localhost ~]# vi 1.txt # 修改为如下内容

    [root@localhost ~]# cat 1.txt

    1

    2c

    3a

    4b

    5a

    [root@localhost ~]# sed '/a/p' 1.txt  #默认会将所有行都打印出来，并且匹配到的a所在的

行重新打印一遍

    1

    2c

    3a

    3a

    4b

    5a

    5a

    [root@localhost ~]# sed -n '/a/p' 1.txt   # 加上-n，进入安静(silent)模式，就不会

将所有内容打印出来了。

    3a

    5a

\    # sed过滤相比grep来说，就比较麻烦。所以，过滤我们一般用grep。

    [root@localhost ~]# sed -n '/tcp/p' test.txt  # 也能过滤出tcp所在的行

\# sed删除匹配的行数据

    [root@localhost ~]# sed  '/tcp/d' test.txt  # 删除所有带tcp的行，并不是删除原文件

中的数据，而是将删除之后的结果打印出来了。

\    # 所以只需要一个重定向，就拿到删除之后的结果了

    [root@localhost ~]# sed  '/tcp/d' test.txt > 2.txt

    [root@localhost ~]# cat -n 2.txt

\    # -i就可以直接删除原文件的数据

    [root@localhost ~]# sed -i '/tcp/d' test.txt

    [root@localhost ~]# cat -n test.txt

    [root@localhost ~]# sed -i '/udp/d' test.txt

    [root@localhost ~]# cat -n test.txt

    [root@localhost ~]# sed '/^#/d' test.txt # 删除以#开头的行，^表示以什么开头的正则表

达式，我没有加-i昂

\    # 指定行号来删除

    [root@localhost ~]# sed '1,10d' test.txt  # 删除1-10行的数据

    [root@localhost ~]# sed -i '1,10d' test.txt

\    # 只要1-5行的数据

    [root@localhost ~]# sed -n '1,5p' test.txt

\    # 只要第5行的数据

    [root@localhost ~]# sed -n '5p' test.txt

\# 插入数据

\    # 在第三行后面插入一行数据

    [root@localhost ~]# sed '3a hello jaden' 1.txt

    1

    2c

    3a

<a id="page-4"></a>

> 第 4 页

    hello jaden

    4b

    5a

\    # 在第2行前面插入一行数据

    [root@localhost ~]# sed '2i hello jaden' 1.txt

    1

    hello jaden

    2c

    3a

    4b

    5a

\    # 加上-i参数就能直接修改原文件

    [root@localhost ~]# sed -i '2i hello jaden' 1.txt

    [root@localhost ~]# cat 1.txt

    1

    hello jaden

    2c

    3a

    4b

    5a

\# 替换数据

\    # 把3a替换成wuLAOBAN

    [root@localhost ~]# sed 's#3a#wuLAOBAN#' 1.txt

    1

    hello jaden

    2c

    wuLAOBAN

    4b

    5a

    [root@localhost ~]# sed -i 's#3a#wuLAOBAN#' 1.txt

    [root@localhost ~]# cat 1.txt

    1

    hello jaden

    2c

    wuLAOBAN

    4b

    5a

\    # 把A替换成xxx，每行只替换一次，同一行的第二个及之后的A都不进行替换

    [root@localhost ~]# sed 's#A#xxx#' 1.txt

    1

    hello jaden

    2c

    wuLxxxOBAN

    4b

    5a

\    # 把所有的A都替换成xxx

    [root@localhost ~]# sed 's#A#xxx#g' 1.txt

    1

    hello jaden

    2c

    wuLxxxOBxxxN

    4b

    5a

\    # 把所有的A和a都替换成xxx，忽略大小写，参数I

<a id="page-5"></a>

> 第 5 页

    [root@localhost ~]# sed 's#A#xxx#gI' 1.txt

    1

    hello jxxxden

    2c

    wuLxxxOBxxxN

    4b

    5xxx

\# -r参数也是和正则搭配来用的，grep是-E和-P参数，我们讲完正则之后再说。

## awk

\# 擅长取列

用法，取列

比如3.txt内容如下：

2 this is a test

3 Do you like awk

This's a test

10 There are orange,apple,mongo

例子1： 取列

    [root@localhost ~]# vi 3.txt

    [root@localhost ~]# cat 3.txt

    2 this is a test

    3 Do you like awk

    This's a test

    10 There are orange,apple,mongo

    [root@localhost ~]# awk '{print $1}' 3.txt

    2

    3

    This's

    10

    [root@localhost ~]# awk '{print $3}' 3.txt  # 取第三列

    [root@localhost ~]# awk '{print $NF}' 3.txt  # 取每一行的最后一列，NF是固定写法

    test

    awk

    test

    orange,apple,mongo

    [root@localhost ~]# awk '{print $1,$NF}' 3.txt  # 取第一列和最后一列

    2 test

    3 awk

    This's test

    10 orange,apple,mongo

    [root@localhost ~]# awk '{print $NF,$1}' 3.txt  # 还可以反着写，所以通过awk，可以

将列顺序重新排版

    [root@localhost ~]# awk '{print $1,$4}' jaden.txt # 取出第一列和第四列

例子2：计算

    vi 4.txt，写上如下内容

\    # 水果，每斤多少钱，总共多少斤

    orange 10 20

    apple 20  30

<a id="page-6"></a>

> 第 6 页

    mongo 50  10

    banana 5  200

\    # 开始计算

    [root@localhost ~]# awk '{print $1,$2*$3}' 4.txt

    orange 200

    apple 600

    mongo 500

    banana 1000

\    # 还可以加备注信息：

    [root@localhost ~]# awk '{print $1"总价为：",$2*$3"元"}' 4.txt

    orange总价为： 200元

    apple总价为： 600元

    mongo总价为： 500元

    banana总价为： 1000元

\# 例子3：根据行号来筛选内容

\# a = 1表示变量赋值，让a=1

\# a == 1，表示判断一下a的值是不是等于1，等于1那么条件判断结果为真，不等1那么条件判断结果为假

\# 支持符号： > <  ==  >=   <=

[root@localhost ~]# awk 'NR==1' 4.txt  # 取出第一行数据，grep不会取出特定的行，只能筛选

某些行

orange 10 20

[root@localhost ~]# awk 'NR>2' 4.txt  # 取出行号大于2的行数据

mongo 50  10

banana 5  200

[root@localhost ~]# awk 'NR<=3' 4.txt  # 取出行号小于等于3的行数据

orange 10 20

apple 20  30

mongo 50  10

[root@localhost ~]# awk 'NR<=3 && NR>1' 4.txt  # 取出行号大于1并且小于等于3的行

apple 20  30

mongo 50  10

\# 还可以取行的同时来取列

[root@localhost ~]# awk 'NR<=3{print $1}' 4.txt

orange

apple

mongo

\# 例子4：

\# 还可以过滤出指定的行，awk也能做过滤，但是

[root@localhost ~]# awk '/apple/' 4.txt # 取出含有apple数据的行数据

apple 20  30

\# grep、sed、awk过滤对比

grep 'apple' 4.txt

sed -n '1,2p' 4.txt

awk 'NR>1 && NR<=3' 4.txt

\# 例子5：

\# 再比如我们刚才取ip地址：比直接写正则要方便很多

[root@localhost log]# grep 'Failed password' secure

<a id="page-7"></a>

> 第 7 页

Mar 25 18:20:48 localhost sshd[16905]: Failed password for root from

192.168.61.1 port 55577 ssh2

Mar 25 18:49:26 localhost sshd[1498]: Failed password for root from

192.168.2.113 port 49991 ssh2

...

[root@localhost log]# grep 'Failed password' secure|awk '{print $11}'

192.168.61.1

192.168.2.113

192.168.2.116

...

\# 例子6： 指定分隔符，默认是按照空格作为分隔符的

awk -F ":"  '{print $7,$1}' /etc/passwd  # 这个文件都是用:做的分隔符

[root@localhost ~]# awk -F ':' 'NR==3 || NR==5 {print $1}' /etc/passwd  # 取出第三

行和第五行的第一列数据，分隔符为:

daemon

lp

\# &&表示and，两个条件同时成立

\# ||表示or，满足一个条件即可

\# 例子7： 拼凑指定文本,双引号之间原样输出

\# awk -F ":"  '{print $1":123:"$7}' /etc/passwd

[root@localhost ~]# awk -F ":"  '{print $1":123:"$7}' /etc/passwd

root:123:/bin/bash

bin:123:/sbin/nologin

...

\# 例子8:  过滤文本

\# awk -F "[ /]+"   '$2~/^47/' 1.txt

\# 找出第一列数据中带h的，并取出第一列和第七列的数据

[root@localhost ~]# awk -F ':' '$1~/h/{print $1,$7}' /etc/passwd

shutdown /sbin/shutdown

halt /sbin/halt

sshd /sbin/nologin

chrony /sbin/nologin

apache /sbin/nologin

## 正则表达式

1.什么是正则表达式？

简单的说，正则表达式就是一套处理大量的字符串而定义的规则和方法。

例如：假设 @代表1234  北京邮电大学--by

通过正则表达式这些特殊符号，我们可以快速的过滤、替换需要的内容。

linux正则一般以行为单位处理的。

2.正则表达式

\# 准备示例：[root@localhost ~]# head -100 /etc/services > test.txt

\1)  ^  表示搜索以什么开头。

<a id="page-8"></a>

> 第 8 页

    [root@localhost ~]# grep '^#' test.txt  # 找出开头为#号的的行数据

    [root@localhost ~]# grep -v '^#' test.txt # 找出开头不是#号的行数据

\2)  $ 表示搜索以什么结尾。

    [root@localhost ~]# grep 'ol$' test.txt # 找出结尾为ol字母的行数据

\3)  ^$    表示空行，不是空格。

    [root@localhost ~]# grep '^$' test.txt # 找出所有的空白行。

    [root@localhost ~]# grep -v '^$' test.txt # 找出所有的非空白行数据，如果保存一下，

那么相当于快速删除所有空行。

\    # sed删除空行，更容易，因为它更擅长修改文件内容

    [root@localhost ~]# sed '/^$/d' test.txt # 加上-i就改了原文件

\4)  . 代表且只能代表任意一个字符。跟癞子斗地主中的癞子一样。

    [root@localhost ~]# grep '.dp' test.txt # 找出xdp，x可以是任意一个字符，注意，是一

个！

\5)  \      转义字符，让有着特殊身份意义的字符，脱掉马甲，还原原型。

          例如：\.只表示小数点，还原原始小数点的意义。

          [root@localhost ~]# grep '\.ia' test.txt # 这就表示，找到含有.dp的行数据

\6)  * 重复0个或多个前面的一个字符。不代表所有了。

\    # 准备一个测试数据：

    [root@localhost ~]# vi num.txt

    [root@localhost ~]# cat num.txt

    a 12222

    b 12222222

    c 1

    b 3

    d 122222222222222

    e 12

    a 4

\    # 看下面几个的效果就知道*的意思了。

    [root@localhost ~]# grep '2' num.txt

    [root@localhost ~]# grep '22' num.txt

    [root@localhost ~]# grep -o '22' num.txt  # -o就能看出来，它是两个字符两个字符的匹

配

    [root@localhost ~]# grep '12' num.txt

    [root@localhost ~]# grep '12*' num.txt

    [root@localhost ~]# grep '.*' num.txt   # 匹配所有字符

    [root@localhost ~]# grep '12.*' num.txt

\7)  .*  匹配所有的字符。^.* 任意多个字符开头。

    [root@localhost ~]# grep '12.*' num.txt

\# 小任务：

\# 1.复制一份/etc/services的前100行数据到serv文件中，然后将去掉serv文件中所有含有#的行和空行

    [root@localhost ~]# head -100 /etc/services > serv

\    # 用sed来玩：

    [root@localhost ~]# sed '/#/d' serv  # 去掉含有#号的行

    [root@localhost ~]# sed '/^$/d' serv # 去掉所有空行

\    # 用grep来玩：

    [root@localhost ~]# grep -Ev '^$|#' serv > ss.txt

    [root@localhost ~]# cat ss.txt

\# 2. 去掉aaa.txt文件中所有的空行和注释(注意：一行中可能只有部分是注释)

[root@localhost ~]# cat aaa.txt

hello -a  #a表示友好

<a id="page-9"></a>

> 第 9 页

hello -b  #b表示不友好

hello -c  #c表示骂人

\# 哈哈,这是个啥

\# what?

hello -d  #d表示非常爱你

[root@localhost ~]# grep '#.*' aaa.txt  # 这么写，可以将所有#号注释的内容全部匹配到，所

以这个正则表达式可以用

[root@localhost ~]# sed -i 's/#.*//g' aaa.txt  # 将#.*匹配到的内容全部替换为空。

[root@localhost ~]# sed -i '/^$/d' aaa.txt  # 再去除空行

[root@localhost ~]# cat aaa.txt  # 结果就ok了。

hello -a

hello -b

hello -c

hello -d

\8)  [abc]  匹配字符集合内任意一个字符[a-z]、[0-9]、[A-Z]，多选一，[0,9]这个是2选1.

    [root@localhost ~]# grep -E '[0-9]' serv

    [root@localhost ~]# grep -E '[0,9]' serv

\9)  [^abc] ^在中括号里面表示非，不包含a或b或c。

    [root@localhost ~]# grep -E '[^0-9]*' serv  # 不要数字

    [root@localhost ~]# grep -E '[^a-z]' serv  # 不要小写字母

    [root@localhost ~]# grep -E '[^a-z0-9A-Z]' serv  # 不要字母和数字

\10) {n,m} 重复n到m次，前一个字符。

    #匹配一下ip地址：0.0.0.0 -- 255.255.255.255，这是ip地址的范围，个数上就是7-15个

    [root@localhost ~]# grep -Eo '[0-9.]{7,15}' /var/log/secure # 但是如果有个大于7

位的数字，也会被匹配上8888888

    [root@localhost ~]# grep -Eo '[0-9.]{7,15}' /var/log/secure|grep '\.'

11） +    重复1次到多次，和*不同

    [root@localhost ~]# grep -E '19*' serv

    [root@localhost ~]# grep -E '19+' serv

12） ? 重复0次到多次，和*号很像。

    [root@localhost ~]# grep -Eo '[0-9]?' serv

13）\d 和[0-9]是一样的，但是它属于perl正则，grep使用perl正则的时候需要用-P参数来指定

    [root@localhost ~]# grep -E '\d' 22.txt

    [root@localhost ~]# grep -P '\d' 22.txt

取ip的例子：

\# 前面我们grep -Eo '[0-9.]{7,15}' /var/log/secure，找ip不是很准确，因为如果有个大于7位的

数字，也会被匹配上

ip addr|grep -Eo '[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}'

grep 'Failed password' secure |grep -Eo '[0-9]{1,3}\.[0-9.]+'

取root用户登录时间

lastlog|sed -n '/root/p'|grep -Eo '[0-9]{2}:[0-9]{2}:[0-9]{2}'

<a id="page-10"></a>

> 第 10 页

关于正则，我们简单学习这么多即可，不要深究昂，因为正则的东西太多了，后面遇到了复杂的我们在

分析。

perl正则：https://www.runoob.com/perl/perl-regular-expressions.html
