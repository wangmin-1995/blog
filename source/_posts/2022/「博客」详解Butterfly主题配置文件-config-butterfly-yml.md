---
title: 「博客」详解Butterfly主题配置文件_config.butterfly.yml
date: 2022-07-02 21:42:46
tags:
- Butterfly
- Blog
categories: 博客
cover: https://s2.loli.net/2022/06/29/cUXnq1JoafuNeOT.png
---


{% note blue 'fas fa-bullhorn' simple %}打勾的为必备选项，没打勾的为可选选项{%endnote%}

{% note blue 'fas fa-bullhorn' simple %}本篇对Butterfly主题配置文件***「_config.butterfly.yml」***详细解析{%endnote%}

---


# <center>默认配置

- ***「_config.butterfly.yml」***未修改时如下

  ~~~yaml
  # Main menu navigation (導航目錄)
  # see https://butterfly.js.org/posts/4aa8abbe/#導航菜單
  # --------------------------------------
  
  menu:
    # Home: / || fas fa-home
    # Archives: /archives/ || fas fa-archive
    # Tags: /tags/ || fas fa-tags
    # Categories: /categories/ || fas fa-folder-open
    # List||fas fa-list:
    #   Music: /music/ || fas fa-music
    #   Movie: /movies/ || fas fa-video
    # Link: /link/ || fas fa-link
    # About: /about/ || fas fa-heart
  
  # Code Blocks (代碼相關)
  # --------------------------------------
  
  highlight_theme: light #  darker / pale night / light / ocean / mac / mac light / false
  highlight_copy: true # copy button
  highlight_lang: true # show the code language
  highlight_shrink: false # true: shrink the code blocks / false: expand the code blocks | none: expand code blocks and hide the button
  highlight_height_limit: false # unit: px
  code_word_wrap: false
  
  # copy settings
  # copyright: Add the copyright information after copied content (複製的內容後面加上版權信息)
  copy:
    enable: true
    copyright:
      enable: false
      limit_count: 50
  
  # social settings (社交圖標設置)
  # formal:
  #   icon: link || the description
  social:
    # fab fa-github: https://github.com/xxxxx || Github
    # fas fa-envelope: mailto:xxxxxx@gmail.com || Email
  
  # search (搜索)
  # see https://butterfly.js.org/posts/ceeb73f/#搜索系統
  # --------------------------------------
  
  # Algolia search
  algolia_search:
    enable: false
    hits:
      per_page: 6
  
  # Local search
  local_search:
    enable: false
    preload: false
    CDN:
  
  # Math (數學)
  # --------------------------------------
  # About the per_page
  # if you set it to true, it will load mathjax/katex script in each page (true 表示每一頁都加載js)
  # if you set it to false, it will load mathjax/katex script according to your setting (add the 'mathjax: true' in page's front-matter)
  # (false 需要時加載，須在使用的 Markdown Front-matter 加上 mathjax: true)
  
  # MathJax
  mathjax:
    enable: false
    per_page: false
  
  # KaTeX
  katex:
    enable: false
    per_page: false
    hide_scrollbar: true
  
  # Image (圖片設置)
  # --------------------------------------
  
  # Favicon（網站圖標）
  favicon: /img/favicon.png
  
  # Avatar (頭像)
  avatar:
    img: https://i.loli.net/2021/02/24/5O1day2nriDzjSu.png
    effect: false
  
  # Disable all banner image
  disable_top_img: false
  
  # The banner image of home page
  index_img:
  
  # If the banner of page not setting, it will show the top_img
  default_top_img:
  
  # The banner image of archive page
  archive_img:
  
  # If the banner of tag page not setting, it will show the top_img
  # note: tag page, not tags page (子標籤頁面的 top_img)
  tag_img:
  
  # The banner image of tag page
  # format:
  #  - tag name: xxxxx
  tag_per_img:
  
  # If the banner of category page not setting, it will show the top_img
  # note: category page, not categories page (子分類頁面的 top_img)
  category_img:
  
  # The banner image of category page
  # format:
  #  - category name: xxxxx
  category_per_img:
  
  cover:
    # display the cover or not (是否顯示文章封面)
    index_enable: true
    aside_enable: true
    archives_enable: true
    # the position of cover in home page (封面顯示的位置)
    # left/right/both
    position: both
    # When cover is not set, the default cover is displayed (當沒有設置cover時，默認的封面顯示)
    default_cover:
      # - https://i.loli.net/2020/05/01/gkihqEjXxJ5UZ1C.jpg
  
  # Replace Broken Images (替換無法顯示的圖片)
  error_img:
    flink: /img/friend_404.gif
    post_page: /img/404.jpg
  
  # A simple 404 page
  error_404:
    enable: false
    subtitle: 'Page Not Found'
    background: https://i.loli.net/2020/05/19/aKOcLiyPl2JQdFD.png
  
  post_meta:
    page: # Home Page
      date_type: created # created or updated or both 主頁文章日期是創建日或者更新日或都顯示
      date_format: date # date/relative 顯示日期還是相對日期
      categories: true # true or false 主頁是否顯示分類
      tags: false # true or false 主頁是否顯示標籤
      label: true # true or false 顯示描述性文字
    post:
      date_type: both # created or updated or both 文章頁日期是創建日或者更新日或都顯示
      date_format: date # date/relative 顯示日期還是相對日期
      categories: true # true or false 文章頁是否顯示分類
      tags: true # true or false 文章頁是否顯示標籤
      label: true # true or false 顯示描述性文字
  
  # wordcount (字數統計)
  # see https://butterfly.js.org/posts/ceeb73f/#字數統計
  wordcount:
    enable: false
    post_wordcount: true
    min2read: true
    total_wordcount: true
  
  # Display the article introduction on homepage
  # 1: description
  # 2: both (if the description exists, it will show description, or show the auto_excerpt)
  # 3: auto_excerpt (default)
  # false: do not show the article introduction
  index_post_content:
    method: 3
    length: 500 # if you set method to 2 or 3, the length need to config
  
  # anchor
  # when you scroll in post, the URL will update according to header id.
  anchor: false
  
  # Post
  # --------------------------------------
  
  # toc (目錄)
  toc:
    post: true
    page: false
    number: true
    expand: false
    style_simple: false # for post
  
  post_copyright:
    enable: true
    decode: false
    author_href:
    license: CC BY-NC-SA 4.0
    license_url: https://creativecommons.org/licenses/by-nc-sa/4.0/
  
  # Sponsor/reward
  reward:
    enable: false
    QR_code:
      # - img: /img/wechat.jpg
      #   link:
      #   text: wechat
      # - img: /img/alipay.jpg
      #   link:
      #   text: alipay
  
  # Post edit
  # Easily browse and edit blog source code online.
  post_edit:
    enable: false
    # url: https://github.com/user-name/repo-name/edit/branch-name/subdirectory-name/
    # For example: https://github.com/jerryc127/butterfly.js.org/edit/main/source/
    url:
  
  # Related Articles
  related_post:
    enable: true
    limit: 6 # Number of posts displayed
    date_type: created # or created or updated 文章日期顯示創建日或者更新日
  
  # figcaption (圖片描述文字)
  photofigcaption: false
  
  # post_pagination (分頁)
  # value: 1 || 2 || false
  # 1: The 'next post' will link to old post
  # 2: The 'next post' will link to new post
  # false: disable pagination
  post_pagination: 1
  
  # Displays outdated notice for a post (文章過期提醒)
  noticeOutdate:
    enable: false
    style: flat # style: simple/flat
    limit_day: 500 # When will it be shown
    position: top # position: top/bottom
    message_prev: It has been
    message_next: days since the last update, the content of the article may be outdated.
  
  # Share System (分享功能)
  # --------------------------------------
  
  # AddThis
  # https://www.addthis.com/
  addThis:
    enable: false
    pubid:
  
  # Share.js
  # https://github.com/overtrue/share.js
  sharejs:
    enable: true
    sites: facebook,twitter,wechat,weibo,qq
  
  # AddToAny
  # https://www.addtoany.com/
  addtoany:
    enable: false
    item: facebook,twitter,wechat,sina_weibo,facebook_messenger,email,copy_link
  
  # Comments System
  # --------------------------------------
  
  comments:
    # Up to two comments system, the first will be shown as default
    # Choose: Disqus/Disqusjs/Livere/Gitalk/Valine/Waline/Utterances/Facebook Comments/Twikoo/Giscus/Remark42
    use: # Valine,Disqus
    text: true # Display the comment name next to the button
    # lazyload: The comment system will be load when comment element enters the browser's viewport.
    # If you set it to true, the comment count will be invalid
    lazyload: false
    count: false # Display comment count in post's top_img
    card_post_count: false # Display comment count in Home Page
  
  # disqus
  # https://disqus.com/
  disqus:
    shortname:
    apikey: # For newest comments widget
  
  # Alternative Disqus - Render comments with Disqus API
  # DisqusJS 評論系統，可以實現在網路審查地區載入 Disqus 評論列表，兼容原版
  # https://github.com/SukkaW/DisqusJS
  disqusjs:
    shortname:
    apikey:
    option:
  
  # livere (來必力)
  # https://www.livere.com/
  livere:
    uid:
  
  # gitalk
  # https://github.com/gitalk/gitalk
  gitalk:
    client_id:
    client_secret:
    repo:
    owner:
    admin:
    option:
  
  # valine
  # https://valine.js.org
  valine:
    appId: # leancloud application app id
    appKey: # leancloud application app key
    avatar: monsterid # gravatar style https://valine.js.org/#/avatar
    serverURLs: # This configuration is suitable for domestic custom domain name users, overseas version will be automatically detected (no need to manually fill in)
    bg: # valine background
    visitor: false
    option:
  
  # waline - A simple comment system with backend support fork from Valine
  # https://waline.js.org/
  waline:
    serverURL: # Waline server address url
    bg: # waline background
    pageview: false
    option:
  
  # utterances
  # https://utteranc.es/
  utterances:
    repo:
    # Issue Mapping: pathname/url/title/og:title
    issue_term: pathname
    # Theme: github-light/github-dark/github-dark-orange/icy-dark/dark-blue/photon-dark
    light_theme: github-light
    dark_theme: photon-dark
  
  # Facebook Comments Plugin
  # https://developers.facebook.com/docs/plugins/comments/
  facebook_comments:
    app_id:
    user_id: # optional
    pageSize: 10 # The number of comments to show
    order_by: social # social/time/reverse_time
    lang: en_US # Language en_US/zh_CN/zh_TW and so on
  
  # Twikoo
  # https://github.com/imaegoo/twikoo
  twikoo:
    envId:
    region:
    visitor: false
    option:
  
  # Giscus
  # https://giscus.app/
  giscus:
    repo:
    repo_id:
    category_id:
    theme:
      light: light
      dark: dark
    option:
  
  # Remark42
  # https://remark42.com/docs/configuration/frontend/
  remark42:
    host: # Your Host URL
    siteId: # Your Site ID
    option:
  
  # Chat Services
  # --------------------------------------
  
  # Chat Button [recommend]
  # It will create a button in the bottom right corner of website, and hide the origin button
  chat_btn: false
  
  # The origin chat button is displayed when scrolling up, and the button is hidden when scrolling down
  chat_hide_show: false
  
  # chatra
  # https://chatra.io/
  chatra:
    enable: false
    id:
  
  # tidio
  # https://www.tidio.com/
  tidio:
    enable: false
    public_key:
  
  # daovoice
  # http://daovoice.io/
  daovoice:
    enable: false
    app_id:
  
  # gitter
  # https://gitter.im/
  gitter:
    enable: false
    room:
  
  # crisp
  # https://crisp.chat/en/
  crisp:
    enable: false
    website_id:
  
  # Footer Settings
  # --------------------------------------
  footer:
    owner:
      enable: true
      since: 2020
    custom_text:
    copyright: true # Copyright of theme and framework
  
  # Analysis
  # --------------------------------------
  
  # Baidu Analytics
  # https://tongji.baidu.com/web/welcome/login
  baidu_analytics:
  
  # Google Analytics
  # https://analytics.google.com/analytics/web/
  google_analytics:
  
  # CNZZ Analytics
  # https://www.umeng.com/
  cnzz_analytics:
  
  # Cloudflare Analytics
  # https://www.cloudflare.com/zh-tw/web-analytics/
  cloudflare_analytics:
  
  # Microsoft Clarity
  # https://clarity.microsoft.com/
  microsoft_clarity:
  
  # Advertisement
  # --------------------------------------
  
  # Google Adsense (谷歌廣告)
  google_adsense:
    enable: false
    auto_ads: true
    js: https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js
    client:
    enable_page_level_ads: true
  
  # Insert ads manually (手動插入廣告)
  # ad:
  #   index:
  #   aside:
  #   post:
  
  # Verification (站長驗證)
  # --------------------------------------
  
  site_verification:
    # - name: google-site-verification
    #   content: xxxxxx
    # - name: baidu-site-verification
    #   content: xxxxxxx
  
  # Beautify/Effect (美化/效果)
  # --------------------------------------
  
  # Theme color for customize
  # Notice: color value must in double quotes like "#000" or may cause error!
  
  # theme_color:
  #   enable: true
  #   main: "#49B1F5"
  #   paginator: "#00c4b6"
  #   button_hover: "#FF7242"
  #   text_selection: "#00c4b6"
  #   link_color: "#99a9bf"
  #   meta_color: "#858585"
  #   hr_color: "#A4D8FA"
  #   code_foreground: "#F47466"
  #   code_background: "rgba(27, 31, 35, .05)"
  #   toc_color: "#00c4b6"
  #   blockquote_padding_color: "#49b1f5"
  #   blockquote_background_color: "#49b1f5"
  #   scrollbar_color: "#49b1f5"
  #   meta_theme_color_light: "ffffff"
  #   meta_theme_color_dark: "#0d0d0d"
  
  # The top_img settings of home page
  # default: top img - full screen, site info - middle (默認top_img全屏，site_info在中間)
  # The position of site info, eg: 300px/300em/300rem/10% (主頁標題距離頂部距離)
  index_site_info_top:
  # The height of top_img, eg: 300px/300em/300rem (主頁top_img高度)
  index_top_img_height:
  
  # The user interface setting of category and tag page (category和tag頁的UI設置)
  # index - same as Homepage UI (index 值代表 UI將與首頁的UI一樣)
  # default - same as archives UI 默認跟archives頁面UI一樣
  category_ui: # 留空或 index
  tag_ui: # 留空或 index
  
  # Website Background (設置網站背景)
  # can set it to color or image (可設置圖片 或者 顔色)
  # The formal of image: url(http://xxxxxx.com/xxx.jpg)
  background:
  
  # Footer Background
  footer_bg: false
  
  # the position of bottom right button/default unit: px (右下角按鈕距離底部的距離/默認單位為px)
  rightside-bottom:
  
  # Enter transitions (開啓網頁進入效果)
  enter_transitions: true
  
  # Background effects (背景特效)
  # --------------------------------------
  
  # canvas_ribbon (靜止彩帶背景)
  # See: https://github.com/hustcc/ribbon.js
  canvas_ribbon:
    enable: false
    size: 150
    alpha: 0.6
    zIndex: -1
    click_to_change: false
    mobile: false
  
  # Fluttering Ribbon (動態彩帶)
  canvas_fluttering_ribbon:
    enable: false
    mobile: false
  
  # canvas_nest
  # https://github.com/hustcc/canvas-nest.js
  canvas_nest:
    enable: false
    color: '0,0,255' #color of lines, default: '0,0,0'; RGB values: (R,G,B).(note: use ',' to separate.)
    opacity: 0.7 # the opacity of line (0~1), default: 0.5.
    zIndex: -1 # z-index property of the background, default: -1.
    count: 99 # the number of lines, default: 99.
    mobile: false
  
  # Typewriter Effect (打字效果)
  # https://github.com/disjukr/activate-power-mode
  activate_power_mode:
    enable: false
    colorful: true # open particle animation (冒光特效)
    shake: true #  open shake (抖動特效)
    mobile: false
  
  # Mouse click effects: fireworks (鼠標點擊效果: 煙火特效)
  fireworks:
    enable: false
    zIndex: 9999 # -1 or 9999
    mobile: false
  
  # Mouse click effects: Heart symbol (鼠標點擊效果: 愛心)
  click_heart:
    enable: false
    mobile: false
  
  # Mouse click effects: words (鼠標點擊效果: 文字)
  ClickShowText:
    enable: false
    text:
      # - I
      # - LOVE
      # - YOU
    fontSize: 15px
    random: false
    mobile: false
  
  # Default display mode (網站默認的顯示模式)
  # light (default) / dark
  display_mode: light
  
  # Beautify (美化頁面顯示)
  beautify:
    enable: false
    field: post # site/post
    title-prefix-icon: # '\f0c1'
    title-prefix-icon-color: # '#F47466'
  
  # Global font settings
  # Don't modify the following settings unless you know how they work (非必要不要修改)
  font:
    global-font-size:
    code-font-size:
    font-family:
    code-font-family:
  
  # Font settings for the site title and site subtitle
  # 左上角網站名字 主頁居中網站名字
  blog_title_font:
    font_link:
    font-family:
  
  # The setting of divider icon (水平分隔線圖標設置)
  hr_icon:
    enable: true
    icon: # the unicode value of Font Awesome icon, such as '\3423'
    icon-top:
  
  # the subtitle on homepage (主頁subtitle)
  subtitle:
    enable: false
    # Typewriter Effect (打字效果)
    effect: true
    # loop (循環打字)
    loop: true
    # source 調用第三方服務
    # source: false 關閉調用
    # source: 1  調用一言網的一句話（簡體） https://hitokoto.cn/
    # source: 2  調用一句網（簡體） http://yijuzhan.com/
    # source: 3  調用今日詩詞（簡體） https://www.jinrishici.com/
    # subtitle 會先顯示 source , 再顯示 sub 的內容
    source: false
    # 如果關閉打字效果，subtitle 只會顯示 sub 的第一行文字
    sub:
  
  # Loading Animation (加載動畫)
  preloader: false
  
  # aside (側邊欄)
  # --------------------------------------
  
  aside:
    enable: true
    hide: false
    button: true
    mobile: true # display on mobile
    position: right # left or right
    display:
      archive: true
      tag: true
      category: true
    card_author:
      enable: true
      description:
      button:
        enable: true
        icon: fab fa-github
        text: Follow Me
        link: https://github.com/xxxxxx
    card_announcement:
      enable: true
      content: This is my Blog
    card_recent_post:
      enable: true
      limit: 5 # if set 0 will show all
      sort: date # date or updated
      sort_order: # Don't modify the setting unless you know how it works
    card_categories:
      enable: true
      limit: 8 # if set 0 will show all
      expand: none # none/true/false
      sort_order: # Don't modify the setting unless you know how it works
    card_tags:
      enable: true
      limit: 40 # if set 0 will show all
      color: false
      sort_order: # Don't modify the setting unless you know how it works
    card_archives:
      enable: true
      type: monthly # yearly or monthly
      format: MMMM YYYY # eg: YYYY年MM月
      order: -1 # Sort of order. 1, asc for ascending; -1, desc for descending
      limit: 8 # if set 0 will show all
      sort_order: # Don't modify the setting unless you know how it works
    card_webinfo:
      enable: true
      post_count: true
      last_push_date: true
      sort_order: # Don't modify the setting unless you know how it works
  
  # busuanzi count for PV / UV in site
  # 訪問人數
  busuanzi:
    site_uv: true
    site_pv: true
    page_pv: true
  
  # Time difference between publish date and now (網頁運行時間)
  # Formal: Month/Day/Year Time or Year/Month/Day Time
  runtimeshow:
    enable: false
    publish_date:
  
  # Aside widget - Newest Comments
  newest_comments:
    enable: false
    sort_order: # Don't modify the setting unless you know how it works
    limit: 6
    storage: 10 # unit: mins, save data to localStorage
    avatar: true
  
  # Bottom right button (右下角按鈕)
  # --------------------------------------
  
  # Conversion between Traditional and Simplified Chinese (簡繁轉換)
  translate:
    enable: false
    # The text of a button
    default: 繁
    # the language of website (1 - Traditional Chinese/ 2 - Simplified Chinese）
    defaultEncoding: 2
    # Time delay
    translateDelay: 0
    # The text of the button when the language is Simplified Chinese
    msgToTraditionalChinese: '繁'
    # The text of the button when the language is Traditional Chinese
    msgToSimplifiedChinese: '簡'
  
  # Read Mode (閲讀模式)
  readmode: true
  
  # dark mode
  darkmode:
    enable: true
    # Toggle Button to switch dark/light mode
    button: true
    # Switch dark/light mode automatically (自動切換 dark mode和 light mode)
    # autoChangeMode: 1  Following System Settings, if the system doesn't support dark mode, it will switch dark mode between 6 pm to 6 am
    # autoChangeMode: 2  Switch dark mode between 6 pm to 6 am
    # autoChangeMode: false
    autoChangeMode: false
  
  # Don't modify the following settings unless you know how they work (非必要請不要修改 )
  # Choose: readmode,translate,darkmode,hideAside,toc,chat,comment
  # Don't repeat 不要重複
  rightside_item_order:
    enable: false
    hide: # readmode,translate,darkmode,hideAside
    show: # toc,chat,comment
  
  # Lightbox (圖片大圖查看模式)
  # --------------------------------------
  # You can only choose one, or neither (只能選擇一個 或者 兩個都不選)
  
  # medium-zoom
  # https://github.com/francoischalifour/medium-zoom
  medium_zoom: false
  
  # fancybox
  # http://fancyapps.com/fancybox/3/
  fancybox: true
  
  # Tag Plugins settings (標籤外掛)
  # --------------------------------------
  
  # mermaid
  # see https://github.com/mermaid-js/mermaid
  mermaid:
    enable: false
    # built-in themes: default/forest/dark/neutral
    theme:
      light: default
      dark: dark
  
  # Note (Bootstrap Callout)
  note:
    # Note tag style values:
    #  - simple    bs-callout old alert style. Default.
    #  - modern    bs-callout new (v2-v3) alert style.
    #  - flat      flat callout style with background, like on Mozilla or StackOverflow.
    #  - disabled  disable all CSS styles import of note tag.
    style: flat
    icons: true
    border_radius: 3
    # Offset lighter of background in % for modern and flat styles (modern: -12 | 12; flat: -18 | 6).
    # Offset also applied to label tag variables. This option can work with disabled note tag.
    light_bg_offset: 0
  
  # other
  # --------------------------------------
  
  # Pjax
  # It may contain bugs and unstable, give feedback when you find the bugs.
  # https://github.com/MoOx/pjax
  pjax:
    enable: false
    exclude:
      # - xxxx
      # - xxxx
  
  # Inject the css and script (aplayer/meting)
  aplayerInject:
    enable: false
    per_page: true
  
  # Snackbar (Toast Notification 彈窗)
  # https://github.com/polonel/SnackBar
  # position 彈窗位置
  # 可選 top-left / top-center / top-right / bottom-left / bottom-center / bottom-right
  snackbar:
    enable: false
    position: bottom-left
    bg_light: '#49b1f5' # The background color of Toast Notification in light mode
    bg_dark: '#1f1f1f' # The background color of Toast Notification in dark mode
  
  # https://instant.page/
  # prefetch (預加載)
  instantpage: false
  
  # https://github.com/vinta/pangu.js
  # Insert a space between Chinese character and English character (中英文之間添加空格)
  pangu:
    enable: false
    field: site # site/post
  
  # Lazyload (圖片懶加載)
  # https://github.com/verlok/vanilla-lazyload
  lazyload:
    enable: false
    field: site # site/post
    placeholder:
    blur: false
  
  # PWA
  # See https://github.com/JLHwung/hexo-offline
  # ---------------
  # pwa:
  #   enable: false
  #   manifest: /pwa/manifest.json
  #   apple_touch_icon: /pwa/apple-touch-icon.png
  #   favicon_32_32: /pwa/32.png
  #   favicon_16_16: /pwa/16.png
  #   mask_icon: /pwa/safari-pinned-tab.svg
  
  # Open graph meta tags
  # https://developers.facebook.com/docs/sharing/webmasters/
  Open_Graph_meta: true
  
  # Add the vendor prefixes to ensure compatibility
  css_prefix: true
  
  # Inject
  # Insert the code to head (before '</head>' tag) and the bottom (before '</body>' tag)
  # 插入代码到头部 </head> 之前 和 底部 </body> 之前
  inject:
    head:
      # - <link rel="stylesheet" href="/xxx.css">
    bottom:
      # - <script src="xxxx"></script>
  
  # CDN
  # Don't modify the following settings unless you know how they work
  # 非必要請不要修改
  CDN:
    # The CDN provider of internal scripts (主題內部 js 的 cdn 配置)
    # option: local/jsdelivr/unpkg/cdnjs/custom
    # Dev version can only choose. ( dev版的主題只能設置為 local )
    internal_provider: local
  
    # The CDN provider of third party scripts (第三方 js 的 cdn 配置)
    # option: local/jsdelivr/unpkg/cdnjs/custom
    # when set it to local, you need to install hexo-butterfly-extjs
    third_party_provider: jsdelivr
  
    # Add version number to CDN, true or false  
    version: false
  
    # Custom format
    # For example: https://cdn.staticfile.org/${cdnjs_name}/${version}/${min_cdnjs_file}
    custom_format:
  
    option:
      # main_css:
      # main:
      # utils:
      # translate:
      # local_search:
      # algolia_js:
      # algolia_search_v4:
      # instantsearch_v4:
      # pjax:
      # gitalk:
      # gitalk_css:
      # blueimp_md5:
      # valine:
      # disqusjs:
      # disqusjs_css:
      # twikoo:
      # waline_js:
      # waline_css:
      # sharejs:
      # sharejs_css:
      # mathjax:
      # katex:
      # katex_copytex:
      # mermaid:
      # canvas_ribbon:
      # canvas_fluttering_ribbon:
      # canvas_nest:
      # lazyload:
      # instantpage:
      # typed:
      # pangu:
      # fancybox_css_v4:
      # fancybox_v4:
      # medium_zoom:
      # snackbar_css:
      # snackbar:
      # activate_power_mode:
      # fireworks:
      # click_heart:
      # ClickShowText:
      # fontawesomeV6:
      # flickr_justified_gallery_js:
      # flickr_justified_gallery_css:
      # aplayer_css:
      # aplayer_js:
      # meting_js:
      # prismjs_js:
      # prismjs_lineNumber_js:
      # prismjs_autoloader:
  ~~~

