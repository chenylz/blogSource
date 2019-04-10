---
title: 使用hexo搭建个人博客
date: 2019-04-10 20:52:29
tags: ['hexo', '个人博客']
categories: hexo
---
# hexo搭建个人博客教程

### 1.hexo是什么

Hexo是高效的静态站点生成框架，她基于Node.js。通过 Hexo 你可以轻松地使用Markdown 编写文章，除了Markdown 本身的语法之外，还可以使用Hexo提供的标签插件来快速的插入特定形式的内容，而且相对于其他框架，Hexo在速度上也有很大优势。

### 2.安装node.js

我们了解到Hexo基于Node.js的，那么我们搭建博客网站首先需要安装Node.js环境。 Node.js 是一个基于 Chrome V8 引擎的 JavaScript 运行环境，可以在非浏览器环境下，解释运行 JS 代码。

下载地址：http://nodejs.cn/download 

测试安装：命令行使用node -v 、npm -v，查看显示版本号即成功。

![1554848335780](1554848335780.png)

下面我们需要更换npm的镜像

```
npm get registry
npm config set registry http://registry.npm.taobao.org/
```



### 3.安装Hexo

Hexo是一个建站工具，可以帮助我们快速生成基本的博客文件，安装它需要在控制台下使用如下命令：

```
npm install hexo-cli -g
```

安装完成之后可以查看一下版本

```
hexo –v
```

出现下图就说明安装完成

![1554848653359](1554848653359.png)

### 4.新建站点

##### 新建一个站点

```
hexo init myblog
```

##### 新建完成之后cd myblog 进入该目录安装依赖

![1554849350391](1554849350391.png)

```
npm install
```

![1554849374739](1554849374739.png)

##### 所有依赖完全安装之后就可以编译代码，启动服务了

```
hexo g
```

![1554849392549](1554849392549.png)

```
hexo s
```

启动服务

![1554849425493](1554849425493.png)



##### 地址栏输入：http://localhost:4000 就可以看到效果了

![1554849475225](1554849475225.png)

### 5.部署站点到github上

首先安装git,已安装的同学请跳过

git官网：<https://git-scm.com/download>

![1554871390762](1554871390762.png)

可根据自己的系统来选择下载

安装完成之后 在桌面右键 出现该选项就说明安装成功了



![TIM截图20190410124456](TIM截图20190410124456.png)



登录自己的github 创建一个repository

![1554871826159](1554871826159.png)



将ssh地址 复制在hexo的配置文件中

![1554871901511](1554871901511.png)



![1554871968149](1554871968149.png)



##### 设置SSH keys

设置为你的邮箱地址

```
ssh-keygen -t rsa -C "yourmail"
```

然后在C:\Users\Administrator 路径下 有.ssh文件夹 打开后可以看到 刚刚生成的秘钥信息



![1554872111863](1554872111863.png)

![1554872276452](1554872276452.png)

点击add ssh key 就完成了ssh key的添加 

最后再来检测一下 

```
ssh -T git@github.com
```



![1554872439191](1554872439191.png)



下面就可以部署了

##### 生成静态页面

```
hexo generate 或者 hexo g
```

##### 部署

```
hexo deploy 或者 hexo d
```



然后输入我们的github地址 **https://chenylz.github.io**  就可以看到效果啦 





