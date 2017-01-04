---
title: Hexo+Github+Markdown搭建博客详解
date: 2016-04-29 15:51:27
tags: 
- hexo
- github
- next
categories: 
- github
---

## 引言	

**经过各种找资料，踩过各种坑，终于搭建好了hexo，域名是在万维网上买的，我的hexo是5.0.1版本，hexo不同的版本，很多配置都不一样。好吧，废话不多说了，开始吧。**

## 正文

### 配置环境
* **安装Node（必须）**
用来生成静态页面的，到Node.js官网下载相应平台的最新版本，一路安装即可。
* **安装Git（必须）**
用来把本地的hexo内容提交到github上去.
* **申请GitHub账号（必须）**
用来做博客的远程创库、域名、服务器之类的。

### 配置Github

**建立与你用户名相对应仓库，仓库名必须是 your_user_name.github.io，固定写法**

### 安装Hexo

**Node和Git都安装好后,首先创建一个文件夹,如blog,用户存放hexo的配置文件,然后进入blog里安装Hexo。**

	sudo npm install-g hexo

** 执行init命令初始化hexo,命令：**

	hexo init
	

**生成静态页面**

	hexo generate


** 启动本地服务，进行文章预览调试，命令：**

	hexo server

**浏览器输入 http://0.0.0.0:4000/ 就可以看到很丑的默认初始页了**
	
### hexo与github关联
**在本地找到 _config.yml 文件。**
文件底部有这样的属性：

	deploy:

     type: 
  改为：
  
*** (注意：冒号后边必须加空格)***
  
	 deploy:

     type: git

     repo: https://github.com/你在github的根路径/你建立的仓库名.git

     branch: master

### 本地文件推送到github

	hexo generate (生成静态页面)

    hexo deploy (远程推送)
    
 ***报错的话执行 npm install hexo-deployer-git --save 后再执行上一步***
 
 ****
 **博客初步建成**
 ****
### 美化博客
**hexo有很多配套主题，可自行百度并都有配置文档**

** 头像图片、作者名字、网站描述等网站基本属性都在`根目录`的_config.yml文件里配置 **

** 评论、搜索、统计、等功能配置都在`主题文件`的_config.yml文件里配置 **
### 发表文章
**新建文章命令后：**
	hexo new "文章名"
**在source/_posts会生成后缀名为.md的文件，支持markdown语法，里面可以设置标签名、分类名、是否开启评论功能等（markdown语法冒号后加空格）**
### 第一篇博客问世
	

