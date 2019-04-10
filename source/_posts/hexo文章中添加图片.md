---
title: hexo文章中添加图片
date: 2019-04-10 21:31:55
tags: ['hexo', '图片插件']
categories: hexo
---
# hexo 添加图片插件

安装图片插件

```
npm install hexo-asset-image --save
```

![1554900187868](1554900187868.png)

在_config.yml配置文件中，修改为 post_asset_folder: true， 然后新建一篇文章 

```
hexo new post ceshi
```

![1554902676171](1554902676171.png)

这个时候会出现一个ceshi.md  和 ceshi的文件夹

然后就可以在文章中引用了 

![1554902983670](1554902983670.png)

重新编译一下 然后启动服务

![1554903016817](1554903016817.png)

当然也可以使用cdn来存储图片，这样速度会相对来说快一点