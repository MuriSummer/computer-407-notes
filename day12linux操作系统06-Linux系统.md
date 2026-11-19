# Linux系统

来源 PDF：Linux系统.pdf（原文件位于课程目录，本文件夹不包含 PDF）

<a id="page-1"></a>

> 第 1 页

Linux系统(守夜人 Jaden（吴老板）)

## 一、简单介绍

Unix，前面其实我们也介绍过，现在的操作系统的鼻祖，windows、mac、linux都是由它发展而来，

1969年诞生于贝尔实验室，作者主要有两个，其中一个大佬叫肯尼斯·蓝·汤普森，当初为了玩游戏发明了Unix操作系统，1970年正式发布，所以1970年称为操作系统元年，所有操作系统都以这个时间来计时，系统奔溃或者多年不用，断电很久，等我们再使用它的时候，时间都会从1970年1月1日0时0分0秒开始显示。

守夜人 Jaden（吴老板）

![第 1 页插图 1](assets/day12linux操作系统06-Linux系统/p001_img01.jpg)

ios、mac os等苹果的第一代操作系统于1984年发布。

windows 1.0 于1985年发布。

linux，于1991年发布，是林纳斯.托瓦兹在大学期间发开的了linux内核1.0/GPL，发展至今已经是能够与Windows抗衡了，很多企业服务器都在用，个人电脑也有在用的，比较少，而且国产系统好多都是基于Linux开发的，比如统信的UOS，如果未来国产的操作系统都普及了之后，微软的市场就没有了。

当时林纳斯.托瓦兹只是开发了linux内核，它可以兼容unix的各种系统软件，所以基于unix开发的各种系统软件，都是可以直接在linux上使用的。操作系统只有内核的话，用户是不能直接使用的，都需要各种系统软件才能正常使用。所以linux也叫做类unix，也就是unix-like。

<a id="page-2"></a>

> 第 2 页

![第 2 页插图 1](assets/day12linux操作系统06-Linux系统/p002_img01.jpg)

市面上的操作系统，基本都是基于unix\linux内核，研发了自己的很多系统软件，封装为了自己的操作

系统。

![第 2 页插图 2](assets/day12linux操作系统06-Linux系统/p002_img02.jpg)

GNU/Linux:

linux是指的内核，使用这种内核的操作系统，我们都叫做linux系统。

而基于linux内核打造出来的各类操作系统，我们称之为发行版操作系统，又分很多的体系，比如下面介绍的几个：

守夜人 Jaden（吴老板）

红帽系(redhat)

    它也有自己的几个分支：fedora、redhat、centos等，红帽体系的操作系统现在已经是一个非常大型成熟的系统了，也是现今linux分支中最牛的存在。它主要做企业级的操作系统，所以需要非常稳定的操作系统，所以redhat开始都是先发布fedora系统，这属于测试用的操作系统，免费给大家用，有什么问题就反馈回来，等bug解决的差不多了，很稳定了，就基于fedora推出稳定版本的操作系统，比如redhat和centos。但是这里面有个问题，redhat系列系统是收费的，而Linux是开源的，要遵循开源协议，比如GPL协议，所以红帽就发布了一个社区开源版本的系列叫做centos，centos其实就是去除了redhat收费的商业系统软件的免费系统，内核都没变，就是开源了。centos也很稳定，而且不要钱，现在中国互联网公司，多数使用的都是

centos系统，企业一般不敢直接使用fedora，这是测试版本，而redhat系列正版系统又是收费的。

现在最稳定企业服务器操作系统centos6.x、centos7.x、centos8.x等

debian系：虽然内核也是linux，但是打造的系统软件生态体系和redhat完全不同。

    它也有自己的几个分支：debian、ubuntu、kali、国产linux、内核 5.10 版本新 人工智能 自动驾驶 大数据

suse系列：opensuse  suse企业版

Android系列：

    小米：miui系统

<a id="page-3"></a>

> 第 3 页

    oppo：coloros系统

    华为：emui、HarmonyOS(鸿蒙操作系统)

    荣耀：MagicUI系统，后面带UI的其实就是提供了自己设计的图形化操作界面。

    ...

大家重点记住红帽系和debian系即可，不管是哪个系的，多数的操作命令都是一样的，只不过是一些操作界面、工具有些不同。所以只要会用一个linux系统，其他的基本也都会用了。再比如apk格式的软件，只要是android手机，都是可以安装使用的。

接下来我们来学习一下Linux操作系统的功能和操作，我们就用centos吧。

## 二、Centos系统的安装

### 1、Centos下载

centos官网在国外，所以下载起来肯定是很慢，国内有很多镜像地址，用国内的下载即可，比如清华大

学开源软件镜像站：https://mirrors.tuna.tsinghua.edu.cn/

守夜人 Jaden（吴老板）

![第 3 页插图 1](assets/day12linux操作系统06-Linux系统/p003_img01.jpg)

虽然最新的已经到8.x版本了，但是企业现在用的最多的还是7.x版本。我们使用7.8.2003即可：

centos的ios镜像下载地址：https://mirrors.tuna.tsinghua.edu.cn/centos-vault/7.8.2003/isos/x86_6

4/CentOS-7-x86_64-DVD-2003.iso

我已经给大家下载好了，如下

![第 3 页插图 2](assets/day12linux操作系统06-Linux系统/p003_img02.jpg)

<a id="page-4"></a>

> 第 4 页

### 2、Centos虚拟机的安装

我这里有之前安装的Centos7的虚拟机，我把它删除掉

![第 4 页插图 1](assets/day12linux操作系统06-Linux系统/p004_img01.jpg)

那么接下来我们安装Centos虚拟机：

首选创建一个存放虚拟机的文件夹：

守夜人 Jaden（吴老板）

![第 4 页插图 2](assets/day12linux操作系统06-Linux系统/p004_img02.jpg)

打开VMware，安装虚拟机：

<a id="page-5"></a>

> 第 5 页

![第 5 页页面图](assets/day12linux操作系统06-Linux系统/p005_full.jpg)

<a id="page-6"></a>

> 第 6 页

![第 6 页页面图](assets/day12linux操作系统06-Linux系统/p006_full.jpg)

<a id="page-7"></a>

> 第 7 页

![第 7 页页面图](assets/day12linux操作系统06-Linux系统/p007_full.jpg)

<a id="page-8"></a>

> 第 8 页

![第 8 页页面图](assets/day12linux操作系统06-Linux系统/p008_full.jpg)

<a id="page-9"></a>

> 第 9 页

![第 9 页页面图](assets/day12linux操作系统06-Linux系统/p009_full.jpg)

<a id="page-10"></a>

> 第 10 页

![第 10 页页面图](assets/day12linux操作系统06-Linux系统/p010_full.jpg)

<a id="page-11"></a>

> 第 11 页

![第 11 页页面图](assets/day12linux操作系统06-Linux系统/p011_full.jpg)

<a id="page-12"></a>

> 第 12 页

![第 12 页插图 1](assets/day12linux操作系统06-Linux系统/p012_img01.jpg)

### 3、系统初始化

字体变为白色表示选中了，选择第一个

守夜人 Jaden（吴老板）

![第 12 页插图 2](assets/day12linux操作系统06-Linux系统/p012_img02.jpg)

如下，选择中文

<a id="page-13"></a>

> 第 13 页

![第 13 页插图 1](assets/day12linux操作系统06-Linux系统/p013_img01.jpg)

如下，默认系统自动安装的软件很少，作为服务器来讲的话，软件需要安装的少一些，但是为了我们自己学习研究，我们还是安装的多一些，windows不会这样，直接就给你装一堆的系统软件，我们点击如下位置：

守夜人 Jaden（吴老板）

![第 13 页插图 2](assets/day12linux操作系统06-Linux系统/p013_img02.jpg)

如下，下面GNOME就是桌面的意思，我们学linux不用桌面，用了桌面学不到精髓，而且桌面本身也是个程序，会消耗系统资源和性能，所以企业服务器上基本都不会安装桌面。

<a id="page-14"></a>

> 第 14 页

![第 14 页插图 1](assets/day12linux操作系统06-Linux系统/p014_img01.jpg)

如下，我们设定分区，跟windows一样，Linux也是有分区的。

守夜人 Jaden（吴老板）

![第 14 页插图 2](assets/day12linux操作系统06-Linux系统/p014_img02.jpg)

如下，默认是自动分区的，但是默认分区分出来的效果不好，该大不大，该小不小的，我们还是手动分

区。

<a id="page-15"></a>

> 第 15 页

![第 15 页插图 1](assets/day12linux操作系统06-Linux系统/p015_img01.jpg)

如下

守夜人 Jaden（吴老板）

![第 15 页插图 2](assets/day12linux操作系统06-Linux系统/p015_img02.jpg)

如下，在linux下不和windows似的，有C盘、D盘..等盘符，它只有一个根盘符，就是/ ，剩下的目录都是再它之下的子目录。先将所有空间给/ 。

<a id="page-16"></a>

> 第 16 页

![第 16 页插图 1](assets/day12linux操作系统06-Linux系统/p016_img01.jpg)

如下

守夜人 Jaden（吴老板）

![第 16 页插图 2](assets/day12linux操作系统06-Linux系统/p016_img02.jpg)

可能会提出如下警告，说我们这么分不太合理，没事，先忽略，直接点击完成

<a id="page-17"></a>

> 第 17 页

![第 17 页插图 1](assets/day12linux操作系统06-Linux系统/p017_img01.jpg)

如下，点击接受

守夜人 Jaden（吴老板）

![第 17 页插图 2](assets/day12linux操作系统06-Linux系统/p017_img02.jpg)

如下，关闭Kdump功能，因为对我们现在学习来讲，没什么用，反而占用内存。

<a id="page-18"></a>

> 第 18 页

![第 18 页插图 1](assets/day12linux操作系统06-Linux系统/p018_img01.jpg)

关闭：

守夜人 Jaden（吴老板）

![第 18 页插图 2](assets/day12linux操作系统06-Linux系统/p018_img02.jpg)

接下来设置网络和主机名：

<a id="page-19"></a>

> 第 19 页

![第 19 页插图 1](assets/day12linux操作系统06-Linux系统/p019_img01.jpg)

如下，Linux的网卡默认是关闭的，想上网就需要我们手动打开，如下

守夜人 Jaden（吴老板）

![第 19 页插图 2](assets/day12linux操作系统06-Linux系统/p019_img02.jpg)

接下来就点击开始安装即可：

<a id="page-20"></a>

> 第 20 页

![第 20 页插图 1](assets/day12linux操作系统06-Linux系统/p020_img01.jpg)

如下，安装中，安装过程中设置个密码，Linux默认有一个root用户，类似于我们windows的

administrator用户，是超级管理员用户，我们上来就只有这么一个root用户，给它设置一个密码，不然一会进入系统的时候还是会让你先设置密码。

守夜人 Jaden（吴老板）

![第 20 页插图 2](assets/day12linux操作系统06-Linux系统/p020_img02.jpg)

如下，当你点击完成的时候，可能提示你密码太弱了，不管他，再点击完成即可

<a id="page-21"></a>

> 第 21 页

![第 21 页插图 1](assets/day12linux操作系统06-Linux系统/p021_img01.jpg)

如下，在这个界面等待即可，它在自行安装和配置。

守夜人 Jaden（吴老板）

![第 21 页插图 2](assets/day12linux操作系统06-Linux系统/p021_img02.jpg)

等待一会之后，就可以看到如下界面，点击重启

<a id="page-22"></a>

> 第 22 页

![第 22 页插图 1](assets/day12linux操作系统06-Linux系统/p022_img01.jpg)

等待一会后，看到如下界面，表示系统启动成功了，可以登录了。

![第 22 页插图 2](assets/day12linux操作系统06-Linux系统/p022_img02.jpg)

### 4、登录系统

先输入用户名：root，在输入密码：123456，输入密码的时候是不显示的。

我们先输入错误一次，看看提示信息：

守夜人 Jaden（吴老板）

![第 22 页插图 3](assets/day12linux操作系统06-Linux系统/p022_img03.jpg)

如下

![第 22 页插图 4](assets/day12linux操作系统06-Linux系统/p022_img04.jpg)

输入logout指令，按回车，表示退出登录

<a id="page-23"></a>

> 第 23 页

![第 23 页插图 1](assets/day12linux操作系统06-Linux系统/p023_img01.jpg)

就回到了登录界面

![第 23 页插图 2](assets/day12linux操作系统06-Linux系统/p023_img02.jpg)

那么这个系统是不能使用鼠标的，而且不能复制黏贴，所以我们操作这个系统，一般都是通过一些工具远程连接上这个系统来进行操作，并且工具提供了复制黏贴等各种操作功能。

## 三、远程连接工具连接控制系统

使用系统自带的ssh工具即可连接这个centos虚拟机，但是需要知道虚拟机的ip地址，那么接下来我们再学习一个linux操作指令，查看ip地址：

查看网络信息的指令：ip addr  # 中间有多少空格都没有关系

如下，我的ip地址为192.168.61.131

守夜人 Jaden（吴老板）

![第 23 页插图 3](assets/day12linux操作系统06-Linux系统/p023_img03.jpg)

### 1、ssh远程连接linux

1.1 windows的指令终端连接linux

使用我们的windows或者linux的物理机或者虚拟机都可以连接上它，指令如下

语法：ssh 用户名@ip地址

比如：ssh root@192.168.61.131

如下

<a id="page-24"></a>

> 第 24 页

![第 24 页插图 1](assets/day12linux操作系统06-Linux系统/p024_img01.jpg)

如下

![第 24 页插图 2](assets/day12linux操作系统06-Linux系统/p024_img02.jpg)

在上面这个界面，就可以进行复制黏贴了，复制某个指令，在这个窗口点击鼠标右键，就直接黏贴了。

这个有点类似于windows的远程桌面功能，也是远程控制主机的一种方式。

但是这种windows自带的ssh远程连接控制方式来控制Linux系统有些不方便，比如每次都要输入ssh那个连接指令，感觉就麻烦，所以远程控制Linux系统有一些专业的工具，比如xshell、iTerm2(mac电脑上用的)、secureCRT、Tabby、OpenSSH等等，windows上最好用的就是xshell这个工具了。

接下来我们学习一下xshell。

1.2 xshell下载安装

1.2.1 xshell下载

在官网下载即可，地址：https://www.xshell.com/zh/xshell/

守夜人 Jaden（吴老板）

![第 24 页插图 3](assets/day12linux操作系统06-Linux系统/p024_img03.jpg)

如下，需要得到一个免费授权：

<a id="page-25"></a>

> 第 25 页

![第 25 页插图 1](assets/day12linux操作系统06-Linux系统/p025_img01.jpg)

如下，大家输入一下邮箱，后面安装xshell的过程中需要输入这个邮箱：

守夜人 Jaden（吴老板）

![第 25 页插图 2](assets/day12linux操作系统06-Linux系统/p025_img02.jpg)

我也给大家下载好了，如下

![第 25 页插图 3](assets/day12linux操作系统06-Linux系统/p025_img03.jpg)

1.2.3 xshell安装

这个直接安装到我们的物理机上即可，我物理机上已经有了，我用虚拟机给大家安装一下：

<a id="page-26"></a>

> 第 26 页

![第 26 页页面图](assets/day12linux操作系统06-Linux系统/p026_full.jpg)

<a id="page-27"></a>

> 第 27 页

![第 27 页页面图](assets/day12linux操作系统06-Linux系统/p027_full.jpg)

<a id="page-28"></a>

> 第 28 页

![第 28 页页面图](assets/day12linux操作系统06-Linux系统/p028_full.jpg)

<a id="page-29"></a>

> 第 29 页

![第 29 页插图 1](assets/day12linux操作系统06-Linux系统/p029_img01.jpg)

看到这里，表示安装完成了。

注意，如果提示更新，不要更新

守夜人 Jaden（吴老板）

![第 29 页插图 2](assets/day12linux操作系统06-Linux系统/p029_img02.jpg)

1.3 xshell连接Linux

新建连接：

<a id="page-30"></a>

> 第 30 页

![第 30 页插图 1](assets/day12linux操作系统06-Linux系统/p030_img01.jpg)

如下

守夜人 Jaden（吴老板）

![第 30 页插图 2](assets/day12linux操作系统06-Linux系统/p030_img02.jpg)

然后点击用户身份验证：

<a id="page-31"></a>

> 第 31 页

![第 31 页插图 1](assets/day12linux操作系统06-Linux系统/p031_img01.jpg)

如下，输入用户名和密码，然后点击确定

守夜人 Jaden（吴老板）

![第 31 页插图 2](assets/day12linux操作系统06-Linux系统/p031_img02.jpg)

如下，看到一个名称，以后双击这个名称就可以连接了，注意你要连接的那个Linux系统必须开着机呢昂

<a id="page-32"></a>

> 第 32 页

![第 32 页插图 1](assets/day12linux操作系统06-Linux系统/p032_img01.jpg)

双击它，如下，如果双击一次之后提示没有连接成功，那么再次双击一下试试。

守夜人 Jaden（吴老板）

![第 32 页插图 2](assets/day12linux操作系统06-Linux系统/p032_img02.jpg)

如下

