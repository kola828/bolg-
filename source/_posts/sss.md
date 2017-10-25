---
title: 第一次使用Hexo + Github Page 搭建个人博客的心酸史
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