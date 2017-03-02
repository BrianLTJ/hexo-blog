---
title: 使用Hexo生成静态博客
tags: 
- hexo部署
- server
---

最近打算重启写博客这事儿，本来是用Django后台+Vue前端，不过工期拖得有点长，因此就暂且用Hexo部署一个静态博客。

[Hexo](https://hexo.io)是一个基于NodeJS的博客框架。编写博客文章使用了Markdown语法，最终Hexo将会生成一个全静态的博客网站供发布。生成的博客网站支持归档查阅，添加了对应插件后还能自动生成RSS订阅。

# 建立Hexo项目

首先确保电脑安装了NodeJS、npm以及Git，在命令行中运行`$ npm install hexo-cli -g`，这样hexo的命令行工具就会被安装到系统全局。

如果要建立一个名为 my-blog的博客，在任意某个位置建立文件夹，在该文件夹下运行`$ hexo init`，hexo命令行工具将会自动把一个基本的库从Git仓库拉取下来，同时安装各种依赖。

等所有的依赖都安装完毕，就可以键入`$ hexo server`，

{% asset_img 1.png This is an example image %}

在浏览器访问`http://localhost:4000/`就能查看网页预览了。

到目前为止，这个项目还没有生成可供访问的网站。接下来，运行`$ hexo g`命令，hexo将会在顶层目录下的public文件夹生成静态网站。这个文件夹的内容也就是最终要部署的网页文件。

# 部署到Github Pages

Github Pages是Github为方便用户快速搭建静态网站提供的一个服务。

由于最终我们只需要将public文件夹内的网页放置到服务器，因此，可以建立两个代码库，一个专门用来放置源代码，另一个放置public文件夹的内容。当然，也可以只建立一个代码库供Github Pages使用，源代码放到该库的另外一个分支。



# 部署到个人云服务器

# What's Next

- 自动更新VPS上的代码
- 配置云服务器的HTTPS访问
- 部署CDN
- 自定义Hexo主题
- 优化压缩前端资源文件
- 将发布过程打包流程化