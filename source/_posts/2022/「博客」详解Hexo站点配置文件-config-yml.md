---
title: 「博客」详解Hexo站点配置文件_config.yml
date: 2022-07-05 19:42:53
tags:
- Hexo
- _config.yml
cover: https://s2.loli.net/2022/07/05/gMqk18cwhWtrNe5.png
categories: 博客
---




---

# <center>默认配置

- ***「_config.yml」***未修改时如下

  ~~~yaml
  # Hexo Configuration
  ## Docs: https://hexo.io/docs/configuration.html
  ## Source: https://github.com/hexojs/hexo/
  
  # Site
  title: Hexo
  subtitle: ''
  description: ''
  keywords:
  author: John Doe
  language: en
  timezone: ''
  
  # URL
  ## Set your site url here. For example, if you use GitHub Page, set url as 'https://username.github.io/project'
  url: http://example.com
  permalink: :year/:month/:day/:title/
  permalink_defaults:
  pretty_urls:
    trailing_index: true # Set to false to remove trailing 'index.html' from permalinks
    trailing_html: true # Set to false to remove trailing '.html' from permalinks
  
  # Directory
  source_dir: source
  public_dir: public
  tag_dir: tags
  archive_dir: archives
  category_dir: categories
  code_dir: downloads/code
  i18n_dir: :lang
  skip_render:
  
  # Writing
  new_post_name: :title.md # File name of new posts
  default_layout: post
  titlecase: false # Transform title into titlecase
  external_link:
    enable: true # Open external links in new tab
    field: site # Apply to the whole site
    exclude: ''
  filename_case: 0
  render_drafts: false
  post_asset_folder: false
  relative_link: false
  future: true
  highlight:
    enable: true
    line_number: true
    auto_detect: false
    tab_replace: ''
    wrap: true
    hljs: false
  prismjs:
    enable: false
    preprocess: true
    line_number: true
    tab_replace: ''
  
  # Home page setting
  # path: Root path for your blogs index page. (default = '')
  # per_page: Posts displayed per page. (0 = disable pagination)
  # order_by: Posts order. (Order by date descending by default)
  index_generator:
    path: ''
    per_page: 10
    order_by: -date
  
  # Category & Tag
  default_category: uncategorized
  category_map:
  tag_map:
  
  # Metadata elements
  ## https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta
  meta_generator: true
  
  # Date / Time format
  ## Hexo uses Moment.js to parse and display date
  ## You can customize the date format as defined in
  ## http://momentjs.com/docs/#/displaying/format/
  date_format: YYYY-MM-DD
  time_format: HH:mm:ss
  ## updated_option supports 'mtime', 'date', 'empty'
  updated_option: 'mtime'
  
  # Pagination
  ## Set per_page to 0 to disable pagination
  per_page: 10
  pagination_dir: page
  
  # Include / Exclude file(s)
  ## include:/exclude: options only apply to the 'source/' folder
  include:
  exclude:
  ignore:
  
  # Extensions
  ## Plugins: https://hexo.io/plugins/
  ## Themes: https://hexo.io/themes/
  theme: landscape
  
  # Deployment
  ## Docs: https://hexo.io/docs/one-command-deployment
  deploy:
    type: ''
  ~~~


---

# <center>完整配置

