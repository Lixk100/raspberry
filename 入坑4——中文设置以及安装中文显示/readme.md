**中文设置**

可以先打开浏览器输入[www.baidu.com](www.baidu.com) 看一下，正常情况下它应该是乱码的

所以说需要安装中文支持

**安装中文字体**

sudo apt-get -y install ttf-wqy-zenhei

到这里重启的话其实就可以了，打开百度你会发现乱码问题解决了的。

**设置显示中文**

额，进入树莓派系统后你会发现一个特别尴尬的问题，树莓派是没有预置中文的，所以如果感觉自己英语水平实在不行，那就需要转换成中文了。

（不过还是建议英文状态输入，或者可以记下按键布局后改回英文）

**在终端下执行命令**

sudo raspi-config

操作提示：按空格键在前面打钩或者去掉勾（星号=勾），PageUp

PageDown 快速翻页，Tab键跳到OK按钮上

去掉en_GB.UTF-8 UTF-8，勾上：“en_US.UTF-8 UTF-8”、“zh_CN.UTF-8 UTF-8”、“zh_CN.GBK GBK”，下一屏幕默认语言选zh_CN.UTF-8。

安装中文输入法

sudo apt-get -y install scim-pinyin

如果需要加装五笔，在执行

sudo apt-get -y install scim-tables-zh

重启生效

sudo reboot
