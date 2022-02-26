---
title: hexo博客搭建流程（附gitee仓库同步等）
date: 2022-02-26 18:52:44
tags:
---
## 搭建前准备
######   1：安装git 
	官网网址：https://git-scm.com/downloads（最新版可能不适配，可以安装学长给的资源）
######   2：安装node.js

## 版本检测
	1  node -v #检测node版本
	2  npm -v #检测npm版本
	3  npm config set registry http://registry.npm.taobao.org   #更换淘宝源使得下载速度更快
## 注册gitee仓库
   官网网址：https://gitee.com/education
   好处：github是国外的，gitee更快
   在gitee上注册并进入个人主页，选择新建仓库（仓库名称需与用户名完全一样）。创建完成之后保存仓库地址。

## 安装hexo并检测版本
	npm install -g hexo-cli #安装hexo
	hexo -v #检测hexo版本
## 搭建本地hexo
	git clone https://github.com/hexojs/hexo-starter.git myblog #从github上下载hexo
	cd myblog #到myblog目录下 （或 cd desktop #到桌面 cd myblog #同）
	git submodule init 
	git submodule update
	npm i
	cd myblog
	hexo generate #启动web资源（或hexo g）
	hexo server #启动本次服务 （或hexo s）# 用浏览器访问http://localhost:4000即可查看
## 创建博客
	hexo new "文章名"  #创建一篇文章，可以用中文
	用markdown编写文章
	接下来执行：
	hexo clean
	hexo generate
	hexo sever # 用浏览器访问http://localhost:4000即可查
## 安装hexo的git插件
	npm install --save hexo-deployer-git  # 安装hexo的git插件
## 与gitee仓库同步
###### 在myblog文件夹下找到_config.yml文件并打开（建议用Visual Studio Code 打开），翻到最底部，你将会看到以下代码：
---
	deploy
	type:''
###### 将其更改为：
	deploy
	type: git
	repository: <刚复制的仓库地址>
###### 然后执行命令
	hexo deploy #同步，第一次同步要输入账号，密码
###### 然后可以发现再gitee仓库上同步好了
###### 在服务里面启用gitee page服务
## 非必要：可以选择更换hexo主题
###### 主题可以在github上搜索hexo主题
###### 一个主题例子：
	git clone https://github.com/litten/hexo-theme-yilia.git themes/yilia
	# 修改一下_config.yml的theme
	hexo clean
	hexo generate
	hexo server
###### 下载后在_config.yml文件中的底部 theme：landscape处将 landspace更改为下载好的文件夹名（即：myblog下的 themes下新出现的文件夹名(文中例子应为yilia)
###### 再次执行以下命令
	hexo clean
	hexo generate
	hexo sever
###### 主题更换结束
## 笔者在进行操作时遇到的问题
###### 搭建博客是遇到了“No layout”报错，原因在于以下命令未能成功执行
	git submodule update
###### 第一次同步时出现报错情况，修改第一篇博客后出现重归只剩hello world博客的情况
	解决办法：
	在_config.yml文件下修改时，注意type：后的空格以及其他需要注意空格的情况；
	在更改和编写原博客时开启源代码模式，并注意markdown语法和空格情况
###### 同步失败后，笔者在gitee上添加了公钥，参考网址如下：
###### 1：csdn上的方法
	https://blog.csdn.net/weixin_41287260/article/details/89715885?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522164587621816780261962417%2522%252C%2522scm%2522%253A%252220140713.130102334.pc%255Fall.%2522%257D&request_id=164587621816780261962417&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~first_rank_ecpm_v1~rank_v31_ecpm-1-89715885.pc_search_result_cache&utm_term=gitee%E6%B7%BB%E5%8A%A0%E5%85%AC%E9%92%A5&spm=1018.2226.3001.4187
###### 2：gitee上官网给的方法
	https://gitee.com/help/articles/4181

###### 笔者均有尝试
###### 必要时可在百度、谷歌、csdn上查找解决方法，或通过重装来解决问题（hexo搭建时，笔者一直在hexo s上报错，就是通过重装hexo来解决的
## 另附markdown语法的网址
	https://blog.csdn.net/u014061630/article/details/81359144
---
参考资料：
技术部长黄一珂为我们编写的”第一次课“课件（以上绝大部分皆出自该课件，加上了一些笔者实践中出现的问题和笔者的操作步骤）
百度和csdn上出现的教程和方法等