# <center>完整配置

- 自定义配置如下

  更新时间：***「2022/07/03」***

  ~~~Yaml
  # 导航目录
  menu:
    主页: / || fas fa-home
    归档: /archives/ || fas fa-archive
    标签: /tags/ || fas fa-tags
    分类: /categories/ || fas fa-folder-open
    收藏||fas fa-list:
      音乐: /music/ || fas fa-music
      视频: /movies/ || fas fa-video
    友链: /link/ || fas fa-link
    关于: /about/ || fas fa-heart
  
  # 代码框
  highlight_theme: light # 代码框样式
  highlight_copy: true # 复制按钮
  highlight_lang: true # 显示代码语法
  highlight_shrink: false  # 收缩代码块/展开代码块/展开代码块并隐藏按钮：true/false/none 
  highlight_height_limit: 200 # 代码框高度限制 unit: px
  code_word_wrap: false # 文本换行
  
  # 复制
  copy:
    enable: true
    copyright:	# 复制的后面加版权信息
      enable: false
      limit_count: 50
  
  # 社交&图标
  social:
    fab fa-github: https://github.com/wangmin-1995 || Github
    fas fa-envelope: mailto:wangmin-1995@outlook.com || Email
  
  # 站内搜索
  
  # Algolia search
  algolia_search:
    enable: false
    hits:
      per_page: 6
  
  # Local search
  local_search:
    enable: true
    preload: false	# 预装
    CDN:
  
  # Math (數學)---不修改
  # --------------------------------------
  # About the per_page
  # if you set it to true, it will load mathjax/katex script in each page (true 表示每一頁都加載js)
  # if you set it to false, it will load mathjax/katex script according to your setting (add the 'mathjax: true' in page's front-matter)
  # (false 需要時加載，須在使用的 Markdown Front-matter 加上 mathjax: true)
  
  # MathJax
  mathjax:
    enable: false
    per_page: false
  
  # KaTeX
  katex:
    enable: false
    per_page: false
    hide_scrollbar: true
  
  # 图标&图片
  
  # 网站图标
  favicon: /img/favicon.png
  
  # 头像
  avatar:
    img: https://s2.loli.net/2022/06/26/GB9iaNPwlk4U1ho.jpg
    effect: false	# true：头像会一直转
  
  # Disable all banner image
  disable_top_img: false
  
  # The banner image of home page
  index_img:
  
  # 默认的top_img，当页面的top_img没有配置时，会显示default_top_img
  default_top_img: https://s2.loli.net/2022/05/06/MF6cDtkeNGTZbE1.jpg
  
  # The banner image of archive page
  archive_img:
  
  # If the banner of tag page not setting, it will show the top_img
  # note: tag page, not tags page (子標籤頁面的 top_img)
  tag_img:
  
  # The banner image of tag page
  # format:
  #  - tag name: xxxxx
  tag_per_img:
  
  # If the banner of category page not setting, it will show the top_img
  # note: category page, not categories page (子分類頁面的 top_img)
  category_img:
  
  # The banner image of category page
  # format:
  #  - category name: xxxxx
  category_per_img:
  
  cover:
    index_enable: true  # 是否显示文章封面
    aside_enable: true
    archives_enable: true
    position: both  # 封面显示的位置：left/right/both
    default_cover:	# 没有设置Front_matter时，默认显示的封面，可设置多个
      - https://s2.loli.net/2022/05/06/MF6cDtkeNGTZbE1.jpg
  
  # Replace Broken Images (替換無法顯示的圖片)
  error_img:
    flink: /img/friend_404.gif
    post_page: /img/404.jpg
  
  # A simple 404 page
  error_404:
    enable: false
    subtitle: 'Page Not Found'
    background: https://i.loli.net/2020/05/19/aKOcLiyPl2JQdFD.png
  
  # 主页封面信息
  post_meta:
    page: # 主页
      date_type: both
      # 主页文章日期是创建日/更新日/都显示：created/updated/both
      date_format: date # 日期/相对日期：date/relative
      categories: true # 主页是否显示分类：true/false
      tags: true # 主页是否显示标签
      label: true # 主页是否显示描述
    post:	# 文章
      date_type: both # created/updated/both
      date_format: date # date/relative
      categories: true # true/false
      tags: true
      label: true
  
  # 字数统计
  wordcount:
    enable: true
    post_wordcount: true
    min2read: true
    total_wordcount: true
  
  # 文章摘录
  index_post_content:
    method: 1	# 仅描述/优先描述/自动节选/不显示：1/2/3/false
    length: 500	# 节选范围
  
  # 文章锚点
  anchor: true	# 阅读文章时上下拖动，地址栏会根据当前位置的标题而变化
  
  # 目录
  toc:
    post: true	# 在文章中显示
    page: false	# 不在标签、分类等页面中显示
    number: true	# 小标题加序号
    expand: true	# 一直展开
    style_simple: false # 侧边栏只显示目录，仅对文章页有效
  
  # 版权信息
  post_copyright:	
    enable: true	# 文章底部的版权信息框
    decode: true	# 显示中文网址
    author_href:
    license: CC BY-NC-SA 4.0
    license_url: https://creativecommons.org/licenses/by-nc-sa/4.0/
  
  # 捐助
  reward:
    enable: true
    QR_code:
      - img: /img/wechat.jpg
        link:
        text: wechat
      - img: /img/alipay.jpg
        link:
        text: alipay
  
  # 在线编辑
  post_edit:
    enable: false
    # For example: https://github.com/jerryc127/butterfly.js.org/edit/main/source/
    # 需要将本地仓库上传到Github仓库
    url:
  
  # 相似文章
  related_post:
    enable: true
    limit: 6 # 显示文章的数量
    date_type: created # 创建日/更新日：created/updated
  
  # 图片描述文字
  photofigcaption: false
  
  # 底部分页
  post_pagination: 2  # 下篇为旧文/下篇为新文/关闭：1/2/false
  
  # 文章过期提醒
  noticeOutdate:
    enable: false
    style: flat # 样式: simple/flat
    limit_day: 500 # 期限天数
    position: top # 位置: top/bottom
    message_prev: It has been
    message_next: days since the last update, the content of the article may be outdated.
  
  # Share System (分享功能)
  # --------------------------------------
  
  # AddThis
  # https://www.addthis.com/
  addThis:
    enable: false
    pubid:
  
  # Share.js
  # https://github.com/overtrue/share.js
  sharejs:
    enable: true
    sites: facebook,twitter,wechat,weibo,qq
  
  # AddToAny
  # https://www.addtoany.com/
  addtoany:
    enable: false
    item: facebook,twitter,wechat,sina_weibo,facebook_messenger,email,copy_link
  
  # Comments System
  # --------------------------------------
  
  comments:
    # Up to two comments system, the first will be shown as default
    # Choose: Disqus/Disqusjs/Livere/Gitalk/Valine/Waline/Utterances/Facebook Comments/Twikoo/Giscus/Remark42
    use: # Valine,Disqus
    text: true # Display the comment name next to the button
    # lazyload: The comment system will be load when comment element enters the browser's viewport.
    # If you set it to true, the comment count will be invalid
    lazyload: false
    count: false # Display comment count in post's top_img
    card_post_count: false # Display comment count in Home Page
  
  # disqus
  # https://disqus.com/
  disqus:
    shortname:
    apikey: # For newest comments widget
  
  # Alternative Disqus - Render comments with Disqus API
  # DisqusJS 評論系統，可以實現在網路審查地區載入 Disqus 評論列表，兼容原版
  # https://github.com/SukkaW/DisqusJS
  disqusjs:
    shortname:
    apikey:
    option:
  
  # livere (來必力)
  # https://www.livere.com/
  livere:
    uid:
  
  # gitalk
  # https://github.com/gitalk/gitalk
  gitalk:
    client_id:
    client_secret:
    repo:
    owner:
    admin:
    option:
  
  # valine
  # https://valine.js.org
  valine:
    appId: # leancloud application app id
    appKey: # leancloud application app key
    avatar: monsterid # gravatar style https://valine.js.org/#/avatar
    serverURLs: # This configuration is suitable for domestic custom domain name users, overseas version will be automatically detected (no need to manually fill in)
    bg: # valine background
    visitor: false
    option:
  
  # waline - A simple comment system with backend support fork from Valine
  # https://waline.js.org/
  waline:
    serverURL: # Waline server address url
    bg: # waline background
    pageview: false
    option:
  
  # utterances
  # https://utteranc.es/
  utterances:
    repo:
    # Issue Mapping: pathname/url/title/og:title
    issue_term: pathname
    # Theme: github-light/github-dark/github-dark-orange/icy-dark/dark-blue/photon-dark
    light_theme: github-light
    dark_theme: photon-dark
  
  # Facebook Comments Plugin
  # https://developers.facebook.com/docs/plugins/comments/
  facebook_comments:
    app_id:
    user_id: # optional
    pageSize: 10 # The number of comments to show
    order_by: social # social/time/reverse_time
    lang: en_US # Language en_US/zh_CN/zh_TW and so on
  
  # Twikoo
  # https://github.com/imaegoo/twikoo
  twikoo:
    envId:
    region:
    visitor: false
    option:
  
  # Giscus
  # https://giscus.app/
  giscus:
    repo:
    repo_id:
    category_id:
    theme:
      light: light
      dark: dark
    option:
  
  # Remark42
  # https://remark42.com/docs/configuration/frontend/
  remark42:
    host: # Your Host URL
    siteId: # Your Site ID
    option:
  
  # Chat Services
  # --------------------------------------
  
  # Chat Button [recommend]
  # It will create a button in the bottom right corner of website, and hide the origin button
  chat_btn: false
  
  # The origin chat button is displayed when scrolling up, and the button is hidden when scrolling down
  chat_hide_show: false
  
  # chatra
  # https://chatra.io/
  chatra:
    enable: false
    id:
  
  # tidio
  # https://www.tidio.com/
  tidio:
    enable: false
    public_key:
  
  # daovoice
  # http://daovoice.io/
  daovoice:
    enable: false
    app_id:
  
  # gitter
  # https://gitter.im/
  gitter:
    enable: false
    room:
  
  # crisp
  # https://crisp.chat/en/
  crisp:
    enable: false
    website_id:
  
  # 页脚
  footer:
    owner:
      enable: true
      since: 2022
    custom_text:
    copyright: true # 主题和框架的著作权
  
  # Analysis
  # --------------------------------------
  
  # Baidu Analytics
  # https://tongji.baidu.com/web/welcome/login
  baidu_analytics:
  
  # Google Analytics
  # https://analytics.google.com/analytics/web/
  google_analytics:
  
  # CNZZ Analytics
  # https://www.umeng.com/
  cnzz_analytics:
  
  # Cloudflare Analytics
  # https://www.cloudflare.com/zh-tw/web-analytics/
  cloudflare_analytics:
  
  # Microsoft Clarity
  # https://clarity.microsoft.com/
  microsoft_clarity:
  
  # Advertisement
  # --------------------------------------
  
  # Google Adsense (谷歌廣告)
  google_adsense:
    enable: false
    auto_ads: true
    js: https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js
    client:
    enable_page_level_ads: true
  
  # Insert ads manually (手動插入廣告)
  # ad:
  #   index:
  #   aside:
  #   post:
  
  # Verification (站長驗證)
  # --------------------------------------
  
  site_verification:
    # - name: google-site-verification
    #   content: xxxxxx
    # - name: baidu-site-verification
    #   content: xxxxxxx
  
  # Beautify/Effect (美化/效果)
  # --------------------------------------
  
  # Theme color for customize
  # Notice: color value must in double quotes like "#000" or may cause error!
  
  theme_color:
    enable: true
    main: "#778899"
    paginator: "#00c4b6"
    button_hover: "#FF7242"
    text_selection: "#00c4b6"
    link_color: "#99a9bf"
    meta_color: "#858585"
    hr_color: "#A4D8FA"
    code_foreground: "#F47466"
    code_background: "rgba(27, 31, 35, .05)"
    toc_color: "#00c4b6"
    blockquote_padding_color: "#49b1f5"
    blockquote_background_color: "#49b1f5"
    scrollbar_color: "#49b1f5"
    meta_theme_color_light: "ffffff"
    meta_theme_color_dark: "#0d0d0d"
  
  # The top_img settings of home page
  # default: top img - full screen, site info - middle (默認top_img全屏，site_info在中間)
  # The position of site info, eg: 300px/300em/300rem/10% (主頁標題距離頂部距離)
  index_site_info_top:
  # The height of top_img, eg: 300px/300em/300rem (主頁top_img高度)
  index_top_img_height:
  
  # The user interface setting of category and tag page (category和tag頁的UI設置)
  # index - same as Homepage UI (index 值代表 UI將與首頁的UI一樣)
  # default - same as archives UI 默認跟archives頁面UI一樣
  category_ui: # 留空或 index
  tag_ui: # 留空或 index
  
  # 网站背景
  background: "#778899"	# 亮岩灰，图片或颜色，颜色代码：https://encycolorpedia.cn/
  
  # 底部背景
  footer_bg: false	# true：顶部图延伸
  
  # the position of bottom right button/default unit: px (右下角按鈕距離底部的距離/默認單位為px)
  rightside-bottom:
  
  # 进入效果
  enter_transitions: true
  
  # Background effects (背景特效)
  # --------------------------------------
  
  # canvas_ribbon (靜止彩帶背景)
  # See: https://github.com/hustcc/ribbon.js
  canvas_ribbon:
    enable: false
    size: 150
    alpha: 0.6
    zIndex: -1
    click_to_change: false
    mobile: false
  
  # 动态彩带
  canvas_fluttering_ribbon:	# 动态彩带
    enable: true
    mobile: true	# 适用手机
  
  # canvas_nest
  # https://github.com/hustcc/canvas-nest.js
  canvas_nest:
    enable: false
    color: '0,0,255' #color of lines, default: '0,0,0'; RGB values: (R,G,B).(note: use ',' to separate.)
    opacity: 0.7 # the opacity of line (0~1), default: 0.5.
    zIndex: -1 # z-index property of the background, default: -1.
    count: 99 # the number of lines, default: 99.
    mobile: false
  
  # 打字效果
  activate_power_mode:
    enable: true
    colorful: true # 冒光特效
    shake: true # 抖动特效
    mobile: true
  
  # Mouse click effects: fireworks (鼠標點擊效果: 煙火特效)
  fireworks:
    enable: false
    zIndex: 9999 # -1 or 9999
    mobile: false
  
  # Mouse click effects: Heart symbol (鼠標點擊效果: 愛心)
  click_heart:
    enable: false
    mobile: false
  
  # 鼠标点击效果: 文字
  ClickShowText:	# 鼠标点击文字
    enable: true
    text:
      - 回归
      - 纯净
      - 自己
    fontSize: 15px
    random: false	# 随机
    mobile: true	# 手机
  
  # Default display mode (網站默認的顯示模式)
  # light (default) / dark
  display_mode: light
  
  # 文章小标题前图标
  beautify:
    enable: true
    field: post # site/post
    title-prefix-icon: # '\f0c1'
    title-prefix-icon-color: # '#F47466'
  
  # 全局字体
  font:
    global-font-size:
    code-font-size:
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", "Helvetica Neue", Lato, Roboto, "PingFang SC", "Microsoft JhengHei", "Microsoft YaHei", sans-serif
    code-font-family: consolas, Menlo, "PingFang SC", "Microsoft JhengHei", "Microsoft YaHei", sans-serif
  
  # 网站标题字体
  blog_title_font:	# 左上角网站名，主页居中网站名
    font_link: https://fonts.googleapis.com/css?family=Titillium+Web&display=swap
    font-family: Titillium Web, 'PingFang SC', 'Hiragino Sans GB', 'Microsoft JhengHei', 'Microsoft YaHei', sans-serif
  
  # 水平分隔线
  hr_icon:
    enable: true
    icon: # 字体图标的unicode值，例如“\ 3423”
    icon-top:
  
  # 主页副标题
  subtitle:
    enable: true
    effect: true	# 打字效果
    loop: true	# 循环打字
    source: 3	# 一言网/一句网/今日诗词/关闭：1/2/3/false
    sub:	# source设置false：只显示sub第一行文字
  
  # 加载动画
  preloader: true
  
  # 侧边栏
  aside:
    enable: true
    hide: false   # 隐藏
    button: true  # 设置按钮
    mobile: true # 手机上显示
    position: right # 左或右
    display:  # 显示归档、标签、分类数量
      archive: true
      tag: true
      category: true
    card_author:  # 显示站长卡片
      enable: true
      description: 我是站长    # 描述
      button: # 站长Github链接
        enable: true
        icon: fab fa-github
        text: Follow Me！
        link: https://github.com/wangmin-1995
    card_announcement:    # 公告
      enable: true
      content: 欢迎来到Minge的博客！
    card_recent_post: # 最近文章
      enable: true
      limit: 0 # 0为显示全部
      sort: updated # date/updated
      sort_order: # 轻易不修改
    card_categories:
      enable: true
      limit: 0 # 设置为0全部显示
      expand: true # 展开：none/true/false
      sort_order: # 轻易不修改
    card_tags: 
      enable: true
      limit: 0 # 设置为0全部显示
      color: true # 不同颜色
      sort_order: # 轻易不修改
    card_archives:
      enable: true
      type: monthly # yearly/monthly
      format: MMMM YYYY # 例: YYYY年MM月
      order: -1 # 升序/降序：1/-1
      limit: 0 # 设置为0全部显示
      sort_order: # 轻易不修改
    card_webinfo: # 网站信息卡片
      enable: true
      post_count: true
      last_push_date: true
      sort_order: # 轻易不修改
  
  # 访问人数
  busuanzi:
    site_uv: true
    site_pv: true
    page_pv: true
  
  # 网页运行时间
  runtimeshow:
    enable: true
    publish_date: 2/22/2022 22:22:22
  
  # 最新评论
  newest_comments:
    enable: false
    sort_order: # 轻易不修改
    limit: 6
    storage: 10 # 单位:分钟,将数据保存到本地文件
    avatar: true
  
  # 繁简转换
  translate:
    enable: true
    default: 繁
    defaultEncoding: 2	# 繁/简：1/2
    translateDelay: 0	# 延时
    msgToTraditionalChinese: '繁'
    msgToSimplifiedChinese: '簡'
  
  # 阅读模式
  readmode: true
  
  # 夜晚模式
  darkmode:
    enable: true
    button: true
    autoChangeMode: 3 # 根据系统自动切换/下午6点至上午6点/关闭：1/2/false
  
  # 按钮顺序
  rightside_item_order:
    enable: false
    hide: # readmode,translate,darkmode,hideAside
    show: # toc,chat,comment
  
  # 大图查看模式
  medium_zoom: false	# 2选1
  fancybox: true
  
  # 标签外挂
  # mermaid
  mermaid:
    enable: false
    theme:
      light: default
      dark: dark
  
  # Note (Bootstrap Callout)
  note:
    style: flat	# simple/modern/flat/desabled
    icons: true
    border_radius: 3
    light_bg_offset: 0
  
  # other
  # --------------------------------------
  
  # Pjax
  # It may contain bugs and unstable, give feedback when you find the bugs.
  # https://github.com/MoOx/pjax
  pjax:
    enable: false
    exclude:
      # - xxxx
      # - xxxx
  
  # Inject the css and script (aplayer/meting)
  aplayerInject:
    enable: false
    per_page: true
  
  # 弹窗
  snackbar:
    enable: false
    position: bottom-left # top-left / top-center / top-right / bottom-left / bottom-center / bottom-right
    bg_light: '#49b1f5' # 亮主题下
    bg_dark: '#1f1f1f' # 暗主题下
  
  # https://instant.page/
  # prefetch (預加載)
  instantpage: false
  
  # 中英文之間添加空格
  pangu:
    enable: true
    field: site # site/post
  
  # 图片懒加载
  lazyload:
    enable: false
    field: site # site/post
    placeholder:
    blur: false
  
  # PWA
  # See https://github.com/JLHwung/hexo-offline
  # ---------------
  # pwa:
  #   enable: false
  #   manifest: /pwa/manifest.json
  #   apple_touch_icon: /pwa/apple-touch-icon.png
  #   favicon_32_32: /pwa/32.png
  #   favicon_16_16: /pwa/16.png
  #   mask_icon: /pwa/safari-pinned-tab.svg
  
  # Open graph meta tags
  # https://developers.facebook.com/docs/sharing/webmasters/
  Open_Graph_meta: true
  
  # Add the vendor prefixes to ensure compatibility
  css_prefix: true
  
  # Inject
  # Insert the code to head (before '</head>' tag) and the bottom (before '</body>' tag)
  # 插入代码到头部 </head> 之前 和 底部 </body> 之前
  inject:
    head:
      # - <link rel="stylesheet" href="/xxx.css">
    bottom:
      # - <script src="xxxx"></script>
  
  # CDN
  # Don't modify the following settings unless you know how they work
  # 非必要請不要修改
  CDN:
    # The CDN provider of internal scripts (主題內部 js 的 cdn 配置)
    # option: local/jsdelivr/unpkg/cdnjs/custom
    # Dev version can only choose. ( dev版的主題只能設置為 local )
    internal_provider: local
  
    # The CDN provider of third party scripts (第三方 js 的 cdn 配置)
    # option: local/jsdelivr/unpkg/cdnjs/custom
    # when set it to local, you need to install hexo-butterfly-extjs
    third_party_provider: jsdelivr
  
    # Add version number to CDN, true or false  
    version: false
  
    # Custom format
    # For example: https://cdn.staticfile.org/${cdnjs_name}/${version}/${min_cdnjs_file}
    custom_format:
  
    option:
      # main_css:
      # main:
      # utils:
      # translate:
      # local_search:
      # algolia_js:
      # algolia_search_v4:
      # instantsearch_v4:
      # pjax:
      # gitalk:
      # gitalk_css:
      # blueimp_md5:
      # valine:
      # disqusjs:
      # disqusjs_css:
      # twikoo:
      # waline_js:
      # waline_css:
      # sharejs:
      # sharejs_css:
      # mathjax:
      # katex:
      # katex_copytex:
      # mermaid:
      # canvas_ribbon:
      # canvas_fluttering_ribbon:
      # canvas_nest:
      # lazyload:
      # instantpage:
      # typed:
      # pangu:
      # fancybox_css_v4:
      # fancybox_v4:
      # medium_zoom:
      # snackbar_css:
      # snackbar:
      # activate_power_mode:
      # fireworks:
      # click_heart:
      # ClickShowText:
      # fontawesomeV6:
      # flickr_justified_gallery_js:
      # flickr_justified_gallery_css:
      # aplayer_css:
      # aplayer_js:
      # meting_js:
      # prismjs_js:
      # prismjs_lineNumber_js:
      # prismjs_autoloader:
  ~~~

