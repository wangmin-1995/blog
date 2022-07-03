---
title: 「博客」利用Git分支上传网站源码
date: 2022-07-03 12:23:28
tags:
- Hexo
- Git
categories: 博客
cover: https://s2.loli.net/2022/07/03/vqcayoE9uZbGreQ.png 
---



---

# <center>上传源码

{% btn 'http://fangzh.top/2018/2018090715/',「[hexo教程:基本配置+更换主题+多终端工作+coding page部署分流(2) | Fangzh的个人博客 | 人工智能拯救世界]」,far fa-hand-point-right,block outline right blue larger %}

1. 在***「GitHub」***新建分支***「Hexo」***，并设置为默认分支

2. 本地任意目录***「Git Bash」***，将***「Hexo」***分支的仓库复制到本地

   ~~~bash
   git clone https://github.com/wangmin-1995/wangmin-1995.github.io.git
   ~~~

   生成的文件夹名为***「wangmin-1995.github.io」***，可重命名为***「博客」***

3. 删除***「博客」***中除***「.git」***外的所有文件夹，***「.git」***默认是隐藏的

4. 将本地仓库下所有文件复制到***「博客」***

5. 删除***「.deploy.git」***和`theme/butterfly`下的***「.git」***，这两个文件夹不能上传

6. ***「博客」***下***「Git Bash」***

   ~~~bash
   git add . && git commit -m 'add branch' && git push
   ~~~


---

# <center>使用场景

## <center>仅本地变更后上传

-  同时上传源码和布署网页

   ~~~bash
   git add . && git commit -m "new" && git push && hexo clean&&hexo g&&hexo d
   ~~~
   
   本地若无变更，无法上传，也没必要上传


## <center>仅远程变更后下载

- 只需

  ~~~bash
  git pull
  ~~~
  

## <center>本地和远程同时有变更

### 「方法一：暂存本地变更」

1. 缓存本地变更

   ~~~bash
   ~~~

   

# <center>疑难杂症

- `git push`报错：连接中止，error10053

  取消代理解决

  ~~~bash
  git config --global --unset http.proxy && git config --global --unset https.proxy
  ~~~

  也可尝试切换代理

  {% btn 'https://blog.csdn.net/LanXiu_/article/details/122325029?spm=1001.2101.3001.6650.2&utm_medium=distribute.pc_relevant.none-task-blog-2~default~CTRLIST~default-2-122325029-blog-116039735.pc_relevant_aa2&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2~default~CTRLIST~default-2-122325029-blog-116039735.pc_relevant_aa2&utm_relevant_index=5',[Github push时报错 OpenSSL_read:Connection was aborted,error 10053__LanXiu的博客-CSDN博客],far fa-hand-point-right,block outline right blue larger %}

- `git pull`无效

  {% btn 'https://blog.csdn.net/lan123456_/article/details/108976999',[拉取远程仓库代码时出现错误：Please commit your changes or stash them before you merge. Aborting_来杯卡布奇洛的博客-CSDN博客],far fa-hand-point-right,block outline right blue larger %}

  - [ ] 方式一：上传

  
  - [x] 缓存本地变更，然后`git pull`
  
    ~~~bash
    git stash && git pull
    ~~~
  
    查看缓存列表
  
    ~~~bash
    git stash list
    ~~~
  
    应用第一个缓存
  
    ~~~bash
    git add . && git stash pop
    ~~~
  
    
  
  - [ ] 放弃本地变更，用远程仓库覆盖，然后`git pull`
  
    ~~~bash
    git reset --hard && git pull
    ~~~
  
    
