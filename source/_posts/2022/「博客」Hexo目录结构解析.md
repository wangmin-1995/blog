---
title: 「博客」Hexo目录结构解析
tags: Hexo
categories: 博客
cover: https://s2.loli.net/2022/07/05/gMqk18cwhWtrNe5.png
date: 2022-07-05 22:58:12
---





---

# <center>总结构

<img src="https://s2.loli.net/2022/07/05/HiGltkyRnspdaBe.png" style="zoom:67%;" />

---

# <center>文件夹详解

## <center>.deploy_git

- 部署到***「GitHub」***后自动创建
- 此目录中的内容 = ***「GitHub」***站点中对应***「Repository」***中的内容 = 最近一次上传到站点的***「public」***目录中的内容
- 在`hexo d`后发生错误导致没有上传到***「GitHub」***仓库时，***「.deploy_git」***内容不会更新

## <center>.git

- 用户手动创建，详见

  {% btn 'https://minge.live/2022/「博客」利用Git分支上传网站源码/',[「博客」利用Git分支上传网站源码 | Minge],far fa-hand-point-right,block outline right blue larger %}

## <center>.github

- 里面只有***「dependabot.yml」***这一个文件
- 版本相关

## <center>node_modules

***「Hexo默认扩展」***

- ***「hexo-deployer-git」***：git部署
- ***「hexo」***：主程序
- ***「hexo-generator-archive」***：存档页面生成器
- ***「hexo-generator-category」***：类别生成器
- ***「hexo-generator-index」***：index生成器
- ***「hexo-generator-tag」***：标签生成器
- ***「hexo-renderer-ejs」***：节点的嵌入式 JavaScript 模板
- ***「hexo-renderer-stylus」***：CSS 预处理器
- ***「hexo-renderer-marked」***：Markdown引擎，让你可以用markdown格式书写博客
- ***「hexo-server」***：服务器，让你可以本地预览博客

## <center>puplic

- 执行 `hexo g` 命令，Hexo程序会解析 ***「source」*** 、当前使用的主题，生成的静态网页内容目录就是 ***「public」*** ，执行 `hexo d` 则将该目录内容复制到 ***「.deploy_git」*** 目录

## <center>scaffolds

- 模板文件夹，新建文章时，***「Hexo」***会根据***「scaffold」***来建立文件

- 以下是各页面相对应的模板名称

  | 模板       | 用途     | 回退      |
  | :--------- | :------- | :-------- |
  | `index`    | 首页     |           |
  | `post`     | 文章     | `index`   |
  | `page`     | 分页     | `index`   |
  | `archive`  | 归档     | `index`   |
  | `category` | 分类归档 | `archive` |
  | `tag`      | 标签归档 | `archive` |

## <center>source

<img src="https://s2.loli.net/2022/07/05/ytrpliKdCM9v6Af.png" alt="image-20220705221410598" style="zoom:67%;" />

### 「_posts」

- 存放正式分布的文章

### 「_drafts」

- 存放草稿的目录

- 在***「_config.yml」***中设置以下两项

  ~~~yaml
  default_layout: draft
  ~~~

  ~~~yaml
  post_asset_folder: true
  ~~~

  `hexo n`时自动在***「_drafts」***生成同名文件夹，用于存放文章封面和所用到的图片，仅用于备份，在`hexo d`时不会上传此文件夹下的图片

### 「...」

- 其它以***「_」***开头的文件、文件夹不会上传到***「.deploy.git」***
- 其它非***「_」***开头的文件、文件夹为用户自定义，会被解析并发布

## <center>themes

### 「Butterfly」

<img src="https://s2.loli.net/2022/07/05/2Cuakv1QPtzRHpN.png" alt="image-20220705222755150" style="zoom:67%;" />

- `buttfly/source/img`存放***「_config.butterfly.yml」***中用到的图片，用时以此处的***「source」***为根目录，如`/img/favicon.png`

  ~~~yaml
  favicon: /img/favicon.png
  ~~~

---

# <center>文件详解

## <center>.gitignore

- 忽略以下文件的上传到***「.deploy.git」***，默认内容

  ~~~
  .DS_Store
  Thumbs.db
  db.json
  *.log
  node_modules/
  public/
  .deploy*/
  _multiconfig.yml
  ~~~

## <center>_config.yml

- 站点配置文件，详见

  {% btn 'https://minge.live/2022/「博客」详解Hexo站点配置文件-config-yml/',[「博客」详解Hexo站点配置文件-config-yml | Minge],far fa-hand-point-right,block outline right blue larger %}

## <center>_config.butterfly.yml

- 主题配置文件，详见

  {% btn 'https://minge.live/2022/「博客」详解Butterfly主题配置文件-config-butterfly-yml/',[「博客」详解Butterfly主题配置文件-config-butterfly-yml | Minge],far fa-hand-point-right,block outline right blue larger %}