<a id="page-33"></a>

> 第 33 页

![第 33 页插图 1](assets/day12linux操作系统06-Linux系统/p033_img01.jpg)

退出登录，输入exit，如下

守夜人 Jaden（吴老板）

![第 33 页插图 2](assets/day12linux操作系统06-Linux系统/p033_img02.jpg)

双击连接名，又可以连接上：

![第 33 页插图 3](assets/day12linux操作系统06-Linux系统/p033_img03.jpg)

<a id="page-34"></a>

> 第 34 页

设置字体大小：

![第 34 页插图 1](assets/day12linux操作系统06-Linux系统/p034_img01.jpg)

这个工具就是以后我们主要使用的一个工具，它的功能先说到这里。

1.4 做快照

我们刚刚安装好的系统，最好做一个快照，万一哪天玩坏了，还可以还原回来。关机状态下做快照会更快一些。

关机指令，这个指令可以直接在xshell上输入，我这里就直接在虚拟机上输入了。

守夜人 Jaden（吴老板）

![第 34 页插图 2](assets/day12linux操作系统06-Linux系统/p034_img02.jpg)

如下

<a id="page-35"></a>

> 第 35 页

![第 35 页页面图](assets/day12linux操作系统06-Linux系统/p035_full.jpg)

<a id="page-36"></a>

> 第 36 页

![第 36 页插图 1](assets/day12linux操作系统06-Linux系统/p036_img01.jpg)

好，这样就ok了。

1.5 简单指令总结

下面这些指令，其实windows也有对应的指令，只不过写法不同。

#远程登录linux系统

守夜人 Jaden（吴老板）

ssh  root@192.168.202.136

#断开连接

exit

#重启系统

reboot 或者 shutdown -r now

#关机指令

shutdown #默认30秒之后才会关机

#立即关机

shutdown  -h  now

#十分钟之后关机

shutdown  -h  10

1.6 注意ip地址

虚拟机每次重启、或者换个地方、或者长时间打开，那么打开之后，ip地址可能会发生变化，别忘了连接时候改一下ip地址。

<a id="page-37"></a>

> 第 37 页

![第 37 页插图 1](assets/day12linux操作系统06-Linux系统/p037_img01.jpg)

## 四、文件和目录操作

守夜人 Jaden（吴老板）

Linux下的指令可以通过tab键进行自动补全。Ctrl+c可以打断指令执行，如果指令执行的很快并且不需要确认的，一般是打不断的。

### 1、基础指令

命令1：

#新建文件

touch

例子1： touch 1.txt  #创建单个文件

例子2： touch test{1..10}.txt #批量创建文件touch test{a..f}.txt

例子3： touch /root/4.txt  #在指定的/root目录下，创建文件4.txt

\# 如果touch的文件名称重复了，不会覆盖原文件

命令2：

<a id="page-38"></a>

> 第 38 页

#查看目录下的文件

ls全称list

ls：显示当前目录下的内容

例子1：ls  test09.txt   #查看test09.txt是否存在，有会显示文件名称，没有会报错例子2：ls  *.txt        #查看以txt结尾的所有文件，类似于windows下的*.后缀名搜索例子3：ls  -1         #以一行一个文件的方式显示，注意这是-1，是数字1，不是l昂例子4：ls  -a  al         #查看所有文件，包括隐藏文件，touch .文件名，.开头的就是隐藏文件例子5：ls -a -1         #查看所有文件，以一行一个来显示例子6：ls -l   #类似于windows的详细列表，这个-l不是数字1

以.开头的文件是隐藏文件，默认不显示

命令3：

#移动、也可以进行重命名

mv全称move

例子1：mv 222.txt 123.txt    #将222.txt文件重命名为123.txt

例子2：mv 123.txt /opt       #将当前目录下的123.txt移动到/opt目录下命令4：

#复制

cp全称copy，复制有个特点，就是如果复制到的文件夹中有同名的文件，会帮我们改名字并加上副本两个字，

linux不会帮我们改名字，我们需要自己指定名字，后缀名尽量不要改。

例子1：cp test01.txt /opt/   #将当前目录下的test01.txt复制到/opt目录下例子2：cp -a dev04 /opt/     #将目录dev04复制到/opt下，注意，要在dev04的上一级目录来复制它，在它内部是不能复制这个文件夹的命令5：

#删除，注意Linux和windows不同，没有回收站，删了就是删了

例子1:  rm /opt/123.txt  #将/opt目录下的123.txt文件删除，需要回复y确认删除例子2： rm -f /opt/test01.txt #将/opt目录下的test01.txt文件删除，不需要回复，强制删除，很守夜人 Jaden（吴老板）多指令都有自己的参数，而且有好多，-f就是强制的意思。

例子3： rm 文件1 文件2 文件3 #删除多个文件

#删除一个目录，linux的参数大部分没有先后顺序

#直接删除文件夹，比如 rm dev，这是不行的，会报错，需要带上r参数

[root@localhost ~]# rm -f -r dev02

[root@localhost ~]# rm -r -f dev03

[root@localhost ~]# rm -fr dev  # rm的两个参数可以合并到一起

[root@localhost ~]# rm -rf dev01

命令6：

<a id="page-39"></a>

> 第 39 页

#创建文件夹 创建目录directory，这里说的目录就是文件夹，默认显示是蓝色的字体，文件显示是白色的字

体

mkdir 全称make directory

例子1：mkdir dev   #创建一个dev目录

例子2：mkdir dev{01..10}     #批量创建多个目录

例子3：mkdir -p 1/2/3/4/5/6  #一次性创建多级子目录

重命名：mv jaden wulaoban # 将jaden目录改名为wulaoban

命令7：

#切换目录

cd  #全称change directory

例子1：

cd  local    #切换到local目录中

cd  /usr/local  #切换到目录/usr/local

cd  ..       #切换到上一级目录

cd ../..  # 进入上一级的上一级目录 ，还可以继续../

cd / # 直接切换到根目录

命令8：

#print work directory

pwd

#打印当前工作目录

命令9：

\# 历史指令查询

history

命令10：

守夜人 Jaden（吴老板）

目录分隔符：

windows：C:\Users\ls198\Desktop  # 微软故意用\，其他的unix分支系统都是/来分割

linux：/root/jaden/xx

linux只有一个盘符，不像windows，可以设置c盘、d盘...

/是根目录

/root 根目录下面的root目录

/root/jaden

/root/jaden/xx

命令11：

<a id="page-40"></a>

> 第 40 页

#修改文件内容，先体验一下，后面再专门讲vi的功能

#vi编辑器，和windows的记事本工具类似

例子1： vi  test03.txt   #编辑文件test03.txt

\# vi编辑保存文件，需要三种模式切换

常规模式：默认是常规模式，在常规模式中可以使用各种快捷键，帮我们快速编辑文件，比如dd，就是删除当前一行数据编辑模式：切换英文输入法，然后按ioa三个键中的任意一个键都可以进入编辑模式，这样才能向文件中写内容，写完内容之后，先回到常规模式，在编辑模式中按esc回到常规模式命令模式：在常规模式时按:(英文的冒号)进入命令模式，命令模式按esc回到常规模式，命令模式下输入q然后回车表示退出文件，wq保存并退出，q!表示强制退出不保存

vi三模式切换，图解

![第 40 页插图 1](assets/day12linux操作系统06-Linux系统/p040_img01.jpg)

命令12：

vi可以查看文件内容，但是每次都要vi进去，看完再退出来，比较麻烦，如果只是查看文件内容，如下指

令即可

守夜人 Jaden（吴老板）

#从上往下顺序查看文本内容

cat

例子1：cat  test03.txt  #查看test03.txt的全部内容

#从下往上倒着查看文本内容

tac

例子1：tac  test03.txt  #倒着查看test03.txt的全部内容

命令13：

#查看文件头几行

head

例子1： head  test03.txt       #查看文件的前十行，默认

例子2： head  -n 5 test03.txt  #查看文件的前5行

例子3： head  -5  test03.txt   #查看文件的前5行

命令14：

<a id="page-41"></a>

> 第 41 页

#查看文件倒数几行

tail

例子1： tail  test03.txt       #查看文件的倒数十行，默认

例子2： tail  -n 5 test03.txt  #查看文件的倒数5行

例子3： tail  -5  test03.txt   #查看文件的倒数5行

### 2、管道

管道符号：| ，可以将前面指令的执行结果，作为后面指令的操作内容。

比如我们通过管道来过滤出ip地址：

[root@localhost ~]# ip addr

1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group

default qlen 1000

    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00

    inet 127.0.0.1/8 scope host lo

       valid_lft forever preferred_lft forever

    inet6 ::1/128 scope host

       valid_lft forever preferred_lft forever

2: ens33: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc pfifo_fast state UP

group default qlen 1000

    link/ether 00:0c:29:83:e4:d9 brd ff:ff:ff:ff:ff:ff

    inet 10.0.0.128/24 brd 10.0.0.255 scope global noprefixroute dynamic ens33

       valid_lft 1253sec preferred_lft 1253sec

    inet6 fe80::ffe1:31ed:56dc:d9aa/64 scope link noprefixroute

       valid_lft forever preferred_lft forever

[root@localhost ~]# ip addr|tail -4

    inet 10.0.0.128/24 brd 10.0.0.255 scope global noprefixroute dynamic ens33

       valid_lft 1224sec preferred_lft 1224sec

    inet6 fe80::ffe1:31ed:56dc:d9aa/64 scope link noprefixroute

守夜人 Jaden（吴老板）

       valid_lft forever preferred_lft forever

[root@localhost ~]# ip addr|tail -4|head -1

    inet 10.0.0.128/24 brd 10.0.0.255 scope global noprefixroute dynamic ens33

[root@localhost ~]# ip addr|tail -4|head -1|cut -c 10-19  #cut -c 10-19表示从第10

个字符显示到第19个字符，这个指令可以忽略，大致了解一下即可，因为字符长度不固定，切的时候有可能切

不准确

10.0.0.128

### 3、文件内容过滤

命令15：

#统计，比如统计文件有多少个字节、多少行等等

wc  #全称Word Count，计数

wc -l按行统计，不会单独使用，需要接在管道后面

例子1：

[root@localhost ~]# cat jaden.txt |wc -l

18  # 共18行

<a id="page-42"></a>

> 第 42 页

[root@localhost ~]# cat -n jaden.txt # 显示内容的同时，显示行号

     1  sdsdsdsdsdsdsd是的是的

     2

     3  sdsd

     4  65656

     5  sdsd

     6  sdsd

     7  sdsd

     8  33333

     9  565656565

    10  33333

    11  565656565

    12  33333

    13  565656565

    14  33333

    15  565656565

    16

    17

    18  sdssds  ;;;;

wc -c jaden.txt # 统计文件中有多少个字节

\# 统计指令执行结果有多少行

例子：ip addr|wc -l

\# 统计bin目录下有多少个命令文件

例子：ls /bin|wc -l

命令16：

后期课程中，我会用它来生成一把密码本，来破解wifi密码。

#生成数字序列

seq # 全称：sequence，序列的意思

例子1：产生一个5到12的序列

[root@localhost ~]# seq 5 12

5

守夜人 Jaden（吴老板）

6

7

8

9

10

11

12

例子2：产生一个5到12等宽的序列

[root@localhost ~]# seq -w 5 110

05

06

07

08

09

10

11

12

<a id="page-43"></a>

> 第 43 页

后面这几个指令简单感受一下即可，后续课程中还会细讲

命令17:

#按行过滤字符串，默认是模糊匹配，只要单词中含有某些内容就过滤出单词所在的每行数据

grep

例子1： #普通过滤，将含有3这个字符的行过滤出来

[root@localhost ~]# grep '333' jaden.txt

33333

33334

33333

53333

例子2： #显示行号

[root@localhost ~]# grep -n '333' jaden.txt

8:33333

10:33333

12:33333

14:33333

grep精准匹配-w

示例：通过管道符和grep来过滤

![第 43 页插图 1](assets/day12linux操作系统06-Linux系统/p043_img01.jpg)

命令18:

#按列过滤

守夜人 Jaden（吴老板）

awk #awk其名称得自于它的创始人 Alfred Aho 、Peter Weinberger 和 Brian Kernighan 姓氏的

首个字母。

例子1： 取列,$1代表第一列，$2代表第二列，$NF代表最后一列，列是由空格分开的

[root@localhost ~]# cat jaden.txt

row 1, cell 1   row 1, cell 2

row 2, cell 1   row 2, cell 2

[root@localhost ~]# awk '{print $1}' jaden.txt  # 注意，必须是单引号

row

row

[root@localhost ~]# awk '{print $2}' jaden.txt

1,

2,

例子2：以逗号,做分隔符

[root@localhost ~]# cat jaden.txt

row 1, cell 1   row 1, cell 2

row 2, cell 1   row 2, cell 2

[root@localhost ~]# awk -F ','   '{print $1}' jaden.txt

row 1

row 2

[root@localhost ~]# awk -F ','   '{print $NF}' jaden.txt

 cell 2

<a id="page-44"></a>

> 第 44 页

 cell 2

命令19:

#排序

sort # 默认排序，先数字后字母

\# sort -n # 先字母(先小写字母后大写字母)后数字的排序方式，sort -n -r 反向排序

例子1：

[root@localhost ~]# cat test02.txt

3

2

6

4

8

7

5

3

2

1

2

3

4

5

6

9

1

5

7

[root@localhost ~]# cat test02.txt|sort -n

1

1

2

2

2

守夜人 Jaden（吴老板）

3

3

3

4

4

5

5

5

6

6

7

7

8

9

命令20：

#统计去重

uniq  #全称：unique，唯一、去重的意思，但是它是将连续的去重，不会间隔去重，所以最好先排序再去

重

<a id="page-45"></a>

> 第 45 页

例子1：

[root@localhost ~]# cat test02.txt|sort -n

1

1

2

2

2

3

3

3

4

4

5

5

5

6

6

7

7

8

9

[root@localhost ~]# cat test02.txt|sort -n|uniq

[root@localhost ~]# cat test02.txt|sort -n|uniq -c  # -c显示重复次数

      2 1

      3 2

      3 3

      2 4

      3 5

      2 6

      2 7

      1 8

      1 9

关于Linux的文件和目录操作的简单指令，大家先学习这么多。

守夜人 Jaden（吴老板）

## 五、目录结构

### 1、安装桌面版Centos

为了方便大家理解目录结构，我们安装一个桌面版的centos吧，其实工作中基本我是不安装桌面的，有些软件开发人员会用桌面版的。

这里就不最小化安装了，选择安装桌面，并且把所有的软件都安装上吧，方便使用。

### 2、目录结构介绍

<a id="page-46"></a>

> 第 46 页

路径分隔符：

    linux系统都是斜杠：也叫做正斜杠，/，linux下，每个目录后面其实默认都有个/，切换目录: cd

jaden或者cs jaden/ 是一样的

    windows系统是反斜杠：\

    G:\jadenwangan\

    /etc/abr

看图解，倒状的树型

![第 46 页插图 1](assets/day12linux操作系统06-Linux系统/p046_img01.jpg)

各个内置目录说明，目前先简单记忆一下即可，后面学习中都会详细说到，linux系统一切皆文件

/bin      #存放二进制的可执行文件，也就是命令，其实每个命令基本都是一个可执行代码文件，特别重

要，不能删除!

\    # window的命令文件都是exe结尾的，linux的命令文件是没有后缀名的，如果删除了某个命令文件，

那么这个命令就不能用了

/boot     #开机启动需要的文件， 特别重要，不要动里面的文件。

/dev      #dev全称：Devices，硬件设备控制文件，特别重要，千万不要动!

/etc      #存放系统的各种配置文件，相当于windows的注册表，也就是超大的配置文件，特别重要，不

能删除!

\    # 比如改密码什么的，其实都是修改的etc下面的某个配置文件(shadow文件)中的配置，还有安装的各

种软件配置文件，一般也是放到这个目录，也可以放到其他目录，但是一般都是放到这里。

守夜人 Jaden（吴老板）

/home     #所有普通用户的家目录就在这个home目录下，每个用户目录中都有自己的桌面等目录，

windows都是放到了Users目录下

/root     #root用户的专属家目录，特别重要，不能删除!

/lib      #library 32位库，一般是so结尾的库文件，特别重要，不能删除!

\    # so结尾的库文件，类似于windows下的系统的dll动态链接库文件。千万不要尝试删除，试试就逝

世。如果有快照的话你可以试试。

/lib64    #library 64位库，一般是so结尾的库文件，特别重要，不能删除!

/media    #多媒体文件目录(音乐、视频、文档等)，是一个不重要的目录，只是linux的作者希望用户能

够按照对应目录来存放内容，这个目录普通用户是没有权限删除的，root用户可以删除它

/mnt      #全称：mount，挂载的意思，一般是用来挂载光盘，U盘，也就是插入U盘、关盘等，打开之后

一般都是在这个mnt目录下，这个目录也是可以删除的

/opt      #部分软件安装存储目录，安装的某些软件的时候，如果默认安装，那么它可能会将自己的程序安

装到这个目录下，如果你不用这个目录，那么也是可以删除的目录

/proc     #全称：process，是进程的意思，每个进程编号一个目录。通过ps -ef指令可以查看到进程编

