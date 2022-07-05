---
title: 「博客」Hexo+Butterfly+GitHub搭建免费个人博客
date: 2022-07-05 19:32:48
tags:
- Hexo
- Butterfly
- GitHub
cover: https://s2.loli.net/2022/07/05/SHEToUpA5NXZ3uR.png
categories: 博客
---



---

# <center>安装软件

- [x] ***「Node」***，主要用到***「Node.Js」***的包管理器***「Npm」***

  {% btn 'https://nodejs.org/en/',[Node.js (nodejs.org)],far fa-hand-point-right,block outline right blue larger %}

- [x] ***「Git」***，所有的命令都在***「Git Bash」***中进行

  {% btn 'http://git-scm.com/',[Git (git-scm.com)],far fa-hand-point-right,block outline right blue larger %}

- [ ] ***「VsCode」***，用于编辑文本，在安装**「Git」**后也可以输入**「Git Bash」**命令

---

# <center>建立仓库

## <center>创建本地仓库

### 「Hexo框架」

{% btn 'https://hexo.io/zh-cn/index.html',[Hexo],far fa-hand-point-right,block outline right blue larger %}

1. 新建本地博客目录***「博客」***

2. 右键***「博客」***➪***「Git Bash Here」***

3. ***「Npm」***安装***「Hexo」***

   ~~~bash
   npm install -g hexo-cli
   ~~~

4. 初始化***「Hexo」***

   ~~~bash
   hexo init
   ~~~

5. 实时预览插件，仅对文章有效

   ~~~bash
   npm install hexo-browsersync --save
   ~~~

6. 启动本地服务器预览

   ~~~bash
   hexo clean && hexo g && hexo s
   ~~~

### 「Butterfly主题」

{% btn 'https://butterfly.js.org/posts/21cfbf15/',[Butterfly - A Simple and Card UI Design theme for Hexo],far fa-hand-point-right,block outline right blue larger %}

1. 安装主题

   - [x] ***「Github」***安装

     ~~~bash
     git clone -b master https://github.com/jerryc127/hexo-theme-butterfly.git themes/butterfly
     ~~~

   - [ ] ***「Gitee」***安装

     ~~~bash
     git clone -b master https://gitee.com/immyw/hexo-theme-butterfly.git themes/butterfly
     ~~~

   - [ ] ***「Npm」***安装

     ~~~bash
     npm i hexo-theme-butterfly
     ~~~

2. 找到`博客\themes\butterfly`下的***「_config.yml」***，复制并重命名为***「_config.butterfly.yml」***，粘贴到***「博客」***下

3. ***「_config.yml」***修改，启用主题

   ~~~yaml
   theme: butterfly
   ~~~

4. 删除自带的***「Landscape」***主题

   - 删除***「_config.Landscape.yml」***

   - 删除***「node_modules」***下的***「hexo-theme-landscape」***文件夹

5. ***「Butterfly」***必须安装***「Pug渲染器」***插件

   ~~~bash
   npm install hexo-renderer-pug --save
   ~~~

6. 启动本地服务器预览

   ~~~bash
   hexo clean && hexo g && hexo s
   ~~~

## <center>创建远程仓库

1. 注册并登录***「GitHub」***
2. 新建一个与用户名同名的空仓库：***「用户名.gitbub.io」***
3. 点击仓库***「用户名.gitbub.io」***➪***「Settings」***➪***「Pages」***，勾选***「Enforce HTTPS」***

---

# <center>绑定仓库

1. 回到***「Git Bash」***，设置***「用户名」***和***「邮箱」***

   ~~~bash
   git config --global user.name "wangmin-1995"
   ~~~

   ~~~bash
   git config --global user.email "wangmin-1995@outlook.mail"
   ~~~

2. 创建***「SSH」***密钥，用于本地计算机和远程的连接

   ~~~bash
   ssh-keygen -t rsa -C "wangmin-1995@outlook.com"
   ~~~

   连按三个***「回车」***，设置为空密码

3. 进入`C:\Users\用户名\.ssh`目录，***「.ssh」***文件夹默认隐藏，打开它，找到***「 id_rsa.pub」***，复制里面的内容

4. 登录***「GitHub」***➪***「Setting」***➪***「SSH and GPG keys」***➪点击***「New SSH key」***➪填入复制的内容并保存

5. 回到***「Git Bash」***验证连接，至此本地电脑与***「GitHub」***绑定成功

   ~~~bash
   ssh -T git@github.com
   ~~~

6. 找到***「博客」***下的***「_config.yml」***，拖到最下面修改，至此本地仓库与***「GitHub」***绑定成功

   ~~~yaml
   deploy:
     type: git
     repo: git@github.com:wangmin-1995/wangmin-1995.github.io.git
     branch: main
   ~~~

7. 安装***「Hexo Deployer」***布署插件

   ~~~bash
   npm install hexo-deployer-git --save
   ~~~

   布署，本地网站上传到互联网

   ~~~bash
   hexo clean && hexo g && hexo d
   ~~~

---

# <center>绑定域名

- [ ] ***「GitHub」***提供的免费域名***「用户名.github.io」***

- [x] 花十几元就能买到一年的付费域名，如腾讯云

  将买到的域名如***「Minge.live」***填入一个文本文件，删除文件后缀，并重命名为**「CNAME」**放到`博客/source`下，布署完成后，打开***「用户名.github.io」***会自动跳转到***「minge.live」***，当然也可以直接打开***「https://minge.live」***

  {% btn 'https://cloud.tencent.com/',[腾讯云 - 产业智变 云启未来 (tencent.com)],far fa-hand-point-right,block outline right blue larger %}

---
