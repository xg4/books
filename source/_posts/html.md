---
title: HTML
date: 2018-12-11 18:24:24
tags: HTML
---

## Table of Contents

- [Table of Contents](#table-of-contents)
- [HTML5 结构化元素](#html5-%E7%BB%93%E6%9E%84%E5%8C%96%E5%85%83%E7%B4%A0)
- [Meta](#meta)
- [Link](#link)

## HTML5 结构化元素

| 标签    | 作用                                                                                                                                                    |
| ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| header  | body、main 标签的直接子标签，位置在页面头部，内容可能为 logo、标语、搜索提示、导航栏                                                                    |
| nav     | 导航栏包在 nav 标签内，可能出现在头部、侧边栏、底部等等，神奇的地方在于设置 nav 标签的 display:inline-block，是作用在 li 标签上的                       |
| main    | body 标签的直接子标签，主内容区域                                                                                                                       |
| aside   | 侧边栏                                                                                                                                                  |
| article | 一般出现在 main 标签内，article 标签内可以有 section、footer 等标签，是比较独立的内容，比如像博客网站主页的一个文章简介                                 |
| section | section 和 div 很类似，如果使用 div 标签是为了对内容做样式控制，或者为了便于 javascript 获取做其他操作，那么使用 div 就是你的答案，其他情况就用 section |
| address | 提供联系信息，放在 article 标签内提供文章作者信息，放在 main、body、footer 内提供网站信息                                                               |
| footer  | 一般在 HTML 结构底部，补充网站信息，如果放在 article 内补充文章信息                                                                                     |

## Meta

```html
<meta charset="utf-8" />

<!-- SEO -->
<title>document</title>
<meta name="keywords" content="keywords" />
<meta name="description" content="description" />

<meta name="author" content="xg4, xingor4@gmail.com" />

<!-- mobile -->
<meta
  name="viewport"
  content="width=device-width, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0, user-scalable=no, shrink-to-fit=no"
/>

<meta name="theme-color" content="#000000" />

<!-- chromium -->
<meta http-equiv="X-UA-Compatible" content="ie=edge,chrome=1" />
<meta name="renderer" content="webkit|ie-comp|ie-stand" />
<meta name="force-rendering" content="webkit|ie-comp|ie-stand" />

<!-- full screen -->
<meta name="full-screen" content="yes" />
<meta name="x5-fullscreen" content="true" />

<!-- robots -->
<meta name="robots" content="index, about" />

<!-- orientation -->
<meta name="screen-orientation" content="portrait" />
<meta name="x5-orientation" content="portrait" />

<!-- 禁止识别电话号码和邮箱 -->
<meta name="format-detection" content="telephone=no, email=no" />

<!-- web app -->
<meta name="browsermode" content="application" />
<meta name="x5-page-mode" content="app" />
<meta name="apple-mobile-web-app-capable" content="yes" />

<!-- status bar style -->
<meta name="apple-mobile-web-app-status-bar-style" content="default" />

<!-- add to home screen of title -->
<meta name="apple-mobile-web-app-title" content="title" />

<!-- windows phone tap highlight -->
<meta name="msapplication-tap-highlight" content="no" />

<!-- old device -->
<meta name="MobileOptimized" content="320" />
<meta name="HandheldFriendly" content="true" />
```

## Link

```html
<!-- icon -->
<link
  rel="apple-touch-icon-precomposed"
  sizes="57x57"
  href="/icons/apple-touch-icon.png"
/>
<link
  rel="apple-touch-icon-precomposed"
  sizes="72x72"
  href="/icons/apple-touch-icon.png"
/>
<link
  rel="apple-touch-icon-precomposed"
  sizes="114x114"
  href="/icons/apple-touch-icon.png"
/>
<link
  rel="apple-touch-icon-precomposed"
  sizes="144x144"
  href="/icons/apple-touch-icon.png"
/>

<!-- PWA -->
<link rel="manifest" href="/manifest.json" />

<!-- favicon -->
<link rel="shortcut icon" href="/favicon.ico" />
```