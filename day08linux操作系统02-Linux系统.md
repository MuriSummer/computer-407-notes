# Linux系统

来源 PDF：Linux系统.pdf（原文件位于课程目录，本文件夹不包含 PDF）

<a id="page-1"></a>

> 第 1 页

Linux系统(守夜人 Jaden（吴老板）)

## 一、简单介绍

Unix，前面其实我们也介绍过，现在的操作系统的鼻祖，windows、mac、linux都是由它发展而来，

1969年诞生于贝尔实验室，作者主要有两个，其中一个大佬叫肯尼斯·蓝·汤普森，当初为了玩游戏发明了Unix操作系统，1970年正式发布，所以1970年称为操作系统元年，所有操作系统都以这个时间来计时，系统奔溃或者多年不用，断电很久，等我们再使用它的时候，时间都会从1970年1月1日0时0分0秒开始显示。

守夜人 Jaden（吴老板）

![第 1 页插图 1](assets/day08linux操作系统02-Linux系统/p001_img01.jpg)

ios、mac os等苹果的第一代操作系统于1984年发布。

windows 1.0 于1985年发布。

linux，于1991年发布，是林纳斯.托瓦兹在大学期间发开的了linux内核1.0/GPL，发展至今已经是能够与Windows抗衡了，很多企业服务器都在用，个人电脑也有在用的，比较少，而且国产系统好多都是基于Linux开发的，比如统信的UOS，如果未来国产的操作系统都普及了之后，微软的市场就没有了。

当时林纳斯.托瓦兹只是开发了linux内核，它可以兼容unix的各种系统软件，所以基于unix开发的各种系统软件，都是可以直接在linux上使用的。操作系统只有内核的话，用户是不能直接使用的，都需要各种系统软件才能正常使用。所以linux也叫做类unix，也就是unix-like。

<a id="page-2"></a>

> 第 2 页

![第 2 页插图 1](assets/day08linux操作系统02-Linux系统/p002_img01.jpg)

市面上的操作系统，基本都是基于unix\linux内核，研发了自己的很多系统软件，封装为了自己的操作

系统。

![第 2 页插图 2](assets/day08linux操作系统02-Linux系统/p002_img02.jpg)

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

![第 3 页插图 1](assets/day08linux操作系统02-Linux系统/p003_img01.jpg)

虽然最新的已经到8.x版本了，但是企业现在用的最多的还是7.x版本。我们使用7.8.2003即可：

centos的ios镜像下载地址：https://mirrors.tuna.tsinghua.edu.cn/centos-vault/7.8.2003/isos/x86_6

4/CentOS-7-x86_64-DVD-2003.iso

我已经给大家下载好了，如下

![第 3 页插图 2](assets/day08linux操作系统02-Linux系统/p003_img02.jpg)

<a id="page-4"></a>

> 第 4 页

### 2、Centos虚拟机的安装

我这里有之前安装的Centos7的虚拟机，我把它删除掉

![第 4 页插图 1](assets/day08linux操作系统02-Linux系统/p004_img01.jpg)

那么接下来我们安装Centos虚拟机：

首选创建一个存放虚拟机的文件夹：

守夜人 Jaden（吴老板）

![第 4 页插图 2](assets/day08linux操作系统02-Linux系统/p004_img02.jpg)

打开VMware，安装虚拟机：

<a id="page-5"></a>

> 第 5 页

![第 5 页页面图](assets/day08linux操作系统02-Linux系统/p005_full.jpg)

<a id="page-6"></a>

> 第 6 页

![第 6 页页面图](assets/day08linux操作系统02-Linux系统/p006_full.jpg)

<a id="page-7"></a>

> 第 7 页

![第 7 页页面图](assets/day08linux操作系统02-Linux系统/p007_full.jpg)

<a id="page-8"></a>

> 第 8 页

![第 8 页页面图](assets/day08linux操作系统02-Linux系统/p008_full.jpg)

<a id="page-9"></a>

> 第 9 页

![第 9 页页面图](assets/day08linux操作系统02-Linux系统/p009_full.jpg)

<a id="page-10"></a>

> 第 10 页

![第 10 页页面图](assets/day08linux操作系统02-Linux系统/p010_full.jpg)

<a id="page-11"></a>

> 第 11 页

![第 11 页页面图](assets/day08linux操作系统02-Linux系统/p011_full.jpg)

<a id="page-12"></a>

