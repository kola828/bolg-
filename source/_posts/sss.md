---
layout: posts
title: 第一次使用Hexo + Github Page 搭建个人博客
date: 2017-09-20 14:28:19
tags: Hexo
reward: false
---

最近工作比较闲，没有什么事情做。于是想搭建一个自己的博客
开始是想用node.js+mysql弄一个尝试一下但是考虑到需要购买服务器和域名
最终决定使用Hexo + Github Page搭建一个先看看<!--more-->


下面先分享一下，使用Hexo + Github Page搭建博客的步骤吧

### 安装node

去官网下载即可

### 安装git

- 使用git可以将本地的文件推送到github仓库
- Hexo的主题是通过git管理的，而不是npm包，所以使用git可以使用各种主题包

### 申请github帐号（如果已经有了，可以省略）

- 新建gitHub仓库

此处请注意 !!!
- 输入Reposiry name　的格式为　yourname.github.io　(yourname与你的注册用户名一致，此处为固定格式。) 
- 点击  Create repository 仓库创建成功
![image](/img/artImg/09-20_one.png)
- 先不用初始化git,直接点击，然后拉到下方 GitHub Pages 那个地方,先随意选择一个主题然后清空仓库
![image](/img/artImg/09202.png)
![image](/img/artImg/09203.png)
![image](/img/artImg/09024.png)


至此gitHub的准备工作完成

### 关于Hexo

 首先中文文档奉上 https://hexo.io/zh-cn/docs/
 (注意 请尽量使用git操作，不要使用cmd命令窗口)
 -  安装hexo
 ``` 
  $ npm install -g hexo-cli
  ```
 -  安装完成后,请执行下列命令。
 ```
 $ hexo init <folder>
 $ cd <folder>
 $ npm install
 ```
Hexo 将会在指定文件夹中新建所需要的文件。目录结构如下:
```
.
├── _config.yml   //网站的配置信息
├── package.json  //应用程序的信息
├── scaffolds     //模版文件夹。当您新建文章时，Hexo 会根据 scaffold 来建立文件
├── source        //资源文件夹是存放用户资源的地方
|   ├── _drafts
|   └── _posts
└── themes        //主题 文件夹。Hexo 会根据主题来生成静态页面。
```

- 新建文章


````
$ hexo new "文章标题"

```

这样你可以在你本地的博客文件中source->_post文件夹下看到我们新建的markdown文件。
你可以是用markdown编辑器对其进行编辑

保存成功后 可以下面的命令进行本地发布,在浏览器打开 http://localhost:4000/ 就可以看到博客和刚刚发布的文章了
```
$ hexo s
```

至此博客已经搭建完成了，剩下的就是将其发布到github page上了


### 发布到github page

- 修改配置文件

打开 _config.yml 文件

修改deploy
```
deploy:
  type: git
  repo: https://github.com/kola828/kola828.github.io.git  //刚刚新建的github地址
  branch: master
```

- 发布
 运行下面的命令
 ```
 $ hexo g
 $ hexo d
 ```
访问 https://（你的github名称）.github.io/  就可以看到你的博客了

 ### 结束
 
 这篇教程只是搭建一个简单的博客，你也可以根据你的需求，进行修改.
 当然你也可以选择不同的主题对你的博客进行美化
 这篇文章里有一些好看的hexo主题推荐,希望可以给你带来帮助
 https://www.zhihu.com/question/24422335
 