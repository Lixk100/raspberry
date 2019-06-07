- 更新最新版的vim  
---
先卸载掉原来的vi
> sudo apt-get remove vim-common  

然后下载vim  
> sudo apt-get install vim

- 编辑软件  
编辑/etc/vim/vimrc.tiny文件    ~~（貌似需要在root权限下进行编辑，当时使用的是第一种）~~  
将 set compatible 改为 set nocompatible  
增加一行 set backspace=2  
 
