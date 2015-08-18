# -apache
git@github.com:zcs110/-apache.git
配置Apache 
	a.	在当前用户的目录创建一个文件夹  
	b.	打开finder进入/etc/apache2  /etc/apache2 是系统目录,默认不显示 进入该目录有两种方法  i. 显示所有隐藏和系统目录 显示:defaults write com.apple.finder AppleShowAllFiles -bool true 隐藏:defaults write com.apple.finder AppleShowAllFiles -bool false  ii. 在finder的菜单栏 前往-->前往文件夹 直接输入目录  
	.	i. 显示所有隐藏和系统目录 显示:defaults write com.apple.finder AppleShowAllFiles -bool true 隐藏:defaults write com.apple.finder AppleShowAllFiles -bool false 
	.	
	.	sudo apachectl -k restart 
	.		A01-配置Apache 2015年3月31日 星期二 15:43 
	.	1. 什么是Apache a. web服务器 
	.	2. 配置Apache 
	.	在当前用户的目录创建一个文件夹  
	.	打开finder进入/etc/apache2  /etc/apache2 是系统目录,默认不显示 进入该目录有两种方法  i. 显示所有隐藏和系统目录 显示:defaults write com.apple.finder AppleShowAllFiles -bool true 隐藏:defaults write com.apple.finder AppleShowAllFiles -bool false  ii. 在finder的菜单栏 前往-->前往文件夹 直接输入目录  
	.	此目录是只读的,要想操作此目录先更改权限,打开apache2文件夹的显示简介  
	.	修改httped.conf前,先备份下该文件,修改此文件中的 DocumentRoot "/Users/你的用户名/myweb" <Directory "/Users/你的用户名/myweb">  添加上Indexes Options Indexes FollowSymLinks Multiviews  MultiviewsMatch Any  把前面的#号去掉 #LoadModule php5_module libexec/apache2/libphp5.so  
	.	3. 启动Apache的命令 sudo apachectl -k restart 重启Apache 
	.	￼ ￼
	.	分区 第二天 解析数据 的第 1 页 
	.	sudo apachectl -k restart 重启
	.	sudo apachectl -k start 启动Apache 
	.	sudo apachectl -k stop 停止Apache 