# <center>详细解析

## <center>导航目录

### 「目录」

- [x] ***「Menu」***

  ~~~yaml
  menu:
    主页: / || fas fa-home
    归档: /archives/ || fas fa-archive
    标签: /tags/ || fas fa-tags
    分类: /categories/ || fas fa-folder-open
    收藏||fas fa-list:
      音乐: /music/ || fas fa-music
      视频: /movies/ || fas fa-video
    友链: /link/ || fas fa-link
    关于: /about/ || fas fa-heart
  ~~~

  其中，***「标签」***、***「分类」***、***「音乐」***、***「视频」***、***「友链」***、***「关于」***需要手动创建页面

### 「标签」

- [x] ***「Tags」***

  ~~~bash
  hexo n page tags
  ~~~

  打开`博客/source/tags/index.md`

  ~~~markdown
  ---
  title: 标签
  date: 2022-06-26 19:56:25
  type: tags
  ---
  ~~~

  给文章加标签

  ~~~markdown
  ---
  title: 文章1
  date: 2022-06-26 19:56:25
  tags:
  - 标签1
  - 标签2
  ---
  文章内容
  ~~~

### 「分类」

- [x] ***「Categories」***

  ~~~bash
  hexo n page categories
  ~~~

  打开`博客/source/categories/index.md`

  ~~~markdown
  ---
  title: 分类
  date: 2022-06-26 20:04:08
  type: categories
  ---
  ~~~

  给文章分类

  ~~~markdown
  ---
  title: 文章2
  date: 2022-06-26 20:04:08
  categories: 博客
  ---
  文章内容
  ~~~