号， 特别重要，不能删除!

/sbin     #全称：super bin，是超级用户才能使用的命令 ，特别重要，不能删除!  shutdown

reboot

\    # 比如普通用户是没有关机(shutdown)、重启(reboot)等危害比较大的指令，这些命令文件在sbin

目录中

/srv      #之前用来存放软件源代码文件的，这个目录也没有实际用途。源代码-->编译-->打包-->软件包，软

件包在windows下叫做可执行文件，linux下叫做命令文件。其实叫啥都行，明白它是啥即可。

<a id="page-47"></a>

> 第 47 页

/sys      #全称：system，是系统功能目录，特别重要，不能删除!

/tmp      #全称：temporary，临时的意思，用来存放临时文件的目录，这里面的文件如果长时间没用的

话，会被系统自动清除。

\    # windows下也有很多这样的临时目录，多数都是隐藏目录，比如C:\Users\用户名

\AppData\Local\Temp，好多清理系统垃圾的软件，其实都是删除了一些临时文件。

/run      #运行，程序运行的时候产生的文件，多数也是临时文件，但是这里的文件不会被系统自动清除。

/usr      #用户级的目录，usr全称是UNIX software resource，主要存放的是一些软件程序以及这些

程序所需要使用的库，当然也会保存一些程序需要的资源文件，特别重要，不能删除! usr目录下面的文件夹种类和/根目录下很像，比如都有bin目录，linux作者这样的设计是想告诉用户，系统的命令文件放到根目录

的bin下，用户自己安装的某些软件的命令文件，放到/usr/bin下面。

/var      #全称是variable，用来存放一些经常变动的文件，比如日志文件、网页文件、缓存等，特别重

要，不能删除!

\    # 这个目录下我们安全人员一般只关注log日志目录。比如用户登录系统、什么时候登录的、登陆了几次

等等，都会在log目录下产生日志记录，这个我们后期会做演示.

### 3、相对路径和绝对路径

相对路径：从当前所在目录开始数的不完整的路径

绝对路径：从根开始的数的完整路径

这是两种路径形式，主要是为了方便用户操作的，到底哪个更方便，这个视实际情况而定。

示例：

创建目录：

    相对路径：

        mkdir jaden

        mkdir ../jaden

    绝对路径：

        mkdir /jaden

找寻目录：

    cd /usr/share/i18n/locales/

    当前位置：/usr/share/i18n/locales/

守夜人 Jaden（吴老板）

    目标位置：/etc/

    绝对路径：

        cd /etc/

    相对路径：

        cd ../../../../etc/

    这么看就绝对路径方便一些。

    但是如果下面的情况：

    当前位置：/usr/share/i18n/locales/

    目标位置：/usr/share/i18n/

    绝对路径：

        cd /usr/share/i18n/

    相对路径：

        cd ..

    或者如下情况

    当前位置：/usr/share/i18n/

    目标位置：/usr/share/i18n/locales/

    绝对路径：

        cd /usr/share/i18n/locales/

    相对路径：

        cd locales

<a id="page-48"></a>

> 第 48 页

    这么看就是相对路径方便一些。

    也就是说，如果目标在上一级或者下一级，离着比较近，相对路径操作就方便，如果目标目录没有和当前目录在一个路径分支上，离着比较远，那么用绝对路径方便一些。

## 六、用户和用户组管理

windows专业版，管理-->用户和用户组，来进行用户和用户组管理。

用户和用户组的关系，说到关系就三种情况：一对一、一对多、多对多。

![第 48 页插图 1](assets/day12linux操作系统06-Linux系统/p048_img01.jpg)

用户和用户组属于多对多的关系。

### 1、用户管理

命令21：

守夜人 Jaden（吴老板）

#创建用户

useradd

#创建一个用户

例子1：useradd  test1

命令22：

#设置密码，远程ssh连接是需要密码的，所以想让某个用户登录系统，必须设置密码

passwd

例子1：passwd  test1

#用root用户给普通用户修改密码

[root@localhost ~]# passwd test1

更改用户 test1 的密码 。

新的 密码：123456

无效的密码： 密码是一个回文

重新输入新的 密码：123456

passwd：所有的身份验证令牌已经成功更新。

#普通用户自己修改密码

<a id="page-49"></a>

> 第 49 页

[test1@localhost ~]$ passwd  # 给当前登录用户修改密码，root用户修改密码不需要输入旧密码，

普通用户需要输入旧密码

更改用户 test1 的密码 。

为 test1 更改 STRESS 密码。

（当前）UNIX 密码：

新的 密码：

无效的密码： 密码少于 8 个字符

新的 密码：

无效的密码： 密码少于 8 个字符

新的 密码：

无效的密码： 密码未通过字典检查 - 过于简单化/系统化

passwd: 已经超出服务重试的最多次数

\# 一般linux的密码是有复杂度要求的，比如下面这种密码就可以通过：大小写组合、数字、特殊字符组合起

来超过8位。

jaden666@qq.COM

jaden666@WSX

例子3：

#免交互修改密码，这样不需要输入两次密码确认。echo是打印的意思，有结果输出给passwd命令来修改

test1用户的密码

echo 123456|passwd --stdin test1

\# 这种一般同时改多个Linux服务器系统的密码时比较方便。

命令23：

#检查用户是否存在

id

例子1:

#用户存在，系统的返回结果

[root@localhost ~]# id test1

uid=1000(test1) gid=1000(test1) 组=1000(test1)

#用户不存在，系统的返回结果

[root@localhost ~]# id test2

守夜人 Jaden（吴老板）

id: test2: no such user

命令24：

#删除用户

userdel

例子1：

#被删除的用户还在登录状态，是不能删除的

[root@localhost ~]# userdel test1

userdel: user test1 is currently used by process 2356

#被删除的用户，退出登录之后，可以正常删除

[root@localhost ~]# userdel test1

linux删除用户之后，/home/目录下对应的用户文件夹还在，如果还想加回来这个用户，那么会提示家目录存

在，不会从样板目录(skel)中复制任何文件了，通过ls -a /etc/skel，可以看到skel目录下的内容了。

还提示邮箱文件已经存在，ls /var/spool/mail下面

windows删除用户之后，c:\Users目录下的用户文件夹也还在

注意：删除之后的用户，再次创建出来，密码是需要重新设置的

[root@localhost ~]# userdel -r test1  # 删除用户，并删除用户相关目录

<a id="page-50"></a>

> 第 50 页

命令25：

#修改用户信息，修改属性

usermod # modify 它有很多选项(参数)，-L是锁定用户，通过命令 -h(或者--help，一个-后面一般跟

一个字母即可，两个-后面一般跟完整单词)，可以查看命令的各种选项的意思，比如usermod -h

#锁定用户(和windows的禁用用户一个意思)

例子1：

[root@localhost ~]# usermod -L test1  #被锁定的用户，下次就登录不上系统了。

[root@localhost ~]# usermod -U test1  #解锁用户

[root@localhost ~]# lchage -l test1 # 查看用户详细信息

帐号被锁。

至少: 0

至多: 99999

警告: 7

不活跃：    从不

最后一次改变： 2021年07月20日

密码过期：   从不

密码不活跃：  从不

帐号过期：   从不

#禁止用户登录(这个后面再说)

[root@localhost ~]# usermod -s /sbin/nologin test2

[root@localhost ~]# grep -w 'test2' /etc/passwd

test2:x:1001:1001::/home/test2:/sbin/nologin

命令26：

#查看用户详细信息

lchage

例子1：

[root@localhost ~]# lchage -l test1

帐号没被锁。

至少: 0

守夜人 Jaden（吴老板）

至多: 99999

警告: 7

不活跃：    从不

最后一次改变： 2021年07月20日

密码过期：   从不

密码不活跃：  从不

帐号过期：   从不

所有的用户信息存储在/etc/passwd文件中，每创建一个用户该文件就会多一行记录

root:x:0:0:root:/root:/bin/bash

\# 下面的用户都是系统自带用户，不用管它

bin:x:1:1:bin:/bin:/sbin/nologin

daemon:x:2:2:daemon:/sbin:/sbin/nologin

adm:x:3:4:adm:/var/adm:/sbin/nologin

lp:x:4:7:lp:/var/spool/lpd:/sbin/nologin

sync:x:5:0:sync:/sbin:/bin/sync

shutdown:x:6:0:shutdown:/sbin:/sbin/shutdown

halt:x:7:0:halt:/sbin:/sbin/halt

mail:x:8:12:mail:/var/spool/mail:/sbin/nologin

<a id="page-51"></a>

> 第 51 页

operator:x:11:0:operator:/root:/sbin/nologin

games:x:12:100:games:/usr/games:/sbin/nologin

ftp:x:14:50:FTP User:/var/ftp:/sbin/nologin

nobody:x:99:99:Nobody:/:/sbin/nologin

systemd-network:x:192:192:systemd Network Management:/:/sbin/nologin

dbus:x:81:81:System message bus:/:/sbin/nologin

polkitd:x:999:998:User for polkitd:/:/sbin/nologin

tss:x:59:59:Account used by the trousers package to sandbox the tcsd

daemon:/dev/null:/sbin/nologin

abrt:x:173:173::/etc/abrt:/sbin/nologin

sshd:x:74:74:Privilege-separated SSH:/var/empty/sshd:/sbin/nologin

postfix:x:89:89::/var/spool/postfix:/sbin/nologin

chrony:x:998:996::/var/lib/chrony:/sbin/nologin

\# 下面这个是我们自己创建的用户

test1:x:1000:1000::/home/test1:/bin/bash

#passwd文件解释

root:x:0:0:root:/root:/bin/bash

test1:x:1000:1000::/home/test1:/bin/bash

test2:x:1001:1001::/home/test2:/sbin/nologin

test3:x:1002:1000::/home/test3:/sbin/nologin

haha:x:1004:1004:putong user:/home/haha:/bin/bash

第一列：用户名

第二列：x

第三列：uid  # root用户的uid是0，我们自己创建的用户uid是1000及之后的数值。

第四列：gid

第五列：注释，一般为空

第六列：家目录的位置

第七列：使用shell的名称，默认使用/bin/bash

所有的用户密码信息存储/etc/shadow，设置了密码的长度比较长。密码是两层加密的，基本无法破

解。但是如果黑客权限比较高，它可以用知道密码的shadow文件来替换这个文件，或者修改这个文件守夜人 Jaden（吴老板）下某个用户的密码，只有root用户才有权力修改这个文件。

[root@localhost ~]# cat /etc/shadow

root:$6$QM3AHtFflOvGbCnt$2wTYZrnO8c66vycaxprE79G.I7hiy8EqXntG86FXxqlSawjtKoTjAnA

a9xFA3ad1QpFskJRPt0QeDPBnZZAdx0::0:99999:7:::

bin:*:18353:0:99999:7:::

daemon:*:18353:0:99999:7:::

adm:*:18353:0:99999:7:::

lp:*:18353:0:99999:7:::

sync:*:18353:0:99999:7:::

shutdown:*:18353:0:99999:7:::

halt:*:18353:0:99999:7:::

mail:*:18353:0:99999:7:::

operator:*:18353:0:99999:7:::

games:*:18353:0:99999:7:::

ftp:*:18353:0:99999:7:::

nobody:*:18353:0:99999:7:::

systemd-network:!!:18827::::::

dbus:!!:18827::::::

polkitd:!!:18827::::::

<a id="page-52"></a>

> 第 52 页

tss:!!:18827::::::

abrt:!!:18827::::::

sshd:!!:18827::::::

postfix:!!:18827::::::

chrony:!!:18827::::::

test1:$6$7PLnhlcr$4SCHINbWrameVSn6rxYgDOeUBwvYOHVbEOIudtNxWXIl5ULSt1Om8FvK6R3s9f

I0qNef1vq8NhVMNJwudmfkM1:18828:0:99999:7:::

命令27：

登录主机的两种方式：

本地登录：直接在主机上输入用户名和密码登录

远程登录：ssh远程登录

windows默认只能同时一个用户登录，登录另外一个用户，前一个用户就会自动下线。

linux支持多个用户在多个地方同时登录一个系统，每个用户都有一个终端来控制操作系统。终端的意思就是连接窗口。

\# 查看当前登录了几个用户，或者打开了几个终端

w

结果：下面表示2个终端登录了

 12:15:42 up 21 min,  2 users,  load average: 0.00, 0.01, 0.03

USER     TTY      FROM             LOGIN@   IDLE   JCPU   PCPU WHAT

root     tty1                      12:15    6.00s  0.00s  0.00s -bash

root     pts/0    192.168.61.1     11:55    6.00s  0.02s  0.01s w

\# tty1表示本地登录的、pts/0表示远程登录的

### 2、用户组管理

命令28：

守夜人 Jaden（吴老板）

新建组和查看组:

    groupadd 组名

例子：

    [root@localhost tmp]# groupadd test

    [root@localhost tmp]# cat /etc/group  # 查看有哪些组

命令29：

#指定组来创建用户，如果没有指定组，那么创建用户的时候，linux会自动创建一个与用户名同名的组。

例子： 组的英文是group

[root@localhost tmp]# useradd  -g test1  test3  #-g 是指定主组

[root@localhost tmp]# id test3

uid=1002(test3) gid=1000(test1) 组=1000(test1)

gid表示用户的属组的主组

组=表示用户的属组，用户可以属于多个组，一个主组，多个其他组。

命令30：

<a id="page-53"></a>

> 第 53 页

\# 删除组

groupdel 组名

例子：

[root@localhost tmp]# groupdel test #如果组内有用户，会报错，需要先删除主组属于这个组的所

有用户(userdel -r 用户名)，或者将用户移到其他的组之后在删除组。

\# 修改组名

groupmod -n jaden wulaoban # 将wulaoban组名改为jaden

命令31：

\# 修改用户所属的主组

usermod -g 组名

例子：

[root@localhost tmp]# usermod -g test jaden #将jaden用户的主组改为test

[root@localhost tmp]# groupdel jaden # 就可以将jaden组删除了。

\# 将用户添加到多个其他组中

usermod -G

[root@localhost tmp]# usermod -G test wulaoban # 将wulaoban用户也添加到test组

好，关于用户和用户组的操作，我们简单说这么多，后面课程中用到了哪些，我们再细说。

## 七、权限管理

### 1、权限介绍和示例

root用户权限最高，所以一般对他不做什么权限设置。其他用户就要设定权限并且遵守权限了。

文件权限：

#文件属性

守夜人 Jaden（吴老板）

[root@localhost ~]# ls -l /tmp/123.txt

-rw-r--r--. 1 root root 0 7月  20 23:17 /tmp/123.txt

#第一段的第一个字符，表示文件类型 -文件、d目录、l软链接(对应着windows快捷方式)、b块设备(ls

/dev，可以看到硬盘sda等)

#第一段第2-4字符，表示该文件所属用户的权限

#第一段第5-7字符，表示该文件所属用户组的权限

#第一段第8-10字符，表示其他用户对该文件的权限

r 4 代表读权限 read

w 2 代表写权限 write

x 1 代表可执行权限 executable

\- 0 空权限位，表示没有这个权限，9位权限不能少，没有的权限就用-代替。

权限值表

0 ---

1 --x

2 -w-

3 -wx

4 r--

5 r-x

<a id="page-54"></a>

> 第 54 页

6 rw-

7 rwx

ugo权限体系:

    rw-   r--    r--

    user  group  other

root没办法玩昂，因为默认权限太高。我们用普通用户来玩：用xshell开启多个窗口连接上这三个用

户。

创建三个用户并设置密码：lisi、wangwu、zhaoliu

[root@localhost ~]# useradd lisi

[root@localhost ~]# passwd lisi

更改用户 lisi 的密码 。

新的 密码：

无效的密码： 密码少于 8 个字符

重新输入新的 密码：

passwd：所有的身份验证令牌已经成功更新。

[root@localhost ~]# useradd wangwu

[root@localhost ~]# passwd wangwu

更改用户 wangwu 的密码 。

新的 密码：

无效的密码： 密码少于 8 个字符

重新输入新的 密码：

passwd：所有的身份验证令牌已经成功更新。

[root@localhost ~]#

[root@localhost ~]# useradd zhaoliu

[root@localhost ~]# passwd zhaoliu

更改用户 zhaoliu 的密码 。

新的 密码：

无效的密码： 密码少于 8 个字符

重新输入新的 密码：

守夜人 Jaden（吴老板）

passwd：所有的身份验证令牌已经成功更新。

使用lisi来登录，并创建个文件，将文件权限全部去掉，修改权限用chmod指令，全称change mode：

\# 例如：chomd -r,就是去掉r权限，chomd +r就是加上读权限，chmod +wr就是加读写权限，chmod

u+r，就是给文件属主用户添加读权限等

[lisi@localhost ~]$ touch 1.txt

[lisi@localhost ~]$ vi 1.txt

[lisi@localhost ~]$ ls -l

总用量 4

-rw-rw-r--. 1 lisi lisi 12 3月  20 09:07 1.txt

[lisi@localhost ~]$ chmod -rw 1.txt

[lisi@localhost ~]$ ls -l

总用量 4

----------. 1 lisi lisi 12 3月  20 09:07 1.txt