> 第 12 页

![第 12 页插图 1](assets/day08linux操作系统02-Linux系统/p012_img01.jpg)

### 3、系统初始化

字体变为白色表示选中了，选择第一个

守夜人 Jaden（吴老板）

![第 12 页插图 2](assets/day08linux操作系统02-Linux系统/p012_img02.jpg)

如下，选择中文

<a id="page-13"></a>

> 第 13 页

![第 13 页插图 1](assets/day08linux操作系统02-Linux系统/p013_img01.jpg)

如下，默认系统自动安装的软件很少，作为服务器来讲的话，软件需要安装的少一些，但是为了我们自己学习研究，我们还是安装的多一些，windows不会这样，直接就给你装一堆的系统软件，我们点击如下位置：

守夜人 Jaden（吴老板）

![第 13 页插图 2](assets/day08linux操作系统02-Linux系统/p013_img02.jpg)

如下，下面GNOME就是桌面的意思，我们学linux不用桌面，用了桌面学不到精髓，而且桌面本身也是个程序，会消耗系统资源和性能，所以企业服务器上基本都不会安装桌面。

<a id="page-14"></a>

> 第 14 页

![第 14 页插图 1](assets/day08linux操作系统02-Linux系统/p014_img01.jpg)

如下，我们设定分区，跟windows一样，Linux也是有分区的。

守夜人 Jaden（吴老板）

![第 14 页插图 2](assets/day08linux操作系统02-Linux系统/p014_img02.jpg)

如下，默认是自动分区的，但是默认分区分出来的效果不好，该大不大，该小不小的，我们还是手动分

区。

<a id="page-15"></a>

> 第 15 页

![第 15 页插图 1](assets/day08linux操作系统02-Linux系统/p015_img01.jpg)

如下

守夜人 Jaden（吴老板）

![第 15 页插图 2](assets/day08linux操作系统02-Linux系统/p015_img02.jpg)

如下，在linux下不和windows似的，有C盘、D盘..等盘符，它只有一个根盘符，就是/ ，剩下的目录都是再它之下的子目录。先将所有空间给/ 。

<a id="page-16"></a>

> 第 16 页

![第 16 页插图 1](assets/day08linux操作系统02-Linux系统/p016_img01.jpg)

如下

守夜人 Jaden（吴老板）

![第 16 页插图 2](assets/day08linux操作系统02-Linux系统/p016_img02.jpg)

可能会提出如下警告，说我们这么分不太合理，没事，先忽略，直接点击完成

<a id="page-17"></a>

> 第 17 页

![第 17 页插图 1](assets/day08linux操作系统02-Linux系统/p017_img01.jpg)

如下，点击接受

守夜人 Jaden（吴老板）

![第 17 页插图 2](assets/day08linux操作系统02-Linux系统/p017_img02.jpg)

如下，关闭Kdump功能，因为对我们现在学习来讲，没什么用，反而占用内存。

<a id="page-18"></a>

> 第 18 页

![第 18 页插图 1](assets/day08linux操作系统02-Linux系统/p018_img01.jpg)

关闭：

守夜人 Jaden（吴老板）

![第 18 页插图 2](assets/day08linux操作系统02-Linux系统/p018_img02.jpg)

接下来设置网络和主机名：

<a id="page-19"></a>

> 第 19 页

![第 19 页插图 1](assets/day08linux操作系统02-Linux系统/p019_img01.jpg)

如下，Linux的网卡默认是关闭的，想上网就需要我们手动打开，如下

守夜人 Jaden（吴老板）

![第 19 页插图 2](assets/day08linux操作系统02-Linux系统/p019_img02.jpg)

接下来就点击开始安装即可：

<a id="page-20"></a>

> 第 20 页

![第 20 页插图 1](assets/day08linux操作系统02-Linux系统/p020_img01.jpg)

如下，安装中，安装过程中设置个密码，Linux默认有一个root用户，类似于我们windows的

administrator用户，是超级管理员用户，我们上来就只有这么一个root用户，给它设置一个密码，不然一会进入系统的时候还是会让你先设置密码。

守夜人 Jaden（吴老板）

![第 20 页插图 2](assets/day08linux操作系统02-Linux系统/p020_img02.jpg)

如下，当你点击完成的时候，可能提示你密码太弱了，不管他，再点击完成即可

<a id="page-21"></a>

> 第 21 页