### 「音乐」

- [ ] ***「Music」***

  ~~~yaml
  hexo n page music
  ~~~

  打开`博客/source/music/index.md`

  ~~~markdown
  <head>
  <meta http-equiv="refresh" content="0;url=https://music.163.com/#/user?id=63658599">
  </head>
  ~~~

### 「视频」

- [ ] ***「Movies」***

  ~~~bash
  hexo n page movies
  ~~~

  打开`博客/source/movies/index.md`

  ~~~markdown
  <head>
  <meta http-equiv="refresh" content="0;url=https://ddrk.me/">
  </head>
  ~~~

### 「友链」

- [ ] ***「Link」***

  ~~~bash
  hexo n page link
  ~~~

  打开`博客/source/link/index.md`

  ~~~markdown
  ---
  title: 友链
  date: 2022-06-26 20:33:11
  type: link
  ---
  ~~~

  创建`博客/source/_data/link.yml`

  ~~~yaml
  - class_name: 友情鏈接
    class_desc: 那些人，那些事
    link_list:
      - name: Hexo
        link: https://hexo.io/zh-tw/
        avatar: https://d33wubrfki0l68.cloudfront.net/6657ba50e702d84afb32fe846bed54fba1a77add/827ae/logo.svg
        descr: 快速、简单且強大的网站框架
        
      - name: Butterfly
        link: https://butterfly.js.org/
        avatar: https://d33wubrfki0l68.cloudfront.net/6657ba50e702d84afb32fe846bed54fba1a77add/827ae/logo.svg
        descr: A Simple and Card Ul Design theme for Hexo
  
  - class_name: Minge
    class_desc: Good job
    link_list:
      - name: Minge
        link: https://minge.live
        avatar: https://d33wubrfki0l68.cloudfront.net/6657ba50e702d84afb32fe846bed54fba1a77add/827ae/logo.svg
        descr: Passing by...
  ~~~