现在这个文件是没有任何权限的，但是文件是lisi创建的，文件属主还是lisi，虽然显示lisi也没有权限，

但是实际上lisi是可以修改文件权限的，其他用户(除了root)是没有权力修改这个文件权限的。

读权限的作用：

<a id="page-55"></a>

> 第 55 页

lisi用户：

    [lisi@localhost ~]$ chmod -rw 1.txt

    [lisi@localhost ~]$ ls -l

    总用量 4

    ----------. 1 lisi lisi 12 3月  20 09:07 1.txt

    [lisi@localhost ~]$ cat 1.txt

    cat: 1.txt: 权限不够

    [lisi@localhost ~]$ chmod u+r 1.txt

    [lisi@localhost ~]$ ls -l

    总用量 4

    -r--------. 1 lisi lisi 12 3月  20 09:07 1.txt

    [lisi@localhost ~]$ cat 1.txt

    hello jaden1

    为了方便其他用户查看，我们先将1.txt放到/tmp目录下。

    [lisi@localhost ~]$ mv 1.txt /tmp/

    [lisi@localhost ~]$ ls /tmp/

    1.txt

wangwu用户：

    [wangwu@localhost ~]$ cd /tmp/

    [wangwu@localhost tmp]$ cat 1.txt

    cat: 1.txt: 权限不够

    [wangwu@localhost tmp]$ chmod o+r 1.txt

    chmod: 更改"1.txt" 的权限: 不允许的操作

切换到lisi：给o加上r权限，再看效果

    [lisi@localhost ~]$ chmod o+r /tmp/1.txt

    [lisi@localhost ~]$ ls -l /tmp/

    总用量 8

    -r-----r--. 1 lisi lisi  12 3月  20 09:07 1.txt

再切换到wangwu来查看文件内容：

    [wangwu@localhost tmp]$ cat 1.txt

    hello jaden

写权限的作用：

守夜人 Jaden（吴老板）

但是wangwu想编辑文件，也是没有权限的。可以vi打开，但是编辑之后不能保存。

再切换到lisi，给o一个w权限，wangwu就可以编辑保存了。

    [lisi@localhost ~]$ chmod o+w /tmp/1.txt

    [lisi@localhost ~]$ ls -l /tmp/

    总用量 8

    -r-----rw-. 1 lisi lisi  12 3月  20 09:07 1.txt

wangwu编辑保存一下，查看内容：

    [wangwu@localhost tmp]$ vi 1.txt

    [wangwu@localhost tmp]$ cat 1.txt

    hello jaden

    hello wangwu

可执行权限的作用：这个需要我们创建一个命令文件才能看效果，我复制某个命令文件过来，谁复制过来的，这个文件的属主就是谁，如下

. 代表当前目录

.. 代表上一级目录

切换到lisi用户来复制ls文件到/tmp目录下，并将执行权限去掉，去掉执行权限的文件显示位白色，有执行权限的显示为绿色。

<a id="page-56"></a>

> 第 56 页

    [lisi@localhost ~]$ cd /tmp/

    [lisi@localhost tmp]$ cp /bin/ls .

    [lisi@localhost tmp]$ ls -l

    总用量 124

    -r-----rw-. 1 lisi lisi     25 3月  20 09:24 1.txt

    -rwx------. 1 root root    836 3月  15 20:14 ks-script-ed2ODG

    -rwxr-xr-x. 1 lisi lisi 117608 3月  20 09:29 ls

    [lisi@localhost tmp]$ chmod -x ls

    [lisi@localhost tmp]$ ls -l

    总用量 124

    -r-----rw-. 1 lisi lisi     25 3月  20 09:24 1.txt

    -rwx------. 1 root root    836 3月  15 20:14 ks-script-ed2ODG

    -rw-r--r--. 1 lisi lisi 117608 3月  20 09:29 ls

切换到wangwu来执行一下ls这个文件：  注意，不能直接ls，直接ls还是调用系统/bin/ls文件，需要

写./ls才是使用当前目录下的ls文件，或者写这个文件的绝对路径/tmp/ls，或者将它放到某个特定目录下，就可以直接使用对应指令而不用管路径了，这个我在下面有补充说明。

    [wangwu@localhost tmp]$ ./ls

    -bash: ./ls: 权限不够

    [wangwu@localhost tmp]$ /tmp/ls

    -bash: /tmp/ls: 权限不够

### 2、安装Xftp上传文件

如果你想自己上传一个执行文件到服务器上，我们可以使用xftp工具，如下

![第 56 页插图 1](assets/day12linux操作系统06-Linux系统/p056_img01.jpg)

守夜人 Jaden（吴老板）

点击它，提示如下

![第 56 页插图 2](assets/day12linux操作系统06-Linux系统/p056_img02.jpg)

这里就需要我们下载xftp并安装一下，不用点击下载xftp，我们直接安装我们之前下载xshell的时候一起下载的那个xftp程序即可，我也给大家准备好了

<a id="page-57"></a>

> 第 57 页

![第 57 页插图 1](assets/day12linux操作系统06-Linux系统/p057_img01.jpg)

安装即可：

![第 57 页插图 2](assets/day12linux操作系统06-Linux系统/p057_img02.jpg)

如下

守夜人 Jaden（吴老板）

![第 57 页插图 3](assets/day12linux操作系统06-Linux系统/p057_img03.jpg)

如下，可以自己修改安装路径

<a id="page-58"></a>

> 第 58 页

![第 58 页页面图](assets/day12linux操作系统06-Linux系统/p058_full.jpg)

<a id="page-59"></a>

> 第 59 页

这就安装完成了，接下来点击这里即可，xshell会自动调用我们安装好的xftp工具：

![第 59 页插图 1](assets/day12linux操作系统06-Linux系统/p059_img01.jpg)

如下

![第 59 页插图 2](assets/day12linux操作系统06-Linux系统/p059_img02.jpg)

守夜人 Jaden（吴老板）

这个工具我们先安装了解一下即可，后面用到了再细说它。

### 3、可执行程序特殊目录说明

通过echo $PATH可以看到，类似于windows的环境变量中的PATH。反式放到这个目录中的命令程序，

我们可以在任意目录下通过这个命令程序名称来直接调用命令来执行：

例如：

<a id="page-60"></a>

> 第 60 页

[lisi@localhost tmp]$ echo $PATH  # 下面这几个就是环境变量路径存放位置

/usr/local/bin:/usr/bin:/usr/local/sbin:/usr/sbin:/home/lisi/.local/bin:/home/li

si/bin

lisi@localhost tmp]$ cp ./ls /home/lisi/bin/

[lisi@localhost tmp]$ ls /home/lisi/bin/

ls

[lisi@localhost tmp]$ mv /home/lisi/bin/ls /home/lisi/bin/xxx  # 为了不和系统默认的

ls冲突，我们改名为xxx

[lisi@localhost tmp]$ ls /home/lisi/bin/

xxx

[lisi@localhost tmp]$ xxx

[lisi@localhost tmp]$ xxx  # 命令可以在任意目录下直接执行

1.txt                                    vmware-root_552-2957583561

ls

### 4、权限值

权限值：

r 4

w 2

x 1

\- 0

权限值表

0 ---

1 --x

2 -w-

3 -wx

4 r--

5 r-x

6 rw-

7 rwx

守夜人 Jaden（吴老板）

修改权限举例

如果我们想将某个文件的：rwxr-xr-x权限改为--x-w-r--，如果按照前面我们chmod指定字母的形式来修改，就比较麻烦，直接使用权限对应的数字改就很方便：

rwxr-xr-x  对应的值为：755

--x-w-r--  对应的值为：124

[lisi@localhost tmp]$ chmod 124 1.txt

[lisi@localhost tmp]$ ls -l

总用量 144

---x-w-r--. 1 lisi   lisi       25 3月  20 09:24 1.txt

别人再问你，某个文件的权限是多少的时候，我们一般都是直接报数字值，比如它的权限是755

命令32

<a id="page-61"></a>

> 第 61 页

#改变文件的权限，例如：chomd -r,就是去掉r权限，chomd +r就是加上读权限

chmod

例子1：

#修改权限之前

[test1@localhost tmp]$ ls -l

总用量 4

-rw-rw----. 1 test1 test1 8 7月  20 17:20 test1.txt

#修改权限

[test1@localhost tmp]$ chmod u+x test1.txt

#修改权限之后

[test1@localhost tmp]$ ls -l

总用量 4

-rwxrw----. 1 test1 test1 8 7月  20 17:20 test1.txt

例子2：

同时修改多个权限

[test1@localhost tmp]$ chmod u-x,g-x,o+x test1.txt

[test1@localhost tmp]$ ls -l

总用量 4

-rw-rw---x. 1 test1 test1 8 7月  20 17:20 test1.txt

例子3：数字修改更方便

[test1@localhost tmp]$ chmod 777 test1.txt

[test1@localhost tmp]$ ls -l

总用量 4

-rwxrwxrwx. 1 test1 test1 8 7月  20 17:20 test1.txt

### 5、修改文件所属

命令33：chown，全称Change Owner，改变拥有者。

#修改文件的所属,普通用户是不能修改其他用户文件的所属的，需要root用户，所以先切换到root用户来操

守夜人 Jaden（吴老板）

作

chown

例子1：修改所属用户和用户组，test2:test2，前面的test2表示用户，后面的test2是组

[root@localhost tmp]# chown test2:test2 ls

[root@localhost tmp]# ls -l

总用量 404

-rwxr-xr-x. 1 test2 test2 159024 7月  20 17:43 grep

-rwxr-xr-x. 1 test2 test2 117608 7月  20 17:38 ls

-rwxr-xr-x. 1 test1 test1 130360 7月  20 17:43 mv

-rw-rw-rw-. 1 test1 test1     14 7月  20 17:38 test1.txt

\# 修改所属用户

[root@localhost tmp]# chown test1 ls

[root@localhost tmp]# ls -l

总用量 404

-rwxr-xr-x. 1 test2 test2 159024 7月  20 17:43 grep

-rwxr-xr-x. 1 test1 test2 117608 7月  20 17:38 ls

-rwxr-xr-x. 1 test1 test1 130360 7月  20 17:43 mv

-rw-rw-rw-. 1 test1 test1     14 7月  20 17:38 test1.txt

\# 修改目录权限和所属

<a id="page-62"></a>

> 第 62 页

例子3：文件夹(目录权限)

用root用户创建一个文件夹，文件夹默认所属用户和组为root:root，那么普通用户是没全限制在这个目录中创建文件的。

[root@localhost ~]# cd /tmp/

[root@localhost tmp]# mkdir jaden

[root@localhost tmp]# ls -l

drwxr-xr-x. 2 root   root        6 3月  20 11:36 jaden

普通用户，比如lisi想在里面创建文件：

[lisi@localhost tmp]$ cd jaden/

[lisi@localhost jaden]$ touch 2.txt

touch: 无法创建"2.txt": 权限不够

如何让lisi有创建文件的权限呢？创建文件的权限就是目录写权限

首先要切换到root用户，然后用root用户修改目录权限，或者直接将目录的所属修改为lisi

修改权限：

    [root@localhost tmp]# chmod o+w jaden

    [root@localhost tmp]# ls -l

    drwxr-xrwx. 2 root   root        6 3月  20 11:36 jaden

切换到lisi，创建文件：

    [lisi@localhost jaden]$ touch 2.txt

    [lisi@localhost jaden]$ ls

    2.txt

修改所属：

    [root@localhost tmp]# chmod o-w jaden

    [root@localhost tmp]# ls -l

    drwxr-xr-x. 2 root   root       19 3月  20 11:39 jaden

    [root@localhost tmp]# chown lisi:lisi jaden

    [root@localhost tmp]# ls -l

    drwxr-xr-x. 2 lisi   lisi       19 3月  20 11:39 jaden

切换到lisi：

    [lisi@localhost jaden]$ touch 3.txt

    [lisi@localhost jaden]$ ls

    2.txt  3.txt

守夜人 Jaden（吴老板）

lisi也可以修改目录的权限了，因为它完全属于的lisi：

    [lisi@localhost tmp]$ chmod o+w jaden

    [lisi@localhost tmp]$ ls -l

    drwxr-xrwx. 2 lisi   lisi       32 3月  20 11:42 jaden

#使用uid和gid修改文件的所属用户和所属用户组  属主，属组

例子2：

[root@localhost tmp]# ls -l

总用量 404

-rwxr-xr-x. 1 test2 test2 159024 7月  20 17:43 grep

-rwxr-xr-x. 1 test1 test2 117608 7月  20 17:38 ls

-rwxr-xr-x. 1 test1 test1 130360 7月  20 17:43 mv

-rw-rw-rw-. 1 test1 test1     14 7月  20 17:38 test1.txt

[root@localhost tmp]# id test1

uid=1000(test1) gid=1000(test1) 组=1000(test1)

[root@localhost tmp]# id test2

uid=1001(test2) gid=1001(test2) 组=1001(test2)

[root@localhost tmp]# useradd  -g test1  test3

[root@localhost tmp]# id test3

<a id="page-63"></a>

> 第 63 页

uid=1002(test3) gid=1000(test1) 组=1000(test1)

[root@localhost tmp]# chown 1001:1001 test1.txt

[root@localhost tmp]# ls -l

总用量 404

-rwxr-xr-x. 1 test2 test2 159024 7月  20 17:43 grep

-rwxr-xr-x. 1 test1 test2 117608 7月  20 17:38 ls

-rwxr-xr-x. 1 test1 test1 130360 7月  20 17:43 mv

-rw-rw-rw-. 1 test2 test2     14 7月  20 17:38 test1.txt

文件权限和目录权限的解释说明：

文件权限： rwx 读写执行

目录的权限： rwx，r表示可以查看目录下有哪些文件  x表示可以cd切换到该目录  w表示可以在目录中创建、修改、删除文件等操作为了安全操作：

文件权限默认： 644权限、狠一点就给600权限

目录权限默认： 755权限、狠一点就给700权限

### 6、文件属性详解

#文件属性

[root@localhost ~]# ls -l

-rw-rw-rw-. 1 lisi   lisi     0 3月  20 16:00 222.txt

#第一段的第一个字符，表示文件类型 -文件、d目录、l软链接(对应着windows快捷方式)、b块设备(ls

/dev，可以看到硬盘sda等)

#第一段第2-4字符，表示该文件所属用户的权限

#第一段第5-7字符，表示该文件所属用户组的权限

#第一段第8-10字符，表示其他用户对该文件的权限

#第一段的第11个字符. ，表示开启selinux的状态下创建的，也证明selinux是开启状态的。

\# 看到.表示这个文件受到selinux的保护，selinux：

https://baike.baidu.com/item/SELinux/8865268?fr=aladdin，这个东西很安全，但是有了它变

守夜人 Jaden（吴老板）

得很麻烦，安全和便利一般是冲突的。主要是红帽系的系统(redhat\centos\阿里的龙蜥\华为的欧拉)有这

个机制。我们一般上来就是关闭它，安全方面我们通过其他方法来控制。查看selinux的指令：

\    # 查看状态

    [lisi@localhost tmp]$ sestatus

    SELinux status:                 enabled  # enabled表示开启状态，disabled表示禁用

状态

    SELinuxfs mount:                /sys/fs/selinux

    SELinux root directory:         /etc/selinux

    Loaded policy name:             targeted

    Current mode:                   enforcing

    Mode from config file:          enforcing

    Policy MLS status:              enabled

    Policy deny_unknown status:     allowed

    Max kernel policy version:      31

\    # 关闭和开启selinux，需要root权限才能修改

    [root@localhost tmp]# ls -l /etc/selinux/config

    -rw-r--r--. 1 root root 543 3月  15 20:11 /etc/selinux/config

    [root@localhost tmp]# vi /etc/selinux/config

    把7行改为： SELINUX=disabled  #然后保存退出，并且重启系统才会生效。

\    # 然后再登录创建文件，查看文件信息，就看不到.了

    [root@localhost ~]# touch 1.txt

<a id="page-64"></a>

> 第 64 页

    [root@localhost ~]# ls -l

    总用量 16

    -rw-r--r--  1 root root    0 3月  20 13:32 1.txt

#第二段的数字，表示该文件的硬链接数量，其实这个和我们的安全没有太大关系，运维人员需要学习，ln是

创建硬链接的指令。我们不提了

#第三段的字符串，表示该文件所属用户

#第四段的字符串，表示该文件所属用户组

#第五段的数字，表示该文件的大小，默认单位为B，如果想按照KB来显示，那么可以通过ls -lh指令来查

看。h是human的意思，以人类可读的方式显示，会自动按照文件大小来设定显示单位。

#第六段到倒数第二段，都是该文件的修改时间，只要改动了文件内容，这个时间就会自动变为修改文件时的时

间。

    #其实linux系统会记录三个时间：

\        # 访问时间(access time) 文件被打开时自动变化这个时间

\        # 修改时间(modify time) 文件内容发生变化时自动改变这个时间，ls -l 显示的就是这个时

间。

\        # 改变时间(change time) 文件属性发生变化时自动改变这个时间，文件大小也是文件的属性，