![第 21 页插图 1](assets/day08linux操作系统02-Linux系统/p021_img01.jpg)

如下，在这个界面等待即可，它在自行安装和配置。

守夜人 Jaden（吴老板）

![第 21 页插图 2](assets/day08linux操作系统02-Linux系统/p021_img02.jpg)

等待一会之后，就可以看到如下界面，点击重启

<a id="page-22"></a>

> 第 22 页

![第 22 页插图 1](assets/day08linux操作系统02-Linux系统/p022_img01.jpg)

等待一会后，看到如下界面，表示系统启动成功了，可以登录了。

![第 22 页插图 2](assets/day08linux操作系统02-Linux系统/p022_img02.jpg)

### 4、登录系统

先输入用户名：root，在输入密码：123456，输入密码的时候是不显示的。

我们先输入错误一次，看看提示信息：

守夜人 Jaden（吴老板）

![第 22 页插图 3](assets/day08linux操作系统02-Linux系统/p022_img03.jpg)

如下

![第 22 页插图 4](assets/day08linux操作系统02-Linux系统/p022_img04.jpg)

输入logout指令，按回车，表示退出登录

<a id="page-23"></a>

> 第 23 页

![第 23 页插图 1](assets/day08linux操作系统02-Linux系统/p023_img01.jpg)

就回到了登录界面

![第 23 页插图 2](assets/day08linux操作系统02-Linux系统/p023_img02.jpg)

那么这个系统是不能使用鼠标的，而且不能复制黏贴，所以我们操作这个系统，一般都是通过一些工具远程连接上这个系统来进行操作，并且工具提供了复制黏贴等各种操作功能。

## 三、远程连接工具连接控制系统

使用系统自带的ssh工具即可连接这个centos虚拟机，但是需要知道虚拟机的ip地址，那么接下来我们再学习一个linux操作指令，查看ip地址：

查看网络信息的指令：ip addr  # 中间有多少空格都没有关系

如下，我的ip地址为192.168.61.131

守夜人 Jaden（吴老板）

![第 23 页插图 3](assets/day08linux操作系统02-Linux系统/p023_img03.jpg)

### 1、ssh远程连接linux

1.1 windows的指令终端连接linux

使用我们的windows或者linux的物理机或者虚拟机都可以连接上它，指令如下

语法：ssh 用户名@ip地址

比如：ssh root@192.168.61.131

如下

<a id="page-24"></a>

> 第 24 页

![第 24 页插图 1](assets/day08linux操作系统02-Linux系统/p024_img01.jpg)

如下

![第 24 页插图 2](assets/day08linux操作系统02-Linux系统/p024_img02.jpg)

在上面这个界面，就可以进行复制黏贴了，复制某个指令，在这个窗口点击鼠标右键，就直接黏贴了。

这个有点类似于windows的远程桌面功能，也是远程控制主机的一种方式。

但是这种windows自带的ssh远程连接控制方式来控制Linux系统有些不方便，比如每次都要输入ssh那个连接指令，感觉就麻烦，所以远程控制Linux系统有一些专业的工具，比如xshell、iTerm2(mac电脑上用的)、secureCRT、Tabby、OpenSSH等等，windows上最好用的就是xshell这个工具了。

接下来我们学习一下xshell。

1.2 xshell下载安装

1.2.1 xshell下载

在官网下载即可，地址：https://www.xshell.com/zh/xshell/

守夜人 Jaden（吴老板）

![第 24 页插图 3](assets/day08linux操作系统02-Linux系统/p024_img03.jpg)

如下，需要得到一个免费授权：

<a id="page-25"></a>

> 第 25 页

![第 25 页插图 1](assets/day08linux操作系统02-Linux系统/p025_img01.jpg)

如下，大家输入一下邮箱，后面安装xshell的过程中需要输入这个邮箱：

守夜人 Jaden（吴老板）

![第 25 页插图 2](assets/day08linux操作系统02-Linux系统/p025_img02.jpg)

我也给大家下载好了，如下

![第 25 页插图 3](assets/day08linux操作系统02-Linux系统/p025_img03.jpg)

1.2.3 xshell安装

这个直接安装到我们的物理机上即可，我物理机上已经有了，我用虚拟机给大家安装一下：

<a id="page-26"></a>

> 第 26 页

![第 26 页页面图](assets/day08linux操作系统02-Linux系统/p026_full.jpg)

<a id="page-27"></a>

> 第 27 页