### 「日志」

- [ ] ***「About」***

  ~~~bash
  hexo n page about
  ~~~

  打开`博客/source/about/index.md`

  ~~~markdown
  {% timeline 2022 %}
  <!-- timeline 2022年06月26日 -->
  重新整理博客😘
  重新记录日志😁
  目标突破55公斤大关🤣
  目前52左右徘徊😒
  <!-- endtimeline -->
  <!-- timeline 2022年06月28日 -->
  测试……
  <!-- endtimeline -->
  {% endtimeline %}
  ~~~

## <center>代码框

- [x] ***「Code Blocks」***

  ~~~yaml
  highlight_theme: light # 代码框样式
  highlight_copy: true # 复制按钮
  highlight_lang: true # 显示代码语法
  highlight_shrink: false  # 收缩代码块/展开代码块/展开代码块并隐藏按钮：true/false/none 
  highlight_height_limit: 200 # 代码框高度限制 unit: px
  code_word_wrap: false # 文本换行
  ~~~

## <center>复制

- [ ] ***「Copy Settings」***

  ~~~yaml
  copy:
    enable: true
    copyright:	# 复制的后面加版权信息
      enable: false
      limit_count: 50
  ~~~

## <center>社交图标

- [x] ***「Social Settings」***

  ~~~yaml
  social:
    fab fa-github: https://github.com/wangmin-1995 || Github
    fas fa-envelope: mailto:wangmin-1995@outlook.com || Email
  ~~~