所以修改文件内容导致大小变化的时候，这个时间也会自动改变。

    #windows系统也会记录三个时间：访问时间、创建时间、修改时间

    #linux下通过stat指令来查看：

        [root@localhost ~]# stat 1.txt

          文件："1.txt"

          大小：0          块：0          IO 块：4096   普通空文件

        设备：801h/2049d   Inode：67108933    硬链接：1

        权限：(0644/-rw-r--r--)  Uid：(    0/    root)   Gid：(    0/    root)

        最近访问：2023-03-20 13:32:34.333042228 +0800

        最近更改：2023-03-20 13:32:34.333042228 +0800

        最近改动：2023-03-20 13:32:34.333042228 +0800

        创建时间：-

\    # 我们改一下文件权限，然后再看时间

        [root@localhost ~]# chmod 777 1.txt

        [root@localhost ~]# stat 1.txt

          文件："1.txt"

          大小：0          块：0          IO 块：4096   普通空文件守夜人 Jaden（吴老板）

        设备：801h/2049d   Inode：67108933    硬链接：1

        权限：(0777/-rwxrwxrwx)  Uid：(    0/    root)   Gid：(    0/    root)

        最近访问：2023-03-20 13:32:34.333042228 +0800

        最近更改：2023-03-20 13:32:34.333042228 +0800

        最近改动：2023-03-20 13:56:43.005634151 +0800  # 改动时间变了

        创建时间：-

#最一段，该文件的名称

linux一切皆文件的系统。

## 八、Linux Shell

<a id="page-65"></a>

> 第 65 页

### 1、Shell的意思

Shell： 蛋壳的意思，是linux中比较重要的一个概念，所有的命令其实都称之为shell命令。

看图解：shell就是内核的一个外壳，用户通过shell来控制内核进而驱动硬件做事情，这是它名字的由来。Linux下，没有shell的话，就不能控制这个计算机了，因为内核是用户不能直接控制的。

![第 65 页插图 1](assets/day12linux操作系统06-Linux系统/p065_img01.jpg)

我们使用的是哪个shell呢？

\# 在/etc/passwd中就可以看到：

wangwu:x:1002:1002::/home/wangwu:/bin/bash

\# 后面这个/bin/bash，就是我们目前使用的shell，后面我们还会更换其他shell来玩，后面再说。

chrony:x:998:996::/var/lib/chrony:/sbin/nologin

\# 如果指定的是/sbin/nologin这个shell的话，是没有办法登录系统的

shell会帮我们检测输入和输出的内容是否正确

\# 随便输入点东西，一回车，shell就检测到你这个指令不对，报错给你看

守夜人 Jaden（吴老板）

[root@localhost ~]# asdf

-bash: asdf: 未找到命令

### 2、优化ssh登录速度

如果你发现你的xshell或者ssh指令连接linux系统的时候很慢，等好久才连接成功，那么就可以按照下面的方式优化一下，目前我们没有遇到，所以这个暂时就不提了。

#修改配置文件，先备份

[root@localhost ~]# cp /etc/ssh/sshd_config /tmp/

[root@localhost ~]# vi /etc/ssh/sshd_config

#直接输入:79回车

    79  GSSAPIAuthentication no

    115 UseDNS no

输入:wq保存退出

#重启sshd服务

[root@localhost ~]# systemctl restart sshd

<a id="page-66"></a>

> 第 66 页

#如果修改失败，还原配置文件

[root@localhost ~]# cp  /tmp/sshd_config  /etc/ssh/sshd_config

[root@localhost ~]# systemctl restart sshd

### 3、shell提示符

#root用户提示符

[root@localhost ~]#

#普通用户test1的提示符

[test1@localhost ~]$

#格式：

[用户名@主机名 所在目录]#

\# 1、用户名，这个没说啥说的

\# 2、主机名：localhost是主机名，windows电脑也有主机名：我的电脑-->属性-->高级系统设置-->计

算机名，同一个网络中如果有多台计算机的话，每个计算机都应该有个自己的名字，就是主机名。Linux主机名默认叫做localhost，也是可以修改的

    [root@localhost ~]# hostname jaden

    [root@localhost ~]# logout

    退出之后，在重新登录，就看到主机名改好了，如下

    [root@jaden ~]# hostname

    jaden

\# 3、所在目录：root登录之后，默认所在目录是/root，此时~表示的/root目录，如果是普通用户登录

的，那么~表示的是用户家目录，cd切换目录的时候，显示的当前所在目录

\    # root用户：

    [root@jaden ~]# pwd

    /root

\    # 普通用户：

    [zhangsan@jaden ~]$ pwd

    /home/zhangsan

\# 4、提示符号

守夜人 Jaden（吴老板）

    #代表当前登录的用户是管理员,$代表的是当前登录用户是普通用户

#提示符格式定制，这个简单理解一下即可，一般都不改

\# 原格式：

[root@test ~]# echo $PS1

[\u@\h \W]\$   # \u是用户，\h是主机名，\W是相对路径

\# 临时修改：重新登录就又还原了

[root@test ~]#cd /usr/local/bin/

[root@test bin]#export  PS1='[\u@\h \w]\$'  # \w表示绝对路径

[root@test /usr/local/bin]#

#永久修改

[root@test 10:23:39 /usr/local/bin]#cd

[root@test 10:24:25 ~]#vi .bashrc

#找个空白的地方，插入一行

export  PS1='[\u@\h \t \w]\$'

#linux PS1可以各种定制：参考https://www.cnblogs.com/Q--T/p/5394993.html

<a id="page-67"></a>

> 第 67 页

linux路径，这个我们讲过的

相对路径  不完整路径，  例子../bin ./bin bin

绝对路径  也叫完整路径，例子/usr/local/bin/

命令34：hostname

#临时修改主机名

hostname

例子1：

[root@localhost ~]# hostname test

#需要重新登录生效

命令35：hostnamectl

hostnamectl

#查看主机的信息

[root@localhost ~]# hostnamectl

   Static hostname: localhost.localdomain

         Icon name: computer-vm

           Chassis: vm

        Machine ID: f8a89169114741a8ac6de82954c5fbcb

           Boot ID: dcf65386ccda42e29699d56101af8cf1

    Virtualization: vmware

  Operating System: CentOS Linux 7 (Core)

       CPE OS Name: cpe:/o:centos:centos:7

            Kernel: Linux 3.10.0-1127.el7.x86_64

      Architecture: x86-64

#永久修改主机名

[root@localhost ~]# hostnamectl set-hostname test

守夜人 Jaden（吴老板）

#需要重新登录生效

命令reboot，讲过了

#重启系统

reboot

例子1：

[root@test ~]# reboot

命令shutdown，讲过了

<a id="page-68"></a>

> 第 68 页

#关闭或者重启linux

shutdown

例子1：

#立即关机

[root@localhost ~]# shutdown -h now

例子2：

#5分钟之后关机，可以使用shutdown -c取消

[root@localhost ~]# shutdown -h 5

例子3：

#5分钟之后重启系统，可以使用shutdown -c取消

[root@localhost ~]# shutdown -r 5

### 4、shell基础语法

Linux的指令基本都是下面的语法结构，遇到什么指令都不用慌了。

不带参数的：

    reboot、pwd、id、ls等都可以不接参数，不多

带参数的：

    命令   参数     目标

    ls   -a -l -h   /opt   # 参数还可以合并为-alh

    rm   -rf    /opt/test1

    命令   源...   目标

    mv    源路径     目标路径

    cp

查看命令的参数： 命令 -h或者--help

    [root@test 11:12:02 /opt]#mv --help

    用法：mv [选项]... [-T] 源文件 目标文件

     或：mv [选项]... 源文件... 目录

守夜人 Jaden（吴老板）

     或：mv [选项]... -t 目录 源文件...

    #格式解释

    [选项] 可选的参数

    ...   可以有多个

我自己简单总结的：

格式1：不带参数的命令：

    reboot、pwd、id、ls等都可以不接参数，不多

格式2：带参数一个参数的指令：

    ls -l

    usermod -h  或者 usermod --help

格式3：带多个参数的指令：

    ls -a -l -h # 参数还可以合并为-alh

格式4：带参数带一个目标的指令

    ls -l /boot

    rm -rf /tmp/jaden   # 注意：千万不要rm -rf /* 这是删除根目录的意思，或者 rm -rf