![第 27 页页面图](assets/day08linux操作系统02-Linux系统/p027_full.jpg)

<a id="page-28"></a>

> 第 28 页

![第 28 页页面图](assets/day08linux操作系统02-Linux系统/p028_full.jpg)

<a id="page-29"></a>

> 第 29 页

![第 29 页插图 1](assets/day08linux操作系统02-Linux系统/p029_img01.jpg)

看到这里，表示安装完成了。

注意，如果提示更新，不要更新

守夜人 Jaden（吴老板）

![第 29 页插图 2](assets/day08linux操作系统02-Linux系统/p029_img02.jpg)

1.3 xshell连接Linux

新建连接：

<a id="page-30"></a>

> 第 30 页

![第 30 页插图 1](assets/day08linux操作系统02-Linux系统/p030_img01.jpg)

如下

守夜人 Jaden（吴老板）

![第 30 页插图 2](assets/day08linux操作系统02-Linux系统/p030_img02.jpg)

然后点击用户身份验证：

<a id="page-31"></a>

> 第 31 页

![第 31 页插图 1](assets/day08linux操作系统02-Linux系统/p031_img01.jpg)

如下，输入用户名和密码，然后点击确定

守夜人 Jaden（吴老板）

![第 31 页插图 2](assets/day08linux操作系统02-Linux系统/p031_img02.jpg)

如下，看到一个名称，以后双击这个名称就可以连接了，注意你要连接的那个Linux系统必须开着机呢昂

<a id="page-32"></a>

> 第 32 页

![第 32 页插图 1](assets/day08linux操作系统02-Linux系统/p032_img01.jpg)

双击它，如下，如果双击一次之后提示没有连接成功，那么再次双击一下试试。

守夜人 Jaden（吴老板）

![第 32 页插图 2](assets/day08linux操作系统02-Linux系统/p032_img02.jpg)

如下

<a id="page-33"></a>

> 第 33 页

![第 33 页插图 1](assets/day08linux操作系统02-Linux系统/p033_img01.jpg)

退出登录，输入exit，如下

守夜人 Jaden（吴老板）

![第 33 页插图 2](assets/day08linux操作系统02-Linux系统/p033_img02.jpg)

双击连接名，又可以连接上：

![第 33 页插图 3](assets/day08linux操作系统02-Linux系统/p033_img03.jpg)

<a id="page-34"></a>

> 第 34 页

设置字体大小：

![第 34 页插图 1](assets/day08linux操作系统02-Linux系统/p034_img01.jpg)

这个工具就是以后我们主要使用的一个工具，它的功能先说到这里。

1.4 做快照

我们刚刚安装好的系统，最好做一个快照，万一哪天玩坏了，还可以还原回来。关机状态下做快照会更快一些。

关机指令，这个指令可以直接在xshell上输入，我这里就直接在虚拟机上输入了。

守夜人 Jaden（吴老板）

![第 34 页插图 2](assets/day08linux操作系统02-Linux系统/p034_img02.jpg)

如下

<a id="page-35"></a>

> 第 35 页

![第 35 页页面图](assets/day08linux操作系统02-Linux系统/p035_full.jpg)

<a id="page-36"></a>

> 第 36 页

![第 36 页插图 1](assets/day08linux操作系统02-Linux系统/p036_img01.jpg)

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

![第 37 页插图 1](assets/day08linux操作系统02-Linux系统/p037_img01.jpg)

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

![第 40 页插图 1](assets/day08linux操作系统02-Linux系统/p040_img01.jpg)

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

![第 43 页插图 1](assets/day08linux操作系统02-Linux系统/p043_img01.jpg)

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

![第 46 页插图 1](assets/day08linux操作系统02-Linux系统/p046_img01.jpg)

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

![第 48 页插图 1](assets/day08linux操作系统02-Linux系统/p048_img01.jpg)

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

## 八、Linux Shell

守夜人 Jaden（吴老板）

## 九、Linux输入输出重定向

## 十、Linux压缩打包

## 十一、文件传输

## 十二、软件的安装

## 十三、find文件查找

<a id="page-54"></a>

> 第 54 页

## 十四、进程管理

## 十五、定时任务

## 十六、优化系统

## 十七、服务管理

守夜人 Jaden（吴老板）

<a id="page-55"></a>

> 第 55 页

![第 55 页页面图](assets/day08linux操作系统02-Linux系统/p055_full.jpg)
