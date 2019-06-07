由于某些众所周知的原因，我们的树莓派一般需要进行换源处理，不然树莓派下载速度可能受到极大的影响。

------

需要说明的是树莓派的版本不同，更改内容也会拿受到影响。

debian9的版本为stretch 

debian8的版本为jessie

所以在更新时注意自己树莓派版本

命令行输入

lsb_release -a 查看自己的版本类型



------

执行命令:(stretch)

sudo   nano  /etc/apt/sources.list

（1）将文件里的默认的官方软件源用# 注释掉（2）添加下面的软件源（中国科技大学的软件源 ） （手动添加注意空格）

deb http://mirrors.ustc.edu.cn/raspbian/raspbian/ stretch maincontrib non-free rpi

执行命令:(stretch)

sudo  nano  /etc/apt/sources.list.d/raspi.list

（1）将文件里的默认的官方软件源用# 注释掉（2）添加下面的软件源（中国科技大学的软件源 )（手动添加注意空格）

deb http://mirrors.ustc.edu.cn/archive.raspberrypi.org/ stretch mainui

更新

sudo apt-get update

sudo apt-get upgrade

------

执行命令:(jessis)

sudo   nano  /etc/apt/sources.list

（1）将文件里的默认的官方软件源用# 注释掉（2）添加下面的软件源（中国科技大学的软件源 ） （手动添加注意空格）

deb http://mirrors.ustc.edu.cn/raspbian/raspbian/ jessis main contribnon-free rpi

执行命令:(jessis)

sudo  nano  /etc/apt/sources.list.d/raspi.list

（1）将文件里的默认的官方软件源用# 注释掉（2）添加下面的软件源（中国科技大学的软件源 )（手动添加注意空格）

deb http://mirrors.ustc.edu.cn/archive.raspberrypi.org/ jessis mainui

更新

> sudo apt-get update
>
> sudo apt-get upgrade