## <center>站内搜索

### 「本地搜索」

- [x] ***「Local  Search」***

  ~~~yaml
  local_search:
    enable: true
    preload: false	# 预装
    CDN:
  ~~~

  需要安装插件
  
  ~~~bash
  npm install hexo-generator-search --save
  ~~~
  
  

### 「Algolia 搜索」

- [ ] ***「Algolia  Search」***

  {% btn 'https://github.com/LouisBarranqueiro/hexo-algoliasearch',[LouisBarranqueiro/hexo-algoliasearch: A plugin to index posts of your Hexo blog on Algolia (github.com)],far fa-hand-point-right,block outline right blue larger %}

## <Center>图标&图片

### 「网站图标」

- [x] ***「Favicon」***

  ~~~yaml
  favicon: /img/favicon.png
  ~~~

  找到`博客\themes\butterfly\source\img\favicon.png`，并用自己想用的网站图标替换***「favicon.png」***，注意图标名字还是***「favicon.png」***

### 「头像」

- [x] ***「Avatar」***

  ~~~yaml
  avatar:
    img: https://s2.loli.net/2022/06/26/GB9iaNPwlk4U1ho.jpg
    effect: false	# true：头像会一直转
  ~~~

### 「顶部图」

- [x] ***「Top Img」***

  ~~~yaml
  default_top_img: https://s2.loli.net/2022/05/06/MF6cDtkeNGTZbE1.jpg
  # 默认的top_img，当页面的top_img没有配置时，会显示default_top_img
  ~~~