/tmp/*,如果tmp目录不存在，也是删除根目录的意思。

格式5：命令带一个目标

    cd /tmp/

<a id="page-69"></a>

> 第 69 页

    ls /tmp/

    mkdir jaden

    useradd jaden

    ...

格式6：命令带多个源和目标

    cp jaden.txt /tmp/11.txt  # cp 源1  目标1

    cp 1.txt 2.txt 3.txt /tmp  # cp 源1 源2 源3 目标1

格式7：命令带多个参数、多个源和多个目标

    ls -a -l -h /tmp /root /opt

    cp -a -v /root /root2  # -v是显示拷贝过程的，-a 保留原文件属性的前提下复制文件

其他格式就不多说了。

### 5、tab键补全

最常用的一个快捷键。

补全命令：

    #如果预选的特别多

    [root@test 11:25:24 ~]#

    Display all 1400 possibilities? (y or n)

    #如果预选少

    [root@test 11:25:24 ~]#cha

    chacl   chage   chattr

补全路径：

    #如果预选的特别多

    [root@test 11:25:24 ~]#cd /etc/

    Display all 188 possibilities? (y or n)

    #如果预选少

    [root@test 11:25:24 ~]#cd /usr/src/

    debug/   kernels/

守夜人 Jaden（吴老板）

\    # 路径不存在的话就说明路径不存在

### 6、快捷键

Ctrl + a    #光标跳转至正在输入的命令行的首部

Ctrl + e    #光标跳转至正在输入的命令行的尾部

Ctrl + c    #终止前台运行的程序，比如ping指令

Ctrl + d    #在shell中，ctrl-d表示推出当前shell。

Ctrl + z    #将任务暂停，挂至后台, 执行fg命令继续运行

Ctrl + l    #清屏，和clear命令等效。

Ctrl + k    #删除从光标到行末的所有字符

Ctrl + u    #删除从光标到行首的所有字符

Ctrl + r    #搜索历史命令, 利用关键字搜索

ctrl + w    #光标往前删除一个参数，以空格为分割。

<a id="page-70"></a>

> 第 70 页

### 7、history历史命令

#历史

history

例子1:

[root@test 14:32:10 ~]#history

    1  exit

    2  ls

    3  head -1 test03.txt

    4  head -1 test03.txt|cat

    5  head -1 test03.txt|tac

    6  head -2 test03.txt|tac

    7  head -2 test03.txt|cat

    8  ip addr

    9  ip addr|tail -4

   10  ip addr|tail -4|head -1

   ......

例子2：

#使用!调用历史命令

[root@test 14:32:10 ~]#history|head -5

    1  exit

    2  ls

    3  head -1 test03.txt

    4  head -1 test03.txt|cat

    5  head -1 test03.txt|tac

[root@test 14:32:26 ~]# !3

 head -1 test03.txt

head: 无法打开"test03.txt" 读取数据: 没有那个文件或目录

#使用!调用mv开头的命令

[root@test 14:42:17 ~]#history

    1  ls -a -l .bash_history

    2  history

守夜人 Jaden（吴老板）

    3  ls

    4  history

    5  mv aaaaa.txt /tmp/

    6  history

[root@test 14:42:19 ~]#!mv  # 按回车，会自动找最近一次执行的mv开头的指令

mv aaaaa.txt /tmp/

mv: 无法获取"aaaaa.txt" 的文件状态(stat): 没有那个文件或目录

例子4：

#清除历史记录

history -c # 这是清除内存中的历史指令

删除主文件夹下面.bash_history  # 这是清除硬盘中的历史指令，内存中的指令会自动备份到.bash_history中，但是有个延迟，退出登录之后，才会将历史指令同步到硬盘文件中每个用户家目录下都有一个.bash_history，记录的是自己用户的历史指令。

.bash_history默认记录最近的1000条指令，通过echo $HISTSIZE可以查看，可以配置的更大或者更小一

些，vi /etc/profile，这个以后再说。

<a id="page-71"></a>

> 第 71 页

### 8、命令别名(花名)

#别名

alias

\# 比如：ls -l 直接可以写ll即可

例子1：

#查看别名

[root@test 15:23:17 ~]#alias

alias cp='cp -i'

alias egrep='egrep --color=auto'

alias fgrep='fgrep --color=auto'

alias grep='grep --color=auto'

alias l.='ls -d .* --color=auto'

alias ll='ls -l --color=auto'

alias ls='ls --color=auto'

alias mv='mv -i'

alias rm='rm -i'

alias which='alias | /usr/bin/which --tty-only --read-alias --show-dot --show-

tilde'

例子2：

#添加别名

[test1@test 15:24:23 ~]$alias rm='rm -i'  # -i是提示警告信息用的

[test1@test 15:27:08 ~]$alias |grep rm

alias rm='rm -i'

或者：[test1@test 15:24:23 ~]$alias rm='echo 禁止使用删除操作'

例子3：

#取消别名

[test1@test 15:27:13 ~]$unalias ls

[test1@test 15:27:47 ~]$alias |grep ls

alias别名的优先级高于系统命令

别名一定要是可执行的，不能随便定义别名，比如jaden='aaaaaaa'，执行jaden会报错，没有aaaaaaa这守夜人 Jaden（吴老板）

个指令

例子4：

#alias永久生效

[root@localhost ~]# vi .bashrc

#空白处，增加一行

alias cip='ip addr|tail -4|head -1'

接下来我们先去学习一下vi的操作，然后再来学后续内容。

## 九、Linux输入输出重定向

输入输出只能对文件进行操作，不能对目录操作。

输出：

\    >  输出重定向， 将命令执行结果不输出到屏幕上，输出到文件里，会清空原文件，所以输出的时候一

定要注意，文件名称要看好了。

        [root@localhost ~]# head -20 services > 2.txt

<a id="page-72"></a>

> 第 72 页

        [root@localhost ~]# cat 2.txt

        [root@localhost ~]# seq 100 > 1.txt

        [root@localhost ~]# echo 123 > 1.txt

        [root@localhost ~]# cat 1.txt

        123

        [root@localhost ~]#  > 1.txt  # 清空文件内容

        [root@localhost ~]# cat 1.txt

    >> 输出追加重定向，不会清空原文件

        [root@localhost ~]# echo aaaaa >> 2.txt

        [root@localhost ~]# cat 2.txt

    #标准正确输出重定向1

    #标准错误输出重定向2

        [root@localhost ~]# cat jaden.txt

        hello jaden

        what are you nongshalie!

        [root@localhost ~]# cat jadent  # 错误信息默认是打印在屏幕上的，如果我们想记录错

误信息，就可以用到标准错误输出

        cat: jadent: 没有那个文件或目录

        [root@localhost ~]# cat jaden.txt 1>1.txt 2>2.txt  # 指令正确会将数据保存到

1.txt中

        [root@localhost ~]# cat 1.txt

        hello jaden

        what are you nongshalie!

        [root@localhost ~]# cat 2.txt

        [root@localhost ~]# cat jade 1>1.txt 2>2.txt  #jade文件不存在，报错信息会进入

到2.txt中

        [root@localhost ~]# cat 1.txt

        [root@localhost ~]# cat 2.txt  # 记录了报错信息

        cat: jade: 没有那个文件或目录

输出重定向我们用的很多，输入重定向用的很少，所以简单演示一下即可。

守夜人 Jaden（吴老板）

输入：

    <  输入重定向

        [root@localhost ~]# cat < jaden.txt > 3.txt  # 将jaden.txt的数据输入过来并写

入3.txt中

        [root@localhost ~]# cat jaden.txt

    << 输入追加重定向(这个就不演示了，遇到了再说)

\    # 标准输入0，支持用户直接输入内容

        [root@localhost ~]# cat << 0

\        > 1

\        > 2

\        > 2222

\        > 0

        1

        2

        2222

        [root@localhost ~]# cat << 0 > 22.txt

\        > a

\        > b

\        > ddd

<a id="page-73"></a>

> 第 73 页

\        > 0

        [root@localhost ~]# cat 22.txt

        a

        b

        ddd

好，关于输入输出重定向就说这么多。

## 十、Linux压缩打包

### 1、tar

\# 压缩文件有时候我们也叫做归档文件。但是归档和压缩有一些区别，归档只是将多个文件捆绑成一个文件，

并没有压缩，而压缩才是将大小压缩的更小。

#Linux最常用的压缩和解压指令是：

tar：能够解压的文件格式是xx.tar.gz

    压缩：tar -zcf 压缩包路径 目标1 目标2 目标3 ...

    解压：tar -zxf 解压路径

例子1：压缩和解压文件

[root@localhost ~]# ls

123.txt  4.txt            a.txt  c.txt         jaden.txt

1.txt    anaconda-ks.cfg  b.txt  jaden.tar.gz  services

[root@localhost ~]# rm -f *

[root@localhost ~]# ls

[root@localhost ~]# cp /etc/services .

[root@localhost ~]# tar -zcf jaden.tar.gz services  #压缩文件

[root@localhost ~]# ls

jaden.tar.gz services

[root@localhost ~]# ls -lh

守夜人 Jaden（吴老板）

-rw-r--r--  1 root root 134K 3月  22 14:51 jaden.tar.gz

-rw-r--r--  1 root root 655K 3月  22 11:22 services

[root@localhost ~]# rm -f services  # 删除原文件之后就再解压

[root@localhost ~]# tar -zxf jaden.tar.gz   # 解压文件

[root@localhost ~]# ls -lh

-rw-r--r--  1 root root 134K 3月  22 14:51 jaden.tar.gz

-rw-r--r--  1 root root 655K 3月  22 11:22 services  #看到和源文件一样的文件，包括文件

属性也一样。

例子2：

#归档，但是不压缩

tar -cf

[root@localhost ~]# cp /etc/services ./shike  # 再拷贝一个services文件过来

[root@localhost ~]# ls -lh

总用量 14M

-rw-r--r-- 1 root root  13M 3月  22 14:58 2.tar.gz

-rw-r--r-- 1 root root 134K 3月  22 14:56 jaden.tar.gz

-rw-r--r-- 1 root root 655K 3月  22 14:55 services

-rw-r--r-- 1 root root 655K 3月  22 15:04 shike

[root@localhost ~]# tar -cf 3.tar.gz services shike  #归档，但是不压缩

<a id="page-74"></a>

> 第 74 页

[root@localhost ~]# ls -lh

总用量 15M

-rw-r--r-- 1 root root  13M 3月  22 14:58 2.tar.gz

-rw-r--r-- 1 root root 1.3M 3月  22 15:04 3.tar.gz  #看大小就知道没有压缩大小。

-rw-r--r-- 1 root root 134K 3月  22 14:56 jaden.tar.gz

-rw-r--r-- 1 root root 655K 3月  22 14:55 services

-rw-r--r-- 1 root root 655K 3月  22 15:04 shike

例子3：

#查看压缩包内容

[root@localhost ~]# tar -tf 3.tar.gz

services

shike

tar这个指令的参数可以不加-，比如tar tf 3.tar.gz

linux系统下解压文件的时候，不同格式的压缩包需要使用不同的命令来解压或者压缩。

### 2、gzip

#打包和压缩

gzip

#压缩文件，会自动删除原文件，和tar不同，tar会留着原文件

[root@localhost ~]# gzip services

[root@localhost ~]# ls -lh

总用量 15M

-rw-r--r-- 1 root root 133K 3月  22 14:55 services.gz

-rw-r--r-- 1 root root 655K 3月  22 15:04 shike

\# 解压，会自动删除原压缩包

[root@localhost ~]# gzip -d services.gz

[root@localhost ~]# ls -lh

总用量 16M

守夜人 Jaden（吴老板）

-rw-r--r-- 1 root root 655K 3月  22 14:55 services

-rw-r--r-- 1 root root 655K 3月  22 15:04 shike

#压缩多个文件，每一个文件产生一个单独的压缩包

[root@localhost ~]# gzip services shike

[root@localhost ~]# ls -lh

总用量 15M

-rw-r--r-- 1 root root 133K 3月  22 14:55 services.gz

-rw-r--r-- 1 root root 133K 3月  22 15:04 shike.gz

#解压缩

[root@localhost ~]# gzip -d services.gz shike.gz

[root@localhost ~]# ls -lh

总用量 16M

-rw-r--r-- 1 root root 655K 3月  22 14:55 services

-rw-r--r-- 1 root root 655K 3月  22 15:04 shike

gzip其实感觉并不太好用，但是工作中我们可能会遇到gzip的压缩包。

<a id="page-75"></a>

> 第 75 页

### 3、zip

#压缩

zip

例子1：

[root@localhost ~]# zip -r 1.zip services shike  #会保留原文件

  adding: services (deflated 80%)

  adding: shike (deflated 80%)

[root@localhost ~]# ls -lh

总用量 16M

-rw-r--r-- 1 root root 267K 3月  22 15:25 1.zip

-rw-r--r-- 1 root root 655K 3月  22 14:55 services

-rw-r--r-- 1 root root 655K 3月  22 15:04 shike

#解压

unzip

例子1： # 解压之前先把原文件删掉，以免冲突

[root@localhost ~]# unzip 1.zip

[root@localhost ~]# ls -lh

总用量 16M

-rw-r--r-- 1 root root 267K 3月  22 15:25 1.zip

-rw-r--r-- 1 root root 655K 3月  22 14:55 services

-rw-r--r-- 1 root root 655K 3月  22 15:04 shike

### 4、关于rar压缩包

windows上常见的rar格式的压缩包，在linux上其实比较难解压，需要我们安装专业的工具：

#解压rar包

#需要安装软件

守夜人 Jaden（吴老板）

yum install epel-release -y

yum install unar -y

#再进行解压

unar -o 解压路径 被解压文件路径

例如：

    unar -o /opt 456.rar

如下

<a id="page-76"></a>

> 第 76 页

![第 76 页插图 1](assets/day12linux操作系统06-Linux系统/p076_img01.jpg)

解压：

[root@localhost ~]# ls

1.zip  2.tar.gz  3.tar.gz  jaden.rar  jaden.tar  services  shike

[root@localhost ~]# mkdir xx

[root@localhost ~]# unar -o ./xx jaden.rar

jaden.rar: RAR 5

  jaden.txt  (49 B)... OK.

Successfully extracted to "./xx/jaden.txt".

[root@localhost ~]# ls xx/

jaden.txt

尽量不要给linux发送rar的压缩包。全世界通用的是zip格式的压缩包。好，关于压缩和解压我们就先说守夜人 Jaden（吴老板）这么多。

## 十一、文件传输

和Linux进行文件传输，大概有下面这么几种情况，看图

<a id="page-77"></a>

> 第 77 页

![第 77 页插图 1](assets/day12linux操作系统06-Linux系统/p077_img01.jpg)

### 1、网站下载文件

#下载文件

curl

例子1：

#下载文件

curl -o 本地存放路径 文件网址

例如：有些网站在后台可能禁了curl下载，导致下载不下来

    curl -o 123.zip https://github.com/nmap/nmap/archive/refs/heads/master.zip

wget 文件网址

\# 需要自行安装一下才有这个功能，curl是系统自带的

\# yum install -y wget

[root@localhost ~]# wget

https://github.com/nmap/nmap/archive/refs/heads/master.zip

\# wget比curl方便，最起码不需要指定文件名，curl如果不指定文件名路径的话会将文件内容打印在屏幕上

守夜人 Jaden（吴老板）

#使用curl和wget的前提是要有网

#检查网络畅通

ping

例子1：ping www.baidu.com

#如果网不通，重启网络服务

systemctl restart network

#查看文件类型

file

例子1：

file 123.zip

<a id="page-78"></a>

> 第 78 页

### 2、scp传输

我们准备两台linux虚拟机来玩：

#主要用于linux和linux服务器之间传输文件，scp要求接受数据的一方要开启了ssh服务端才行，如果你电

脑是苹果电脑mac系统，也可以使用scp来传输，mac默认ssh服务端是没有开启的，可以自行开启，客户端是可以直接使用的。windows往linux上面发送文件也可以用scp，但是只能单向的，因为windows上没有ssh

服务端。

#把本地文件推送到远程服务端

\# 格式： scp 本地文件路径 远程主机用户@远程主机ip地址:远程主机某个目录

scp typora-setup-x64.exe  root@10.0.0.128:/tmp

#把远端服务文件拉取到本地

\# 格式：scp 远程主机用户@远程主机ip地址:远程主机某个文件路径 本地路径

scp root@10.0.0.128:/tmp/typora-setup-x64.exe  .

win10及以上版本是有scp指令的，win和win之间是不能使用scp互相传文件的，因为windows上默认是没有ssh的服务端的，只有客户端。

\# windows使用scp给linux上传文件的时候，文件路径和文件名中不允许出现中文和空格。

\# 格式和上面一样

scp typora-setup-x64.exe  root@10.0.0.128:/tmp

mac系统也是直接可以使用scp来给linux上传文件的。

### 3、rz和sz

#上传和下载

rz  #上传

sz  #下载

#需要先安装lrzsz软件包，这个用的比较多

yum  install lrzsz  -y

守夜人 Jaden（吴老板）

#上传的例子

如果使用xshell，那么直接鼠标拖拽即可，或者执行rz -E选择要上传的文件

#下载的例子

sz /root/test3.tar.gz  # windows上自行选择存储目录

### 4、xftp上传下载

这个我们都会玩了，就不演示了。

<a id="page-79"></a>

> 第 79 页

![第 79 页插图 1](assets/day12linux操作系统06-Linux系统/p079_img01.jpg)

关于文件传输，我们暂时先说这么多。

## 十二、软件的安装

学习这个课程之前，我们先将虚拟机恢复一下快照。

不管是什么系统，安装软件都有多种方式。比如前面讲解windows的时候，我们也说到了几种安装方式，linux也不列外，也有多种软件安装方式。而linux安装软件其实是比windows要复杂一些的，原因

如下：

守夜人 Jaden（吴老板）

![第 79 页插图 2](assets/day12linux操作系统06-Linux系统/p079_img02.jpg)

<a id="page-80"></a>

> 第 80 页

Linux软件安装复杂主要就复杂在软件的依赖文件上了，也叫做依赖包，要想安装某个软件，先要去安装它的依赖包。

### 一、编译安装

我们有时候安装软件，下载下来的是软件源代码，不能直接运行，需要编译之后才能运行，源代码-->编译-->二进制机器码，才能运行。比如windows的某些软件是从源代码编译打包之后才生成exe程序，平常我们接触不到，大家安装的软件都是基本别人编译好的。而linux下编译之后会生成二进制的可执行文件，不是exe程序昂，和windows不同，这种文件没有后缀名。其实linux系统下就没有文件后缀名这个概念，好多后缀名都是我们人工自己加上去的，为了让自己知道文件是干嘛的，主要是给我们自己看的，区分作用。

我们用一个网站服务软件来玩一玩试试：

1.下载源码包

cd /opt/

rm -fr *

curl -o nginx.tar.gz http://nginx.org/download/nginx-1.20.1.tar.gz

2.编译安装

tar xf nginx.tar.gz

cd nginx-1.20.1/

    [root@localhost nginx-1.20.1]# ls

    auto  CHANGES  CHANGES.ru  conf  configure  contrib  html  LICENSE  man

README  src

\# 1.配置编译参数

\# 这个软件给我们提供了很多功能，我们在编译的过程中可以自己选择哪些功能要，哪些功能不要，所有功能

都要就是完整版，好多功能都不要就成了精简版，比如qq精简版，不知道大家听没听过。

./configure --prefix=/usr/local/nginx --without-pcre --without-

http_rewrite_module --without-http_gzip_module

    #我这里禁掉了一些功能，以为这些功能都需要好多依赖包，大家还不知道依赖包是怎么回事儿，所以我

就暂时先删除了。--without就是去掉的意思。--prefix=/usr/local/nginx是指定软件的安装目录，目

守夜人 Jaden（吴老板）

录不存在的话会自动创建。./是用相对路径来执行这个configure文件，用绝对路径也可以执行这个文件。这个指令执行之后，会自动检查各种依赖环境是否满足软件运行的要求，检查通过之后会生成一个叫做

Makefile的文件。

    [root@localhost nginx-1.20.1]# ls

    auto     CHANGES.ru  configure  html     Makefile  objs    src

    CHANGES  conf        contrib    LICENSE  man       README

    #多了两个文件Makefile和objs，刚才的指令主要是为了生成Makefile

\# 2.编译

make  #make会找当前目录中的Makefile文件来进行编译，这个编译过程一般是比较长的。到底多长时间

呢？1、看CPU性能  2、软件功能复杂度

    [root@localhost nginx-1.20.1]# ls

    auto     CHANGES.ru  configure  html     Makefile  objs    src

    CHANGES  conf        contrib    LICENSE  man       README

\    # 编译之后看上去目录结构和之前一样，但是objs目录里面其实多了好多东西。

    [root@localhost nginx-1.20.1]# ls objs/

    autoconf.err  nginx    ngx_auto_config.h   ngx_modules.c  src

    Makefile      nginx.8  ngx_auto_headers.h  ngx_modules.o

\    # 其中nginx文件就是我们的二进制可执行的命令文件。它是可执行的程序了，比如我们查看一下它的版

本

    [root@localhost nginx-1.20.1]# ./objs/nginx -v

<a id="page-81"></a>

> 第 81 页

    nginx version: nginx/1.20.1

\    # 到这里只是编译完了，还需要安装，其实安装就是将这个程序的某些文件放到对应的目录中去。其实我

们在上面的编译参数中已经指定好了--prefix=/usr/local/nginx，要安装到/usr/local/nginx目录中

去。

\# 3.安装

make install

\    # 查看安装目录，这就是它这个软件安装的所有文件

    [root@localhost nginx-1.20.1]# ls /usr/local/nginx/

    conf  html  logs  sbin

\    # 这样看目录结构看着不太清晰，我们可以安装一下tree这个工具，来进行目录查看

    [root@localhost nginx-1.20.1]# yum install tree -y

\    # 安装完tree之后，我们来看一下目录，看着就清晰多了，树状结构显示。

    [root@localhost nginx-1.20.1]# tree /usr/local/nginx/

    /usr/local/nginx/

    ├── conf  # 该软件的配置文件所在目录

    │   ├── fastcgi.conf

    │   ├── fastcgi.conf.default

    │   ├── fastcgi_params

    │   ├── fastcgi_params.default

    │   ├── koi-utf

    │   ├── koi-win

    │   ├── mime.types

    │   ├── mime.types.default

    │   ├── nginx.conf

    │   ├── nginx.conf.default

    │   ├── scgi_params

    │   ├── scgi_params.default

    │   ├── uwsgi_params

    │   ├── uwsgi_params.default

    │   └── win-utf

    ├── html  # 网站源代码存放目录，这个nginx其实主要是用来部署网站的，网站的代码可以放到这个

目录中

    │   ├── 50x.html

    │   └── index.html

守夜人 Jaden（吴老板）

    ├── logs  # 这个软件自带日志记录功能，记录的日志存放在这个目录中

    └── sbin

        └── nginx  # 这个是软件的关键性的启动程序，类似于我们windows安装的qq目录中的QQ.exe

    4 directories, 18 files

3.运行

指令：/usr/local/nginx/sbin/nginx，没有配置环境变量，所以要用完整路径来运行

[root@localhost nginx-1.20.1]# /usr/local/nginx/sbin/nginx

[root@localhost nginx-1.20.1]#    #看上去没什么效果，但是已经运行了

\# 可以通过浏览器访问这个nginx了，访问之前要关闭一下防火墙。

\# 关闭防火墙

systemctl stop firewalld

\# 取消防火墙的开机自启

systemctl disable firewalld

\# 使用浏览器访问http://<虚拟机的ip地址>

http://192.168.61.132/  就可以看到网站了。

<a id="page-82"></a>

> 第 82 页

关于nginx这个软件如何使用，我们后面课程中会详细的讲解，这里先简单感受一下编译安装过程即可。

\# 打包：就是将我们编译好的程序打包起来，给其他人用的时候，其他人就不用编译了，因为你已经编译好

了，我们普通用户使用的软件就是别人编译打包之后的软件。

/usr/local/nginx 这个目录就是我们编译好之后的整个软件的所有运行文件目录，我们打包它即可

\# 打包压缩

[root@localhost nginx-1.20.1]# cd /usr/local/

[root@localhost local]# ls

bin  etc  games  include  lib  lib64  libexec  nginx  sbin  share  src

[root@localhost local]# tar -zcf /tmp/nginx_jaden.tar.gz nginx

[root@localhost local]# ls

bin  etc  games  include  lib  lib64  libexec  nginx  sbin  share  src

[root@localhost local]# ls /tmp/

ks-script-ed2ODG

nginx_jaden.tar.gz

\# 推送给另外一台主机

[root@localhost tmp]# scp nginx_jaden.tar.gz root@192.168.61.135:/tmp

\# 另外一台主机的操作：解压到/usr/local目录下，然后运行

root@localhost tmp]# ls

nginx_jaden.tar.gz

[root@localhost tmp]# mv nginx_jaden.tar.gz /usr/local/

[root@localhost tmp]# cd /usr/local/

[root@localhost local]# ls

bin  etc  games  include  lib  lib64  libexec  nginx_jaden.tar.gz  sbin  share

src

[root@localhost local]# tar -zxf nginx_jaden.tar.gz

[root@localhost local]# ls

bin  etc  games  include  lib  lib64  libexec  nginx  nginx_jaden.tar.gz  sbin

share  src

[root@localhost local]# /usr/local/nginx/sbin/nginx

[root@localhost local]# systemctl stop firewalld

守夜人 Jaden（吴老板）

### 二、rpm安装

\# 刚才我们提到过，编译还是比较繁琐的，为了方便使用者，一般都会编译之后发给使用者，用起来不需要编

译，就方便多了。只要有人编译一次，将编译后的程序贡献出来，大家就可以用了。所以这些做系统的厂商也发现这样挺好，所以这些厂商干脆将自己的软件也打包一下，redhat、debian等都做了自己软件的打包工作，将自己的软件打包好之后，供用户下载使用。下载软件需要用到对应系统的包管理工具。

\# redhat系打出来的包叫做：rpm包。用yum安装的程序包其实都是rmp包，比如刚才安装的tree。rpm的包

我们也可以不使用yum而手动安装。

\# debian系打出来的包叫做：deb包。

#rpm全称：redhat package manager包管理器

\# 手动安装rpm包示例：不需要编译安装、也不用yum安装。

\# 安装wget

yum install wget -y

\# 使用wget下载rpm包

wget https://mirrors.tuna.tsinghua.edu.cn/centos/7/os/x86_64/Packages/tree-1.6.0-

10.el7.x86_64.rpm

<a id="page-83"></a>

> 第 83 页

\# 如果没有wget，可以先用curl下载：

curl -o wget.rpm

https://mirrors.tuna.tsinghua.edu.cn/centos/7/os/x86_64/Packages/wget-1.14-

18.el7_6.1.x86_64.rpm

\# 安装rpm包 #rpm -i是安装，vh是显示安装进度条的意思。

rpm -ivh tree-1.6.0-10.el7.x86_64.rpm

\# 卸载

rpm -e tree

\# 升级

rpm -Uvh  xxx.rpm

\# 查看已安装的软件

rpm -qa|grep httpd

命令

#以树状的显示指定目录下的目录和文件的名称

tree

例子1：

tree /usr/local

rpm安装软件个小问题：

比如：安装vim，会提示安装失败，需要各种依赖包，需要先去安装依赖包。

wget http://mirrors.tuna.tsinghua.edu.cn/centos/7/os/x86_64/Packages/vim-

enhanced-7.4.629-7.el7.x86_64.rpm

rpm -ivh vim-enhanced-7.4.629-7.el7.x86_64.rpm

所以，用rpm安装软件不好解决依赖包的问题，所以出来了下面的yum安装方式，自动下载安装需要的依赖包。以后都用yum来安装。

### 三、yum安装

#自动解决rpm依赖

守夜人 Jaden（吴老板）

#yum安装扩展yum仓库

yum install epel-release -y

#yum安装nginx

yum install nginx -y

#yum移除nginx

yum remove nginx -y

#查看仓库rpm的数量

yum repolist

安装方法总结

编译安装：优点： 自由定制  痛点：难度高，步骤繁琐

rpm安装：优点：安装简单   痛点：需要自己解决依赖，不支持定制

yum安装：优点：自动解决依赖，默认安装最新版  痛点：不支持定制

<a id="page-84"></a>

> 第 84 页

### 四、yum仓库(镜像站)

如下，安装工具时会提示：自动会从下面的仓库中来下载软件包，centos的官方库在国外http://mirror.

centos.org/，

![第 84 页插图 1](assets/day12linux操作系统06-Linux系统/p084_img01.jpg)

这个仓库地址是在centos中配置的，在如下配置文件中

[root@localhost ~]# cd /etc/yum.repos.d/

[root@localhost yum.repos.d]# ls

CentOS-Base.repo  CentOS-Debuginfo.repo  CentOS-Media.repo    CentOS-Vault.repo

CentOS-CR.repo    CentOS-fasttrack.repo  CentOS-Sources.repo  CentOS-x86_64-

kernel.repo

\# 有几个repo文件，表示配置了几个仓库，其中大部分是禁用状态的，默认就一个启用的CentOS-

Base.repo。比如我们看一个文件CentOS-Vault.repo

CentOS-Vault.repo如下，看不到enabled=0的表示启用状态。

守夜人 Jaden（吴老板）

![第 84 页插图 2](assets/day12linux操作系统06-Linux系统/p084_img02.jpg)

CentOS-Base.repo如下：

![第 84 页插图 3](assets/day12linux操作系统06-Linux系统/p084_img03.jpg)

但是国外的地址下载软件太慢了，所以centos官方说我允许你们和我同步，比如华为，你和我同步一下，做一个你国内的镜像库，这就是华为的yum仓库了或者说镜像站了，很多企业和学校都有自己的镜像站。那么我们yum安装的时候有看到，明明使用的是国内的镜像站呀，这是怎么做到的，其实配置文件中做了一个镜像地址列表，如下

<a id="page-85"></a>

> 第 85 页

![第 85 页插图 1](assets/day12linux操作系统06-Linux系统/p085_img01.jpg)

我们拿出来这个地址改一改：

http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=os&infra

\# $releasever表示版本

\# $basearch表示32还是64位

\# repo=os表示我们要下载的是操作系统相关的东西

\# infra这个参数没什么用，可删掉

\# 那么我们改一改网址，如下

http://mirrorlist.centos.org/?release=7&arch=x86_64&repo=os

\# 访问一下这个地址。

效果如下

守夜人 Jaden（吴老板）

![第 85 页插图 2](assets/day12linux操作系统06-Linux系统/p085_img02.jpg)

这就是为什么，我们用yum安装软件的时候，仓库地址都是国内的镜像站地址的原因了，它会自动选择离我们最近、网速最佳的几个地址来下载。

## 十三、find文件查找

文件查找，我们在windows用的比较多，系统自带的搜索方式、第三方搜索工具everything等。

linux上没有图形化界面，就要借助find指令来查了。

<a id="page-86"></a>

> 第 86 页

#文件查找

例子1：普通查询

find   /etc   -maxdepth 1  -type f  -name "pa*"

命令   目录...   查找深度     类型   文件名称包含

\# -type文件类型：f表示文件，不指定类型的话，文件和目录都会查找

\# -maxdepth查找深度：目录层级的意思，不指定的话，就按照最大深度来查找

\# "pa*"： *表示匹配任意pa开头的内容，*号还可以写在开头

![第 86 页插图 1](assets/day12linux操作系统06-Linux系统/p086_img01.jpg)

例子2：按照文件大小查找(单位kMG,k要小写，MG要大写，不带单位就按照B单位来查找)

1.查找大于100M的文件

find / -type f -size +100M

    [root@localhost tmp]# find / -type f -size +100M

    /proc/kcore

    find: ‘/proc/1945/task/1945/fdinfo/6’: 没有那个文件或目录  # proc是进程目录，有些进程运行起来之后能看到文件信息，程序运行结束之后，进程文件也消失了，所以看到proc的报错很正常，并且

proc的权限很高，不是一般人可以访问的，所以也经常会报权限不够等错误信息，所以以后看到proc的报错直接忽略即可。

    find: ‘/proc/1945/fdinfo/5’: 没有那个文件或目录

    /sys/devices/pci0000:00/0000:00:0f.0/resource1_wc

守夜人 Jaden（吴老板）

    /sys/devices/pci0000:00/0000:00:0f.0/resource1

    /var/cache/yum/x86_64/7/updates/gen/primary_db.sqlite

    /usr/lib/locale/locale-archive

    [root@localhost tmp]# ll -h /usr/lib/locale/locale-archive   #大小确实超过了

100M

    -rw-r--r--. 1 root root 102M 3月  15 20:10 /usr/lib/locale/locale-archive

2.查找小于2k的文件

find /root/nginx-1.20.2 -type f -size -2k

3.查找大于50M同时小于100M的文件

find /  -type f   -size +50M  -and -size -100M

![第 86 页插图 2](assets/day12linux操作系统06-Linux系统/p086_img02.jpg)

<a id="page-87"></a>

> 第 87 页

例子3：

忽略大小写查询

find /etc -maxdepth 1  -iname "pa*"  # i是ignore的简写，忽略的意思

![第 87 页插图 1](assets/day12linux操作系统06-Linux系统/p087_img01.jpg)

例子4：

根据修改时间查找文件

    [root@localhost ~]# stat 1.txt

      文件："1.txt"

      大小：0          块：0          IO 块：4096   普通空文件

    设备：801h/2049d   Inode：67108933    硬链接：1

    权限：(0644/-rw-r--r--)  Uid：(    0/    root)   Gid：(    0/    root)

    环境：unconfined_u:object_r:admin_home_t:s0

    最近访问：2023-03-23 09:04:35.339235371 +0800 #Access time

    最近更改：2023-03-23 09:04:35.339235371 +0800 #Modify time

    最近改动：2023-03-23 09:04:35.339235371 +0800 #Change time

    创建时间：-

时间参数：atime mtime ctime amin mmin cmin  #(time是按照天来查找，min是按分钟查找)

\# 时间单位为天

find /opt -type f -mtime -1   #-1代表一天以内，+1一天以前

守夜人 Jaden（吴老板）

\# 时间单位为分钟

[root@localhost ~]# find /root -type f -mmin -20

/root/.bash_history

/root/ReadMe.txt

/root/.lesshst

\# 查找1天之前，10天之内，修改过的文件

[root@localhost ~]# find /etc/ -type f -mtime +1 -and -mtime -10

例子5：  取反: !

例子：

    [root@localhost ~]# find /root -type f -name "*.txt" # 找名称以.txt结尾的文件

    /root/1.txt

    /root/学习前准备.txt

    [root@localhost ~]# find /root -type f ! -name "*.txt" # 找名称中不是.txt结尾的

文件

    /root/.bash_logout

<a id="page-88"></a>

> 第 88 页

    /root/.bash_profile

    ...

    [root@localhost ~]# mkdir jaden

    [root@localhost ~]# mkdir wulaoban

    [root@localhost ~]# find /root -type f  # 找文件

    /root/.bash_logout

    /root/.bash_profile

    ...

    [root@localhost ~]# find /root ! -type f  # 找文件夹

    /root/jaden

    /root/wulaoban

    ...

例子6：

根据用户来查找文件

    [root@localhost ~]# useradd jaden

    [root@localhost ~]# find / -user jaden  # 查找属于jaden用户的所有目录和文件

    ...

    /var/spool/mail/jaden

    /home/jaden

    /home/jaden/.bash_logout

    /home/jaden/.bash_profile

    /home/jaden/.bashrc

根据用户组来查

    [root@localhost ~]# find / -group jaden

    ...

例子7：

守夜人 Jaden（吴老板）

对找出的文件进行处理

\# 格式：正常的find语句+操作exec

\# 比如我们查找到了一些病毒文件，想直接删除

\# find /tmp -type f -size +10K -exec rm rf {} \;  # {}表示我们找到的那些文件，\;是这样

的：正常exec语句最后要分号结尾，但是分号在linux中有特殊的意义，比如一次性执行两个指令可以 ls -

lh;id，这样执行，所以要对;进行转义，意思是不要将;作为shell指令的分隔符，\就是转义符号。

例子：

    [root@localhost tmp]# find /tmp -name "vm*" -exec rm -rf {} \;

    find: ‘/tmp/vmware-root_560-2957190359’: 没有那个文件或目录

    find: ‘/tmp/vmware-root_555-4282367637’: 没有那个文件或目录

    find: ‘/tmp/vmware-root_631-4021718894’: 没有那个文件或目录

    [root@localhost tmp]# ls

    ks-script-ed2ODG

    nginx_jaden.tar.gz

    systemd-private-d38b668730bf4589896221daead5dbea-chronyd.service-be3NkF

    yum.log

下面的例子就不演示了。

find /root -type f -mmin -30  ! -name ".*"  -exec rm {} \;

<a id="page-89"></a>

> 第 89 页

find /root  -maxdepth 1  -type d  -name "Apa*"   -mmin -30 -exec cp -a {} /tmp

\; # 复制到tmp目录中

## 十四、进程管理

操作系统都有进程的概念，windows在任务管理器中查看，linux用ps指令来查看。

### 1、查看和关闭进程

程序：安装到你电脑或者手机上的程序文件。

进程：正在运行的程序。

#查看进程

ps

参数1：ps -ef

\# pid：全称process id，是进程编号，每次启动某个程序，它的编号可能都不一样，这个是程序启动之后

系统随机分配的。

\# uid：全称user id，是进程所属用户，也就是哪个用户启动的，我们可以切换个用户执行一下sleep

60，就可以看到效果

\# CMD中看到[]括起来的，表示这些都是系统级别的进程，比如一些硬件驱动程序之类的，这些都不要动。不

带[]的都是用户级别的。

\# ppid：全称parent process id，父进程，记录的是某个进程是由哪个进程创建出来的。可以通过

pstree工具来查看从属关系。

\# C：这个不用管。

\# STIME：全称start time，进程的启动时间。

\# TTY： 用来显示哪些是本地启动的，哪些是远程终端连接上来启动的。通过w指令可以看到哪些终端登录着

主机。只要登录成功一个终端，那就多一个终端。

\# TIME：这个没有实际用途

\# CMD：这个进程执行了什么指令。

守夜人 Jaden（吴老板）

![第 89 页插图 1](assets/day12linux操作系统06-Linux系统/p089_img01.jpg)

安装一个pstree

\# 注意：我们安装的软件的名字和使用的时候的指令名称不一定是一样的，比如lrzsz，使用的时候是rz\sz

上传下载。

\# 想查看我们想要使用的某个指令，是哪个软件包提供的，可以输入yum provides 指令名称，比如yum

provides pstree

[root@localhost ~]# yum provides pstree

[root@localhost ~]# yum install psmisc -y

[root@localhost ~]# pstree

\# 可以看到，系统的第一个进程是systemd，由他创建起来了好多其他的进程，可以看到从属关系：

systemd─┬─NetworkManager─┬─dhclient

<a id="page-90"></a>

> 第 90 页

        │                └─2*[{NetworkManager}]

        ├─VGAuthService

        ├─abrt-watch-log

        ├─abrtd

        ├─agetty

        ├─auditd───{auditd}

        ├─chronyd

        ├─crond

        ├─dbus-daemon───{dbus-daemon}

        ├─master─┬─pickup

        │        └─qmgr

        ├─polkitd───6*[{polkitd}]

        ├─rsyslogd───2*[{rsyslogd}]

        ├─sshd─┬─sshd───bash───pstree

        │      └─sshd───bash

        ├─systemd-journal

        ├─systemd-logind

        ├─systemd-udevd

        ├─tuned───4*[{tuned}]

        └─vmtoolsd───{vmtoolsd}

#关闭进程

kill pid号

例子1： kill  7851  #使用进程id号，来终止进程

       kill -9  pid号  #慎用！！！

#批量关闭进程，pkill全称program kill

pkill CMD命令名称

例子1： pkill sleep  #使用进程的命令名称，来终止进程，会中止所有CMD执行着sleep的进程的。

       pkill -9 sleep

守夜人 Jaden（吴老板）

\# kill -9，这个强大和危险的命令迫使进程在运行时突然终止，进程在结束后不能自我清理。危害是导致系

统资源无法正常释放，一般不推荐使用，除非其他办法都无效。

\# 如果想把某个远程连接踢下线，可以杀掉显示pts的远程连接进程的父进程，如下图

看图：

![第 90 页插图 1](assets/day12linux操作系统06-Linux系统/p090_img01.jpg)

<a id="page-91"></a>

> 第 91 页

### 2、查看计算机硬件信息

#查看cpu

lscpu

#查看内存命令

free -h

#查看硬盘命令

df -h  #h表示人类可读

[root@localhost ~]# df -h

文件系统        容量  已用  可用 已用% 挂载点

devtmpfs        980M     0  980M    0% /dev

tmpfs           991M     0  991M    0% /dev/shm

tmpfs           991M  9.5M  981M    1% /run

tmpfs           991M     0  991M    0% /sys/fs/cgroup

/dev/sda1       100G  2.2G   98G    3% /

tmpfs           199M     0  199M    0% /run/user/0

\# 含有tmp的表示是内存给硬盘的空间，默认会给1半内存空间，把内存当作硬盘使用，这个我们不用管。

#查看计算机的cpu，内存，进程等信息(和windows的任务管理器很像)

top

    top - 08:34:27 up 20 min,  1 user,  load average: 0.00, 0.01, 0.05

    Tasks:  89 total,   2 running,  87 sleeping,   0 stopped,   0 zombie

    %Cpu(s):  0.0 us,  0.0 sy,  0.0 ni,100.0 id,  0.0 wa,  0.0 hi,  0.0 si,  0.0

st

    KiB Mem :  2027872 total,  1779000 free,   135668 used,   113204 buff/cache

    KiB Swap:        0 total,        0 free,        0 used.  1755332 avail Mem

\    # 下面是进程信息，值得看的是每个进程占用的%CPU %MEM，CPU使用率和内存使用率

     PID USER      PR  NI    VIRT    RES    SHR S %CPU %MEM     TIME+ COMMAND

     1 root      20   0  128556   7132   4144 S  0.0  0.4   0:01.27 systemd

     2 root      20   0       0      0      0 S  0.0  0.0   0:00.00 kthreadd

守夜人 Jaden（吴老板）

     4 root       0 -20       0      0      0 S  0.0  0.0   0:00.00 kworker/0:0H

\# 08:34:27 up 20 min：表示08:34:27是系统当前时间，开机了20分钟，如果看到3:20，表示开了3小

时20分钟，看到10 days表示10天了，linux很稳定耐用，开机好多年都稳定运行着，不会卡顿。

\# 1 user ：表示当前只有一个用户在使用

\# load average: 0.00, 0.01, 0.05：平均负荷，指的是CPU的负载高不高，CPU负载高，那么平均负

荷就比较大，如果这几个值很大的时候，服务器会变得很卡。如果发现服务器卡了，就是异常情况，就可以看看这个数据。这三个值表示：1分钟、5分钟、15分钟的负载情况，load average数据是每隔5秒钟检查一次活跃的进程数，然后按特定算法计算出的数值。如果这个数除以逻辑CPU的数量，结果高于5的时候就表明系统在超负荷运转了。

\# Tasks:  89 total， 2 running,  87 sleeping, 0 stopped,   0 zombie：表示进程数量，

总共89个，2个正在运行，87个在睡眠状态，当我们的CPU是1核的时候，是在所有进程之间来回切换执行，所以只有一个或者切换速度很快的时候显示2个。 0 stopped表示停止的进程，但是这里一般都是0，以为进程结束之后会自动从内存中释放。0 zombie表示僵尸进程数量，僵尸进程是杀不死的，就是由于各种原因，系统无法自动释放的进程，僵尸进程也消耗系统资源，一般kill掉它的父进程可以杀掉僵尸进程，或者kill -9

来杀掉。但是kill -9要慎用！！！它也容易产生僵尸进程，kill会将进程运行中的信息保存下来，进程不会出问题，kill -9不会保存，强制结束进程的运行，容易出现僵尸进程。

\# 按数字1，可以查看cpu数量

<a id="page-92"></a>

> 第 92 页

\# %Cpu(s):  0.0 us,  0.0 sy,  0.0 ni,100.0 id,  0.0 wa,  0.0 hi,  0.0 si,  0.0

st，关于CPU我们其他参数不用看，就看这个100.0 id，id是idle的简写，表示100%空闲，因为我们现在

CPU使用率很低，所以显示了100%空闲。我们只关注这个参数即可，看一下CPU忙不忙就行。

\# KiB Mem :  2027872 total,  1779000 free,   135668 used,   113204 buff/cache，是

内存(英文：memroy)的描述信息，total表示总内存量，free表示可用剩余量，userd表示已经使用的量，

buff/cache表示用作缓存，是和磁盘进行读写时的缓存区域，这个参数不用管。

\# KiB Swap:        0 total,        0 free,        0 used.  1755332 avail Mem ：

Swap表示虚拟内存，这是硬盘分配给内存的一部分空间，为了当内存不足时，临时将硬盘当作内存使用。这个数值是可以自行调整的。一般自动就分配好了，所以我们不用管，实在是内存不够用的时候再加大这个虚拟内存。我现在看的是虚拟机上的虚拟内存，虚拟机不设置虚拟内存,所以显示为0。

swap虚拟内存在windows也内看到：

守夜人 Jaden（吴老板）

![第 92 页插图 1](assets/day12linux操作系统06-Linux系统/p092_img01.jpg)

## 十五、定时任务

定期执行任务（执行命令），和windows的计划任务是一样的。

#时间命令

date

例子1：

#查看时间

[root@localhost ~]# date

2021年 07月 23日 星期五 14:38:19 CST

[root@localhost ~]# date +%F

2021-07-23

[root@localhost ~]# date +%T

14:35:47

[root@localhost tmp]# date +%F\ %T

2022-01-11 10:07:50

<a id="page-93"></a>

> 第 93 页

例子2：

#修改时间和日期

[root@localhost ~]# date -s '20200723 14:40:00'

2020年 07月 23日 星期四 14:40:00 CST

\# 修改时间

[root@localhost ~]# date -s '14:40:00'

#同步时间，如果时间和当前时间不一致，可以做一下时间同步，来让时间准确起来

systemctl restart chronyd # 一次执行完是有延迟的，等待一会才看到准确时间，前提是我们有网

#定时任务的格式

\*  *  * *  *    cmd

分 时 日 月 周    命令

分：0-59

时：0-23

日：0-31

月：1-12

周：1-7

#每5分钟执行一次

*/5  *  * *  *

