---
title: 「软件」解决Git慢速问题+Clash全局代理
tags:
  - Git
  - Clash
categories: 软件
cover: https://s2.loli.net/2022/07/20/JOtFRg2hsEAckPM.jpg
date: 2022-07-18 13:10:06
---




---

# <center>解决Git慢速问题

- 本地开启代理后，能正常用浏览器访问***「Google」***等外网，但对***「GIt bash」***、***「Netfilx」***等软件无效，这是因为这些软件默认不走代理，需要手动设置

- 给***「Git」***设置代理

  {% btn 'https://ruby-china.org/topics/40408',[如何提高 Github 的 pull/push 速度 · Ruby China (ruby-china.org)],far fa-hand-point-right,block outline right blue larger %}

  <img src="https://s2.loli.net/2022/07/18/F6JCWfYcwh8ZGeb.png" alt="image-20220718124615886" style="zoom: 67%;" />

  - [ ] ***「HTTP」***形式的仓库

    ~~~bash
    git config --global http.proxy "http://127.0.0.1:8080"
    git config --global https.proxy "http://127.0.0.1:8080"
    ~~~

    设置和取消也可以通过更改配置文件`C:\Users\Administrator\.gitconfig`进行

    端口号***「8080」***替换成***「Clash」***中的端口号

  - [ ] ***「SSH」***形式的仓库

    在`~/.ssh/config `设置代理

    ~~~
    Host github.com
        User git
        HostName github.com
        ProxyCommand nc -v -x 127.0.0.1:1080 %h %p
    ~~~

    若无此文件，可新建无后缀文件名***「config」***

---

# <center>Clash全局代理

- ***「Clash」***虚拟网卡***「TUN模式」***，更简单，高效，可以实现本机全局翻墙

  <img src="https://s2.loli.net/2022/07/18/DodmWgziZHR8vQ5.png" alt="屏幕截图 2022-07-18 130501" style="zoom:67%;" />

---