### 「文章封面」

- [x] ***「Cover」***

  ~~~yaml
  cover:
    index_enable: true  # 是否显示文章封面
    aside_enable: true
    archives_enable: true
    position: both  # 封面显示的位置：left/right/both
    default_cover:	# 没有设置Front_matter时，默认显示的封面，可设置多个
      - https://s2.loli.net/2022/05/06/MF6cDtkeNGTZbE1.jpg
  ~~~

### 「无法显示的图片」

- [ ] ***「Error_404」***

  同***「Favicon」***，替换就好

## <center>文章封面信息

### 「日期&标签」

- [x] ***「post_meta」***

  ~~~yaml
  post_meta:
    page: # 主页
      date_type: both
      # 主页文章日期是创建日/更新日/都显示：created/updated/both
      date_format: date # 日期/相对日期：date/relative
      categories: true # 主页是否显示分类：true/false
      tags: true # 主页是否显示标签
      label: true # 主页是否显示描述
    post:	# 文章
      date_type: both # created/updated/both
      date_format: date # date/relative
      categories: true # true/false
      tags: true
      label: true
  ~~~

### 「摘要&描述」

- [x] ***「Description」***

  ~~~yaml
  index_post_content:
    method: 2	
    # 主页只显示描述/优先显示描述/自动节选/不显示摘要：1/2/3/false
    length: 500	# 节选长度
  ~~~

### 「字数统计」

- [x] ***「Word Count」***

  ~~~yaml
  wordcount:
    enable: true
    post_wordcount: true
    min2read: true
    total_wordcount: true
  ~~~

    需要安装插件
  
  ~~~bash
  npm i --save hexo-wordcount
  ~~~

- [x] ***「Index Post Content」***

  ~~~yaml
  index_post_content:
    method: 1	# 仅描述/优先描述/自动节选/不显示：1/2/3/false
    length: 500	# 节选范围
  ~~~

## <center>文章页

### 「文章锚点」

- [x] ***「Anchor」***

  ~~~yaml
  anchor: true	# 阅读文章时上下拖动，地址栏会根据当前位置的标题而变化
  ~~~

### 「目录」

- [x] ***「Toc」***

  ~~~yaml
  toc:
    post: true	# 在文章中显示
    page: false	# 不在标签、分类等页面中显示
    number: true	# 小标题加序号
    expand: true	# 一直展开
    style_simple: false # 侧边栏只显示目录，仅对文章页有效
  ~~~

### 「版权信息」

- [x] ***「Post Copyright」***

  ~~~yaml
  post_copyright:	
    enable: true	# 文章底部的版权信息框
    decode: true	# 显示中文网址
    author_href:
    license: CC BY-NC-SA 4.0
    license_url: https://creativecommons.org/licenses/by-nc-sa/4.0/
  ~~~

### 「捐助」

- [ ] ***「Reward」***

  ~~~yaml
  reward:
    enable: true
    QR_code:
      - img: /img/wechat.jpg
        link:
        text: wechat
      - img: /img/alipay.jpg
        link:
        text: alipay
  ~~~

  将***「wechat.jpg」***和***「alipay.jpg」***放入`博客\themes\butterfly\source\img`

### 「在线编辑」

- [ ] ***「Post Edit」***

  ~~~yaml
  post_edit:
    enable: false
    # For example: https://github.com/jerryc127/butterfly.js.org/edit/main/source/
    # 需要将本地仓库上传到Github仓库
    url:
  ~~~
  

### 「相似文章」

- [x] ***「Related Post」***

  ~~~yaml
  related_post:
    enable: true
    limit: 6 # 显示文章的数量
    date_type: created # 创建日/更新日：created/updated
  ~~~

### 「图片描述文字」

- [ ] ***「Figcaption」***

  ~~~yaml
  photofigcaption: false
  ~~~

### 「底部分页」

- [x] ***「Post Pagination」***

  ~~~yaml
  post_pagination: 2  # 下篇为旧文/下篇为新文/关闭：1/2/false
  ~~~

### 「文章过期提醒」

- [ ] ***「Outdated Notice」***

  ~~~yaml
  noticeOutdate:
    enable: false
    style: flat # style: simple/flat
    limit_day: 500 # When will it be shown
    position: top # position: top/bottom
    message_prev: It has been
    message_next: days since the last update, the content of the article may be outdated.
  ~~~

## <center>分享功能

- [ ] ***「Share System」***

  ~~~yaml
  # AddThis
  # https://www.addthis.com/
  addThis:
    enable: false
    pubid:
  
  # Share.js
  # https://github.com/overtrue/share.js
  sharejs:
    enable: true
    sites: facebook,twitter,wechat,weibo,qq
  
  # AddToAny
  # https://www.addtoany.com/
  addtoany:
    enable: false
    item: facebook,twitter,wechat,sina_weibo,facebook_messenger,email,copy_link
  ~~~


## <center>评论系统

- [ ] ***「Comments System」***

  {% btn 'https://valine.js.org/quickstart.html',[快速开始 | Valine 一款快速、简洁且高效的无后端评论系统。],far fa-hand-point-right,block outline right blue larger %}

  {% btn 'https://blog.csdn.net/Lott0419/article/details/107232586/',[LeanCloud保姆级配置教程_Lete乐特的博客-CSDN博客],far fa-hand-point-right,block outline right blue larger %}

  ***「待完善……」***

## <center>聊天系统

- [ ] ***「Chat Services」***

  ***「待完善……」***

  

## <center>页脚

- [ ] ***「Footer」***

  ~~~yaml
  footer:
    owner:
      enable: true
      since: 2022
    custom_text:
    copyright: true # Copyright of theme and framework
  ~~~

## <center>分析

- [ ] ***「Analysis」***

  ***「待完善……」***

## <center>广告

- [ ] ***「Advertisement」***

  ***「待完善……」***

## <center>站长验证

- [ ] ***「Verification」***

  ***「待完善……」***

## <center>美化

### 「主题颜色」

