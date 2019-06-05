# 新手入坑之系统安装
第一次接触树莓派是在加入实验室的时候，当时还是有点懵的，完全不知到是什么，从那是开始，逐渐接触了树莓派。  
现在看肯定是简单的了，才接触的时候还是碰到了好多问题的。
## 给树莓派烧制系统镜像
### 配件
- 树莓派3b  
树莓派充电接口为Micro USB接口，输出电压为5V/2A，在宿舍或者外面没电的地方，充电宝也是可以供电的。
- 内存卡  
树莓派本身不带硬盘的，在树莓派上有个SD卡插口可以用SD卡来当作树莓派的硬盘。SD卡最小容量为8GB。
- 显示器    
树莓派（3b）的显示器连接口为HDMI接口，可以直接用HDMI线来连接显示器，显示器不支持HDMI的也可以使用VGA-HDMI转接线来连接。  
树莓派一般都用ssh来远程连接操作，一般烧制系统完成后打开ssh就可以在PC端进行连接了。~~（之前看过教程说烧制完成后可以在启动盘里加一个ssh的文件来开启ssh,
不过我没有尝试过。）~~
- 其余配件
鼠标，键盘等设备就不多说了。
### 系统烧制
把SD卡接到电脑上。
#### 下载系统
 [树莓派官网](https://www.raspberrypi.org)  
 [官网下载链接](https://www.raspberrypi.org/downloads/raspbian/)
#### 下载烧录工具
[WIn32DIsklmager](https://pan.baidu.com/s/12Gq_xQKLaxvxUzjFtdYU1g"百度网盘")(提取码：2g4w)    
![win](https://github.com/liytgy/raspberry/blob/master/%E5%85%A5%E5%9D%911%E2%80%94%E2%80%94%E7%B3%BB%E7%BB%9F%E5%AE%89%E8%A3%85/win32.PNG)
#### 格式化SD卡
如果原来的sd卡有东西的话，可以直接进行格式化。这里需要说明的是，安装树莓派系统后在电脑U盘那里右键格式化是没有用的，需要下载专门工具进行格式化。我这里用的是SDFormatter这款工具。  
[百度网盘](https://pan.baidu.com/s/1a2g0OZAt_hOWgsk0prqLIw)(提取码：abfa)
#### 烧制系统
打开win32diskmager，点击文件夹的图标，找到你下载的镜像路径，选择
然后！在旁边选择你读卡器的盘符！记住！不要选错！不要选错！
选择之前最好先把其他的USB设备移除！
然后点击“Write”，然后，等待系统烧制成功提示出现。
![烧制系统](https://github.com/liytgy/raspberry/blob/master/%E5%85%A5%E5%9D%911%E2%80%94%E2%80%94%E7%B3%BB%E7%BB%9F%E5%AE%89%E8%A3%85/%E7%83%A7%E5%88%B6.png)
## 使用并连接树莓派
**树莓派上电**
**将烧制好的SD卡插到树莓派上，用HDMI线连接显示器，连接电源。**
进入系统后右上角有WiFi图标，点击连接，或直接通过网线连接树莓派。
打开指令窗口，输入

>sudo raspi-config  

上下键移动，选择advanced options  移动到ssh选项，打开它。  
电脑下载[putty](https://pan.baidu.com/s/12iZLVejW3qVkSnXx4DwZdw)（ 提取码：r6nt ），advanced IP Scanner
~~（之前的链接失效了，然后自己也不需要，就不发了）~~这两个软件。  
- 打开Advanced IP Scanner,按右上角的按钮，绿色扫面按钮
等待几秒，在下面的列表里，标有raspbian （或者是raspberry Pi）的那一栏目
你就能看到树莓派的IP了  
- 打开路由器也可以查看树莓派ip
- 树莓派桌面右上角有WiFi的标志鼠标停留在那里会显示出IP地址的，或者打开命令终端输入"ifconfig"查看IP地址。
然后，打开Putty，填入树莓派IP点击连接,
过一会后就会提示Login in：的提示
你输入”pi“然后按回车键
它就会提示你输入密码，初始密码为:”raspberry”(这里需要强调的是，树莓派在远程连接输入密码时是不会显示内容的，所以尽管输入就好
~~(当时年纪小不懂事，一直以为自己的键盘坏了，直到翻看了某篇博客才知道)~~)  

---
系统安装就先到这里了