- 自定义配置如下

  {% timeline 2022 %}

  <!-- timeline 2022年07月03日 -->

  第一次配置

  <!-- endtimeline -->

  <!-- timeline 2022年07月05日 -->

  - 改默认生成文章为草稿
  - 改主页文章排版顺序为修改日期
  - 同步创建与文章同名的资源文件夹

  <!-- endtimeline -->

  {% endtimeline %}

  ~~~yaml
  # Hexo Configuration
  ## Docs: https://hexo.io/docs/configuration.html
  ## Source: https://github.com/hexojs/hexo/
  
  # Site
  title: Minge # 网站名
  subtitle: 'Blog'  # 副标题
  description: '越自律，越自由' # 描述
  keywords: # 关键词
  - 博客
  - 编程
  - 机械
  author: WangMin  # 作者
  language: 'zh-CN'  # 语言，必须加引号
  timezone: 'Asia/Shanghai'  # 时区
  
  # URL
  url: https://minge.live	# 域名
  permalink: :year/:title/  # 文章网络地址：https://域名/年份/文章名/文章名.html
  permalink_defaults:	# 永久链接中各部分的默认值
  pretty_urls:
    trailing_index: false # 设置为FALSE将从固定链接中删除尾随的‘index.html’
    trailing_html: false  # 设置为False可从固定链接中删除尾随的‘.html’
  
  # Directory---不修改
  source_dir: source  # 资源文件夹，用来存放源文件
  public_dir: public  # 存放生成的站点文件
  tag_dir: tags # 标签文件夹
  archive_dir: archives # 归档文件夹
  category_dir: categories # 分类文件夹
  code_dir: downloads/code  # Include code 文件夹
  i18n_dir: :lang # 国际化（i18n）文件夹
  skip_render:  # 跳过指定文件的渲染，可以使用glob表达式来匹配路径, 如跳过README.md的渲染
  
  # Writing
  new_post_name: :year/:title.md # 新生成文章名
  default_layout: draft  # 帖子/草稿/页面：post/draft/page，设置后，hexo n 默认生成对应属性文章
  titlecase: false # 生成文章名首字母为大写
  external_link:  # 外部链接
    enable: true # 在新选项卡中打开外部链接
    field: site # 适用于整个网站/仅适用于文章：site/post
    exclude: '' # 排除选定域名
  filename_case: 0 # 不转/转为大写/转为小写：0/1/2
  render_drafts: true  # 显示草稿
  post_asset_folder: true  # 同步创建与文章同名的资源文件夹
  relative_link: false  # 把链接改为与根目录的相对地址
  future: true  # 显示当前时间之后的文章
  highlight:  # 代码高亮
    enable: true  # 启用
    line_number: true # 显示行号
    auto_detect: false  # 自动检测语法
    tab_replace: '' # 用指定字符串替换tab键
    wrap: true	# 将代码放在table标签里
    hljs: false	# 对CSS类使用hljs-*前缀
  prismjs:
    enable: false
    preprocess: true
    line_number: true
    tab_replace: ''
  
  # Home page setting
  index_generator:  # 主页设置
    path: ''  # 博客根目录
    per_page: 0  # 每页显示的帖子，0➪禁用分页
    order_by: -date # 随机/名称/使用频率/修改时间：random/name/length/date
  
  # Category & Tag
  default_category: uncategorized # 默认分类：未分类
  category_map: # 分类别名
  tag_map:  # 标签别名
  
  # Metadata elements
  meta_generator: true  # 元数据元素
  
  # Date / Time format
  date_format: YYYY-MM-DD # 日期格式
  time_format: HH:mm:ss # 时间格式
  updated_option: 'mtime' # 更新选项： 'mtime', 'date', 'empty'
  
  # Pagination
  ## Set per_page to 0 to disable pagination
  per_page: 10
  pagination_dir: page
  
  # Include / Exclude file(s)
  include:  # 仅适用于source文件夹
  exclude:
  ignore:
  
  # Extensions
  theme: butterfly # 主题
  
  # Deployment
  deploy:
  # - type: git
  #   repo: git@github.com:wangmin-1995/wangmin-1995.github.io.git
  #   branch: main
  - type: git
    repo: https://github.com/wangmin-1995/wangmin-1995.github.io.git
    branch: main
  ~~~


---

# <center>详细解析

- 参考文章

  {% btn 'https://blog.csdn.net/qq_32767041/article/details/103283413',[Hexo 搭建个人博客（四）Hexo 站点配置_15wylu的博客-CSDN博客],far fa-hand-point-right,block outline right blue larger %}

  {% btn 'https://blog.csdn.net/zemprogram/article/details/104288872',[个人博客搭建笔记----hexo根目录下的_config.yml配置解释_前端小黑的博客-CSDN博客_config.yml],far fa-hand-point-right,block outline right blue larger %}

## <center>网站信息

- [x] ***「Site」***

  ~~~yaml
  title: Minge # 网站名
  subtitle: 'Blog'  # 副标题
  description: '越自律，越自由' # 描述
  keywords: # 关键词
  - 博客
  - 编程
  - 机械
  author: WangMin  # 作者
  language: 'zh-CN'  # 语言，必须加引号
  timezone: 'Asia/Shanghai'  # 时区
  ~~~

## <center>网络地址

- [x] ***「Url」***

  ~~~yaml
  url: https://minge.live	# 域名
  permalink: :year/:title/  # 文章网络地址：https://域名/年份/文章名/文章名.html
  # permalink: :year/:month/:day/:title/  
  permalink_defaults:	# 永久链接中各部分的默认值
  pretty_urls:
    trailing_index: false # 设置为FALSE将从固定链接中删除尾随的‘index.html’
    trailing_html: false  # 设置为False可从固定链接中删除尾随的‘.html’
  ~~~

## <center>目录

- [ ] ***「Directory」***

  ~~~yaml
  source_dir: source  # 资源文件夹，用来存放源文件
  public_dir: public  # 存放生成的站点文件
  tag_dir: tags # 标签文件夹
  archive_dir: archives # 归档文件夹
  category_dir: categories # 分类文件夹
  code_dir: downloads/code  # Include code 文件夹
  i18n_dir: :lang # 国际化（i18n）文件夹
  skip_render:  # 跳过指定文件的渲染，可以使用glob表达式来匹配路径, 如跳过README.md的渲染
  ~~~

## <center>文章