- [ ] ***「Theme Color」***

  ~~~yaml
  theme_color:
    enable: true
    main: "#778899"
    paginator: "#00c4b6"
    button_hover: "#FF7242"
    text_selection: "#00c4b6"
    link_color: "#99a9bf"
    meta_color: "#858585"
    hr_color: "#A4D8FA"
    code_foreground: "#F47466"
    code_background: "rgba(27, 31, 35, .05)"
    toc_color: "#00c4b6"
    blockquote_padding_color: "#49b1f5"
    blockquote_background_color: "#49b1f5"
    scrollbar_color: "#49b1f5"
    meta_theme_color_light: "ffffff"
    meta_theme_color_dark: "#0d0d0d"
  ~~~

### 「主页顶部图」

- [ ] ***「The Top_Img Settings Of Home Page」***

  ~~~yaml
  index_site_info_top:	# 主页标题距离顶部距离
  index_top_img_height:	# 主页顶部图高度
  ~~~

### 「分类&标签页UI」

- [ ] ***「The UI Setting Of Category And Tag Page」***

  ~~~yaml
  category_ui: # 留空或 index
  tag_ui: # 留空或 index
  # 留空/Index：同归档页/同主页
  ~~~

### 「网站背景」

- [x] ***「Website Background」***

  ~~~yaml
  background: "#778899"	# 亮岩灰，图片或颜色，颜色代码：https://encycolorpedia.cn/
  ~~~

### 「底部背景」

- [ ] ***「Footer Background」***

  ~~~yaml
  footer_bg: false	# true：顶部图延伸
  ~~~

### 「按钮位置」

- [ ] ***「The Position Of Bottom 」***

  ~~~yaml
  rightside-bottom:	# 右下角按钮距底部的距离，单位：Px
  ~~~

### 「进入效果」

- [ ] ***「Enter Transitions」***

  ~~~yaml
  enter_transitions: true
  ~~~

### 「背景特效」

- [x] ***「Background Effects」***

  ~~~yaml
  canvas_fluttering_ribbon:	# 动态彩带
    enable: true
    mobile: true	# 手机
  ~~~

### 「打字效果」

- [x] 「Activate Power Mode」

  ~~~yaml
  activate_power_mode:
    enable: true
    colorful: true # 冒光特效
    shake: true # 抖动特效
    mobile: true
  ~~~

### 「鼠标点击效果」

- [x] ***「Typewriter Effect」***

  ~~~yaml
  ClickShowText:	# 鼠标点击文字
    enable: true
    text:
      - 回归
      - 纯净
      - 自己
    fontSize: 15px
    random: false	# 随机
    mobile: true	# 手机
  ~~~

### 「网站显示模式」

- [ ] ***「Display Mode」***

  ~~~yaml
  display_mode: light	# 亮/暗：light/dark
  ~~~

### 「小标题前图标」

- [x] ***「Beautify」***

  ~~~yaml
  beautify:
    enable: true
    field: post # site/post
    title-prefix-icon: # '\f0c1'
    title-prefix-icon-color: # '#F47466'
  ~~~

### 「全局字体」

- [x] ***「Font」***

  ~~~yaml
  font:
    global-font-size:
    code-font-size:
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", "Helvetica Neue", Lato, Roboto, "PingFang SC", "Microsoft JhengHei", "Microsoft YaHei", sans-serif
    code-font-family: consolas, Menlo, "PingFang SC", "Microsoft JhengHei", "Microsoft YaHei", sans-serif
  ~~~

  

### 「网站标题字体」

- [x] ***「Font Settings」***

  ~~~yaml
  blog_title_font:	# 左上角网站名，主页居中网站名
    font_link: https://fonts.googleapis.com/css?family=Titillium+Web&display=swap
    font-family: Titillium Web, 'PingFang SC', 'Hiragino Sans GB', 'Microsoft JhengHei', 'Microsoft YaHei', sans-serif
  ~~~

### 「水平分隔线」

- [ ] ***「Divider Icon」***

  ~~~yaml
  hr_icon:
    enable: true
    icon: # 字体图标的unicode值，例如“\ 3423”
    icon-top:
  ~~~

### 「主页副标题」

- [x] ***「subtitle」***

  ~~~yaml
  subtitle:
    enable: true
    effect: true	# 打字效果
    loop: true	# 循环打字
    source: 3	# 一言网/一句网/今日诗词/关闭：1/2/3/false
    sub:	# source设置false：只显示sub第一行文字
  ~~~

### 「加载动画」

- [x] ***「Loading Animation」***

  ~~~yaml
  preloader: true
  ~~~

## <center>侧边栏

- [x] ***「Aside」***

  ~~~yaml
  aside:
    enable: true
    hide: false   # 隐藏
    button: true  # 设置按钮
    mobile: true # 手机上显示
    position: right # 左或右
    display:  # 显示归档、标签、分类数量
      archive: true
      tag: true
      category: true
    card_author:  # 显示站长卡片
      enable: true
      description: 我是站长    # 描述
      button: # 站长Github链接
        enable: true
        icon: fab fa-github
        text: Follow Me！
        link: https://github.com/wangmin-1995
    card_announcement:    # 公告
      enable: true
      content: 欢迎来到Minge的博客！
    card_recent_post: # 最近文章
      enable: true
      limit: 0 # 0为显示全部
      sort: updated # date/updated
      sort_order: # 轻易不修改
    card_categories:
      enable: true
      limit: 0 # 设置为0全部显示
      expand: true # 展开：none/true/false
      sort_order: # 轻易不修改
    card_tags: 
      enable: true
      limit: 0 # 设置为0全部显示
      color: true # 不同颜色
      sort_order: # 轻易不修改
    card_archives:
      enable: true
      type: monthly # yearly/monthly
      format: MMMM YYYY # 例: YYYY年MM月
      order: -1 # 升序/降序：1/-1
      limit: 0 # 设置为0全部显示
      sort_order: # 轻易不修改
    card_webinfo: # 网站信息卡片
      enable: true
      post_count: true
      last_push_date: true
      sort_order: # 轻易不修改
  ~~~


### 「访问人数」

- [ ] ***「Bu Suan Zi」***

  ~~~yaml
  busuanzi:
    site_uv: true
    site_pv: true
    page_pv: true
  ~~~

### 「网页运行时间」

- [x] ***「Run Time Show」***

  ~~~yaml
  runtimeshow:
    enable: true
    publish_date: 2/22/2022 22:22:22
  ~~~

### 「最新评论」

- [ ] ***「Newest Comments」***

  ~~~yaml
  newest_comments:
    enable: false
    sort_order: # 轻易不修改
    limit: 6
    storage: 10 # 单位:分钟,将数据保存到本地文件
    avatar: true
  ~~~

  ***「待完善……」***

## <center>右下角按钮

### 「繁简转换」

- [x] ***「Conversion」***

  ~~~yaml
  translate:
    enable: true
    default: 繁
    defaultEncoding: 2	# 繁/简：1/2
    translateDelay: 0	# 延时
    msgToTraditionalChinese: '繁'
    msgToSimplifiedChinese: '簡'
  ~~~

### 「阅读模式」

- [ ] ***「Read Mode」***

  ~~~yaml
  readmode: true
  ~~~

### 「夜晚模式」

- [x] ***「Dark Mode」***

  ~~~yaml
  darkmode:
    enable: true
    button: true
    autoChangeMode: 3 # 根据系统自动切换/下午6点至上午6点/关闭：1/2/false
  ~~~

### 「按钮顺序」

- [ ] ***「Item Order」***

  ~~~yaml
  rightside_item_order:
    enable: false
    hide: # readmode,translate,darkmode,hideAside
    show: # toc,chat,comment
  ~~~

## <center>大图查看模式

- [ ] ***「Light Box」***

  ~~~Yaml
  medium_zoom: false	# 2选1
  fancybox: true
  ~~~

## <center>标签外挂

- [ ] ***「Tag Plugins」***

  ~~~yaml
  # mermaid
  mermaid:
    enable: false
    theme:
      light: default
      dark: dark
  
  # Note (Bootstrap Callout)
  note:
    style: flat	# simple/modern/flat/desabled
    icons: true
    border_radius: 3
    light_bg_offset: 0
  ~~~

## <center>弹窗

- [ ] ***「Snackbar」***

  ~~~yaml
  snackbar:
    enable: false
    position: bottom-left # top-left / top-center / top-right / bottom-left / bottom-center / bottom-right
    bg_light: '#49b1f5' # 亮主题下
    bg_dark: '#1f1f1f' # 暗主题下
  ~~~

## <center>预加载

- [ ] ***「Prefetch」***

  ~~~yaml
  instantpage: false
  ~~~

## <center>中英文之間添加空格

- [x] ***「Pangu」***

  ~~~yaml
  pangu:
    enable: true
    field: site # site/post
  ~~~

## <center>图片懒加载

- [ ] ***「Lazyload」***

  ~~~yaml
  lazyload:
    enable: false
    field: site # site/post
    placeholder:
    blur: false
  ~~~


# <center>疑难杂症

- 此配置必须安装以下插件，不然会报错

  ~~~bash
  npm install hexo-generator-search --save
  ~~~

  ~~~bash
  npm i --save hexo-wordcount
  ~~~

  

