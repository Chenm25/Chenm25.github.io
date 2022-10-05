---
title: Jekyll 学习笔记
author: Chen
date: 2022-09-14 14:00:42 +0800
categories: [笔记]
tags: [note, jekyll]
pin: false
render_with_liquid: false
math: false
mermaid: false
---

# Jekyll 使用经验
1. 在使用 `jekyll s` 命令生成本地博客预览时，对 `_posts` 文件夹下的 `.md` 文档进行的新建、删除、修改，Jekyll 都会直接进行修改。在浏览器刷新博客页面时，就能看到内容已完成修改。
2. 用 Jekyll 来写博客，即便文章没有添加 Front Matter 也可以生成页面，添加 Front Matter 只是用于修改 post 的一些属性，比如是否置顶，是否有分类和标签等。但是，文件名必须要有日期，没有日期 Jekyll 将不会创建页面。
3. 在 `_posts` 文件夹下，可以创建子文件夹用于文章分类，Jekyll 能够正常识别子文件夹中的 `.md` 文档。
