---
layout: '[layout]'
title: Hexo theme config
date: 2017-04-25 11:33:22
tags: hexo
---

### 安装主题
从GitHub上获取代码，在..\hexo\themes目录，Git Bash Here , and excute：

``` bash
$ git clone https://github.com/iTimeTraveler/hexo-theme-hiker.git themes/hiker
```

### 改变主题
把Hexo主目录下的 _config.yml 文件中的字段 theme 修改为 hiker.
``` bash
theme: hiker
```
<!--more-->

### 更新主题

``` bash
$ cd themes/Hiker
$ git pull
```
### 自定义首页背景图
您可以将选择的大图放到 YOUR_HEXO_SITE\themes\hiker\source\css\images 文件夹下. 然后更改 hiker/_config.yml文件里的home_background_image字段.
``` bash
home_background_image:
  enable: true
  url: [css/images/poke.jpg, http://t.cn/RMbvEza]
```

如果url为空（enable仍然保持true）, 主题会自动使用下面这种漂亮的随机线条填充：
![](/images/random.jpg)

Ps：顺便补充一下如何在文章中插入图片: [官方文档](https://hexo.io/zh-cn/docs/asset-folders.html)

### Code 色彩主题
Hiker 使用[Tomorrow Theme](https://github.com/chriskempson/tomorrow-theme) 作为代码高亮的配色. 总共有六种选择: default, normal, night, night blue, night bright, night eighties

Modify highlight_theme in hiker/_config.yml.

``` bash
highlight_theme: default
```
I like the default one,so I don't modify it.

### 博客主题色

Modify theme_color in hiker/_config.yml.

``` bash
theme_color: random
```

### 夜间模式

只有在文章阅读页面，点击左上角的logo图片，就能打开设置对话框。






