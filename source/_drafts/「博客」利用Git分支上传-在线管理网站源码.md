---
title: 「博客」利用Git分支上传+在线管理网站源码
tags: 
- Git
- Hexo
cover: https://s2.loli.net/2022/07/06/3pzqfb2NIOACJX6.jpg
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

4. 将本地仓库下所有文件转移到***「博客」***，之前的仓库文件夹可以删除了

5. 删除***「博客」***下的***「.deploy.git」***、`博客/theme/butterfly`下的***「.git」***，这两个文件夹不能上传

6. ***「博客」***下***「Git Bash」***

   ~~~bash
   git add . && git commit -m 'first push' && git push
   ~~~

   在***「GItHub」***切换***「Hexo」***分支，可见所有网站源码已上传至仓库

---

# <center>在线编辑



---