- [x] ***「Writing」***

  ~~~yaml
  new_post_name: :title.md # 新生成文章名
  default_layout: post  # 帖子/草稿/页面：post/draft/page，设置后，hexo n 默认生成对应属性文章
  titlecase: false # 生成文章名首字母为大写
  external_link:  # 外部链接
    enable: true # 在新选项卡中打开外部链接
    field: site # 适用于整个网站/仅适用于文章：site/post
    exclude: '' # 排除选定域名
  filename_case: 0 # 不转/转为大写/转为小写：0/1/2
  render_drafts: true  # 显示草稿
  post_asset_folder: false  # 同步创建与文章同名的资源文件夹
  relative_link: true  # 把链接改为与根目录的相对地址
  future: true  # 显示当前时间之后的文章
  highlight:  # 代码高亮
    enable: true  # 启用
    line_number: true # 显示行号
    auto_detect: false  # 自动检测语法
    tab_replace: '' # 用指定字符串替换tab键
    wrap: true	# 将代码放在table标签里
    hljs: false	# 对CSS类使用hljs-*前缀
  prismjs:
    enable: false
    preprocess: true
    line_number: true
    tab_replace: ''
  ~~~

### 「新文章路径」

- [ ] ***「New Post Name」***

  `hexo n 新文章`时，新文章生成的目录位置

  本地路径：`source/_posts/文章名/文章名.md`

  ~~~yaml
  new_post_name: :title/:title.md
  ~~~

  本地路径：`source/_posts/年/月/日/文章名/文章名.md`

  ~~~yaml
  new_post_name: :year/:month/:day/:title/:title.md
  ~~~

### 「草稿」

- [x] ***「Draft」***

  Hexo 的一种特殊布局：***「draft」***，这种布局在建立时会被保存到 `source/_drafts`文件夹，通过 ***「publish」***命令将草稿移动到 `source/_posts` 文件夹

  ~~~bash
  $ hexo p 文章名
  ~~~

  草稿默认不会显示在页面中，在执行时加上***「--draft」***参数，或是把***「render_drafts」***参数设为***「true」***来预览草稿。

## <center>主页设置

- [x] ***「Home Page」***

  ~~~yaml
  index_generator:  # 主页设置
    path: ''  # 博客根目录
    per_page: 5  # 每页显示的帖子，0➪禁用分页
    order_by: name # 随机/名称/使用频率/修改时间：random/name/length/date
  ~~~

## <center>分类&标签

- [ ] ***「Category & Tag」***

  ~~~yaml
  default_category: uncategorized # 默认分类：未分类
  category_map: # 分类别名
  tag_map:  # 标签别名
  ~~~

## <center>元数据元素

- [ ] ***「Metadata Elements」***

  ~~~yaml
  meta_generator: true  # 元数据元素
  ~~~

  是否在页面开头插入下面的meta标签，默认为***「true」***

  ~~~html
  <meta name="generator" content="Hexo 4.1.1"> == $0
  ~~~

## <center>时间格式

- [ ] ***「Date / Time format」***

  ~~~yaml
  # Hexo 使用 Moment.js 来解析和显示时间
  date_format: YYYY-MM-DD # 日期格式
  time_format: HH:mm:ss # 时间格式
  updated_option: 'mtime' # 更新选项： 'mtime', 'date', 'empty'
  ~~~

## <center>包含&排除&忽略

- [ ] ***「Include / Exclude / Ignore file」***

  ~~~yaml
  include:
  exclude:
  ignore:
  ~~~
  
  | 参数      | 描述                                                         |
  | :-------- | :----------------------------------------------------------- |
  | `include` | Hexo 默认会不包括 `source/` 下的文件和文件夹（包括名称以下划线和 ***「.」*** 开头的文件和文件夹，Hexo 的 ***「_posts」***和 ***「_data」*** 等目录除外）。通过设置此字段将使 Hexo 处理他们并将它们复制到 ***「source」*** 目录下。 |
  | `exclude` | Hexo 不包括 `source/` 下的这些文件和目录                     |
  | `ignore`  | Hexo 会忽略整个 Hexo 项目下的这些文件夹或文件                |

## <center>主题选用

- [x] ***「Theme」***

  ~~~yaml
  theme: butterfly # 主题
  ~~~

## <center>链接仓库

- [x] ***「Deployment」***

  ~~~yaml
  deploy:
  # - type: git
  #   repo: git@github.com:wangmin-1995/wangmin-1995.github.io.git
  #   branch: main
  - type: git
    repo: https://github.com/wangmin-1995/wangmin-1995.github.io.git
    branch: main
  ~~~

  - 两种方式都可行

    `git@github.com:用户名/用户名.github.io.git`或`https://github.com/用户名/用户名.github.io.git`

  - 可同时布署至多个仓库

# <center>疑难杂症

- ***「Site」***➪***「Language」***

  ~~~yaml
  language: 'zh-CN'  # 语言，必须加引号
  timezone: 'Asia/Shanghai'  # 时区
  ~~~

  设置中文后无效，原因是***「language」***一栏要加引号

- ***「Writing」***➪***「Relative Link」***

  ~~~yaml
  relative_link: false  # 把链接改为与根目录的相对地址
  ~~~

  设置为***「true」***会导致意想不到的***「404」***问题，原因是获取不到网页文件的正确目录

  如进入***「https://minge.live/categories/博客/」***时，再次点击导航栏的***「分类」***，打开的网址是***「https://minge.live/categories/博客/categories)」***，显然***「GitHub」***仓库中并没有这个目录，所以报错

---
