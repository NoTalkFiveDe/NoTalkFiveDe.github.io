---
layout: post
date: 2020-12-05
title: "基于Jekyll和Github Page搭建个人博客"
tags: "blog"
---
## 1.Jekyll

> Jekyll是一种简单的、适用于博客的、静态网站生成引擎。它使用一个模板目录作为网站布局的基础框架，支持Markdown、Textile等标记语言的解析，提供了模板、变量、插件等功能，最终生成一个完整的静态Web站点。说白了就是，只要安装Jekyll的规范和结构，不用写html，就可以生成网站。


安装jekyll
```bash
#安装Ruby
sudo apt-get install ruby-full  zlib1g-dev build-essential

#使用gem安装jekyll和bundler
gem install jekyll bundler

```
使用jekyll搭建网页

```bash
#创建项目目录
jekyll new my-page

cd my-page

bundle install

#编译并启动jekyll服务
bundle exec jekyll serve

#
```
浏览器输入 **localhost:4000** 测试是否开启成功
  
   _

**发布新文章**：将在_post文件夹下添加.md文件，其中文件顶部加上以下头部
```bash
#注意冒号后有空格

---
layout: post
date: yyyy-mm-dd
title: "Your title"
tags: "blog"
categories: jekyll update
---
```

## 2.Github Pages
安装git和ssh

```bash
sudo apt install git 
sudo apt install openssh
```
设置标识

```bash
git config --global user.name "myname"
git config --global user.email "myemail"
```
创建ssh密钥对

```bash
ssh-keygen
#按提示一直回车

cd ～/.ssh

#将公钥写入authoried_keys
cat id_rsa.pub > authorized_keys
```
进入Github添加SSH keys

> 依次点击
> settings   
>  ssh and gpg keys   
>  new ssh key

测试公钥是否添加成功

```bash
ssh -T git@github.com

#以下为登陆成功
Hi <yourid>! You've successfully authenticated, but GitHub does not provide shell access.

```
新建仓库（用来托管个人博客项目）

> 1.设置Repository name(你的id.github.io)
> 2.勾选public
> 3.Create repository

将刚刚的项目推到新建仓库

```bash
cd my-page
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/<YourGithubID>/<YourRepositoryName>.git
git push -u origin main

#可能会验证你的github帐号密码
```
部署Github Pages

> 进入刚刚新建的仓库
> settingss
> 下拉
> Github Pages大标题的Source下，选择main分支，并save

至此，基于Jekyll和Github Page搭建个人博客就搭建好了。

一杯茶的功夫应该就部署好了

访问地址如下：

```bash
#id换成自己的
https://<YourGithubId>.github.io
```


