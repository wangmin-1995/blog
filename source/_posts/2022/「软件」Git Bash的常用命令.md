---
title: 「软件」Git Bash的常用命令
date: 2022-07-03 14:59:06
tags:
- Git
- 命令
categories: 软件
cover: https://s2.loli.net/2022/07/03/RvuTwoDSiQsLeld.jpg 
---

---

{% btn 'https://juejin.cn/post/7003214976391315470',[「03」Git之add、branch、stash和checkout命令 - 掘金 (juejin.cn)],far fa-hand-point-right,block outline right blue larger %}

- 查看本地修改与服务器的差异

  ~~~bash
  git status
  ~~~

- 将差异文件添加，这样就可以提交了

  ~~~bash
  git add .
  ~~~

- 提交更改到服务器

  ~~~bash
  git commit -m "注释"
  ~~~

- 切换到另一个分支

  ~~~bash
  git checkout master
  ~~~

- 创建并切换到新分支

  ~~~bash
  git checkout -b 新分支
  ~~~

- 获取服务器最新的更改到本地

  ~~~bash
  git pull
  ~~~

- 将本地最新的更改上传到服务器

  ~~~bash
  git push
  ~~~

- 解决无法连接的问题，取消代理

  ~~~bash
  git config --global --unset http.proxy && git config --global --unset https.proxy
  ~~~

  
  
  test

  

---