#每1小时的01分执行一次

01 */1 * * *

#每半个小时执行一次，下面的意思是每小时的00分和30分各执行一次

00,30  */1 * * *

#每天晚上8:00执行一次

00 20 * * *

#每个月1号晚上8:00执行

00 20 1 * *

#每年1月1号晚上8:00执行

00 20 1 1 *

守夜人 Jaden（吴老板）

#每周1、周三、周五晚上8:00执行一次

00 20 * * 1,3,5

\# 几个符号的意思：

\# * 每分钟

\# */5 每5分钟

\# 05 第5分钟

\# 每秒钟执行的任务，需要单独写脚本，繁琐一些。

#查看定时任务，遇到特殊符号%,需要添加转义符号\;

[root@localhost ~]# crontab -l

\* * * * *  echo `date +\%T` >>/tmp/time.txt

#编辑定时任务

[root@localhost ~]# crontab -e

示例：

\    * * * * *  date >> /tmp/time.txt  # 每分钟执行一次

[root@localhost ~]# crontab -l

\* * * * *  date >> /tmp/time.txt

<a id="page-94"></a>

> 第 94 页

我们可以通过cat来查看任务是否执行了，但是比较麻烦，每次手动输入cat，所以我们可以用如下指令

tail -f /tmp/time.txt  #监测文件尾部内容的变化.

[root@localhost ~]# tail -f /tmp/time.txt

2023年 03月 24日 星期五 10:58:01 CST

2023年 03月 24日 星期五 10:59:01 CST

2023年 03月 24日 星期五 11:00:01 CST

2023年 03月 24日 星期五 11:01:01 CST

\# 是这个进程再帮我们执行定时任务：

[root@localhost ~]# ps -ef|grep cron

root        581      1  0 18:05 ?        00:00:00 /usr/sbin/crond -n

\# 我们还可以自行重启这个进程

root@localhost ~]# systemctl restart crond

[root@localhost ~]# ps -ef|grep cron  # 可以看到进程启动时间变化了

root       2611      1 25 21:27 ?        00:00:00 /usr/sbin/crond -n

#改为每小时的03分执行

[root@localhost ~]# crontab -e

[root@localhost ~]# crontab -l

03 * * * *  date >> /tmp/time.txt

#修改一下系统时间

[root@localhost ~]# date -s '12:02:50'

2023年 03月 24日 星期五 12:02:50 CST

[root@localhost ~]# tail -f /tmp/time.txt

...

2023年 03月 24日 星期五 11:13:01 CST

2023年 03月 24日 星期五 11:14:01 CST

2023年 03月 24日 星期五 12:03:03 CST  # 12点03分执行的

\# crontab -e里面每一行都可以写一个定时任务，也就是可以写多个定时任务。

\# 比如，再加一个热内：每天晚上9:20自动关机

\# 20 21 * * * shutdown -h now

[root@localhost ~]# date -s '21:19:50'

2023年 03月 24日 星期五 21:19:50 CST

守夜人 Jaden（吴老板）

[root@localhost ~]# crontab -l

03 * * * *  date >> /tmp/time.txt

20 21 * * * shutdown -h now

[root@localhost ~]# date

2023年 03月 24日 星期五 21:21:03 CST

您在 /var/spool/mail/root 中有邮件

\# 错误的原因可能是需要我们写shutdown的绝对路径

[root@localhost ~]# which shutdown  # which也是查找，可以查找指令的绝对路径

/usr/sbin/shutdown

\# 这里就是想提示大家，如果指令不行，就写指令的绝对路径

\# 我们发现，没有关闭成功，并且看到了一个提示，有个邮件？我们去看一下

如果定时任务的格式，或者内容有问题，系统都会发邮件提示：

![第 94 页插图 1](assets/day12linux操作系统06-Linux系统/p094_img01.jpg)

<a id="page-95"></a>

> 第 95 页

## 十六、优化系统

现在的操作系统需要优化的地方不多了，甚至直接就可以使用，之前的老系统都需要好多优化才行。我这里简单做一些优化，大家最好和我的一致昂。我们先还原一下快照，优化好之后我们再做一个新的快

照。

### 1、优化

1.优化ssh，以防连接过慢

vi /etc/ssh/sshd_config  # 改配置文件之前，最好先做好备份，cp /etc/ssh/sshd_config

/etc/ssh/sshd_config.bak

79行：GSSAPIAuthentication no

115行：UseDNS no  # 别忘了删除前面的注释符号#

systemctl restart sshd

2.优化selinux

#修改配置文件，永久关闭

vi /etc/selinux/config

#第7行修改为

SELINUX=disabled

需要重启生效

#立即生效，临时的  #有时候有些服务器不让重启，就可以先这样临时用一下

setenforce 0

守夜人 Jaden（吴老板）

![第 95 页插图 1](assets/day12linux操作系统06-Linux系统/p095_img01.jpg)

3.关闭firewalld

systemctl stop firewalld

systemctl disable firewalld

4.安装常用软件

yum install lrzsz vim tree wget net-tools screen bash-completion tcpdump -y

<a id="page-96"></a>

> 第 96 页

\# net-tools：网络相关工具，比如ifconfig、ifconfig ens33(只看某个网卡的ip)，rpm -qa是查看

安装了哪些rpm包，具体这个软件有哪些命令，可以通过rpm -ql net-tools来查看。

\# screen：屏幕工具。

\    # 我们以后可能要远程连接某个服务器，比如服务器在国外，那么我们通过本地xshell等远程连接到目

标服务器，那么中间有要经过很多个网络设备的传输，很容易断掉连接，如果我们正在执行某个程序，突然断开连接了，那么我们执行的程序也会自动中断，如果我们不想让程序终端，就可以用到screen命令了。

    [root@localhost ~]# screen  # 会单独再给我们开启一个终端

    [root@localhost ~]# sleep 100

\    # 然后模拟一下，断开连接，在重新连接回来，还可以通过screen恢复到之前的窗口状态，发现程序还

在继续执行着。

    [root@localhost ~]# screen -ls

    There is a screen on:

        16389.pts-1.localhost   (Detached)

    1 Socket in /var/run/screen/S-root.

    [root@localhost ~]# screen -r 16389  # 恢复窗口

\    # 所以当网络不稳定的时候最好用screen来操作。

\# bash-completion：这个软件很神奇，叫做超级自动补全。这个包安装完之后，要重新登录一下才行。

\# 这个工具是tab键的加强版，输入-然后再使用tab的时候可以提示我们有哪些参数了，也就是提示信息更全

了。

[root@localhost ~]# find /etc/ -size 10k -

-amin                   -ignore_readdir_race    -path

-anewer                 -ilname                 -perm

-atime                  -iname                  -print

\# 再比如我们想下载某个软件，我记得好像是psm，然后一个tab键就自动补全包名了

[root@localhost ~]# yum install ps

psacct.x86_64        psmisc.x86_64        psutils-perl.noarch  psutils.x86_64

\# 关于优化，我们就暂时说这么多。

[root@localhost ~]# rpm -qa|wc -l  # 可以查看一下已经安装的软件包，看看是不是484个。

484

\# 优化好之后，关机做快照。

守夜人 Jaden（吴老板）

\# tcpdump： 先简单知道一下即可，后续我们还会用它，到时候再详解

\    # 这是个抓包指令，可以抓取网络传输的数据包。用户可以参考下面几个网址：

\    # https://www.bbsmax.com/A/WpdKENY1JV/

\    # https://www.codenong.com/cs105816177/

\    # https://blog.csdn.net/yangshengwei230612/article/details/110878714

\    # 后面我们会学习其他的抓包工具，比如wireshark、burp suite等等

### 2、wireshark安装使用

有人不认识wireshark的发音，说这个是鲨鱼鳍。https://www.wireshark.org ， 我给大家下载好了：

![第 96 页插图 1](assets/day12linux操作系统06-Linux系统/p096_img01.jpg)

<a id="page-97"></a>

> 第 97 页

2.1 安装

先创建个文件夹，作为它的安装目录：

![第 97 页插图 1](assets/day12linux操作系统06-Linux系统/p097_img01.jpg)

如下

守夜人 Jaden（吴老板）

<a id="page-98"></a>

> 第 98 页

![第 98 页页面图](assets/day12linux操作系统06-Linux系统/p098_full.jpg)

<a id="page-99"></a>

> 第 99 页

![第 99 页页面图](assets/day12linux操作系统06-Linux系统/p099_full.jpg)

<a id="page-100"></a>

> 第 100 页

![第 100 页插图 1](assets/day12linux操作系统06-Linux系统/p100_img01.jpg)

如下

守夜人 Jaden（吴老板）

![第 100 页插图 2](assets/day12linux操作系统06-Linux系统/p100_img02.jpg)

如下，正在安装，等待一会

<a id="page-101"></a>

> 第 101 页

![第 101 页插图 1](assets/day12linux操作系统06-Linux系统/p101_img01.jpg)

如下，弹出这个窗口，点击I Agree

守夜人 Jaden（吴老板）

![第 101 页插图 2](assets/day12linux操作系统06-Linux系统/p101_img02.jpg)

如下

<a id="page-102"></a>

> 第 102 页

![第 102 页页面图](assets/day12linux操作系统06-Linux系统/p102_full.jpg)

<a id="page-103"></a>

> 第 103 页

![第 103 页页面图](assets/day12linux操作系统06-Linux系统/p103_full.jpg)

<a id="page-104"></a>

> 第 104 页

![第 104 页插图 1](assets/day12linux操作系统06-Linux系统/p104_img01.jpg)

这样就安装完成了。

2.2 使用

打开桌面图标，可能会提示更新，忽略即可，也可以选择更新。

守夜人 Jaden（吴老板）

![第 104 页插图 2](assets/day12linux操作系统06-Linux系统/p104_img02.jpg)

然后看到了这个界面：

<a id="page-105"></a>

> 第 105 页

![第 105 页插图 1](assets/day12linux操作系统06-Linux系统/p105_img01.jpg)

选择抓取哪个网卡的数据包，查看本机的网卡信息，我的是下面这个WLAN：

守夜人 Jaden（吴老板）

![第 105 页插图 2](assets/day12linux操作系统06-Linux系统/p105_img02.jpg)

wireshark上选择它，点击抓包

<a id="page-106"></a>

> 第 106 页

![第 106 页插图 1](assets/day12linux操作系统06-Linux系统/p106_img01.jpg)

看到的数据包会比较多，因为我电脑上很多程序都在进行网络数据传输，简单看看数据包什么的即可，

我们后面课程中会详细使用。

## 十七、服务管理

服务管理，服务我们在windows课程中就讲解过，服务程序一般是开机自启动的，并且是一直运行着守夜人 Jaden（吴老板）的，提供服务的，某些软件或者系统程序需要用到它提供的功能，它就默默的在后台运行着，用户看不到服务程序的界面。linux下也有服务程序，比如xshell是一个软件，内置了ssh客户端程序，linux开机就运行着sshd服务程序，你客户端什么时候来连接我，我什么时候和你连接上，所以sshd就是一个服务

程序。

软件和服务都是程序。

软件一般是客户端，比如curl。

服务一般是给客户端提供某一个功能，7*24一直运行。

我们可以自己安装一个服务，其实就是安装一个软件，这里我们克隆一个虚拟机出来单独玩吧。

下面这个我们优化完的主机以后就不要用了，想玩什么其他功能，我们都克隆一份它来玩，它就作为我们的模板机吧。

<a id="page-107"></a>

> 第 107 页

![第 107 页插图 1](assets/day12linux操作系统06-Linux系统/p107_img01.jpg)

克隆：

守夜人 Jaden（吴老板）

![第 107 页插图 2](assets/day12linux操作系统06-Linux系统/p107_img02.jpg)

服务的操作：开机自启、重启服务、启动服务、停止服务等等。

安装服务

yum install httpd  # 网站服务程序，类似于nginx，它叫做apache

\# systemctl 是centos7上专门管理服务的命令

查看所有服务列表

systemctl list-unit-files

启动服务

<a id="page-108"></a>

> 第 108 页

systemctl  start  httpd  #start启动 或者 systemctl  start  httpd.service

\# ps -ef|grep httpd，可以看到服务进程，表示启动了。

停止服务

systemctl  stop   httpd  #stop停止

重启服务

systemctl  restart   httpd #restart重启，就是关闭再开启

查看服务状态

systemctl  status   httpd  #查看服务状态

把服务设置为开机启动

systemctl enable httpd.service

取消服务的开机自启

systemctl disable httpd.service

httpd是一个网站服务软件，我们通过浏览器访问：

![第 108 页插图 1](assets/day12linux操作系统06-Linux系统/p108_img01.jpg)

并且可以直接上传一个网站代码，上传到一个特定目录/var/www/html 目录下面：

守夜人 Jaden（吴老板）

![第 108 页插图 2](assets/day12linux操作系统06-Linux系统/p108_img02.jpg)

解压：

<a id="page-109"></a>

> 第 109 页

[root@localhost html]# tar zxf youxi.tar.gz

[root@localhost html]# ls

youxi  youxi.tar.gz

[root@localhost html]# ls youxi

ceshi  games  icon  index  index0  index1  index2  index3  index4  index5

index.html

[root@localhost html]#

访问：

![第 109 页插图 1](assets/day12linux操作系统06-Linux系统/p109_img01.jpg)

就可以玩游戏了。

守夜人 Jaden（吴老板）

<a id="page-110"></a>

> 第 110 页

![第 110 页页面图](assets/day12linux操作系统06-Linux系统/p110_full.jpg)
