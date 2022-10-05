---
title: Jekyll 教程
date: 2022-10-05
tags: [tutorial, jekyll]
categories: [Tutorials]
---

# Jekyll 搭建博客教程

本文将介绍如何在 Win10/11 下用 Jekyll 搭建个人博客。

## 1. Jekyll 博客本地搭建基础步骤

1. 到 [Ruby 官网](https://rubyinstaller.org/downloads/) 下载最新版本的Ruby+Devkit，下载完成后，点击安装文件，全部按照默认安装
2. 安装完成后，在命令行终端中输入 `ruby -v` 检查 Ruby 是否安装成功
3. 因为安装的是 Ruby+Devkit，Gem 也会附带安装，因此也输入 `gem -v` 查看 Gem 是否安装成功
4. Gem 安装成功后就可以开始安装 Jekyll 了，输入 `gem install jekyll bundler` 来安装 Jekyll 和 Bundler gems
5. 安装完成后，输入 `jekyll -v` 和 `bundle -v` 查看 Jekyll 和 bundler gem 是否安装成功
6. Jekyll 和 Bundle 安装成功后，在你计划存放你的博客的文件夹打开命令行终端，输入以下命令构建新的 blog site，并在本地运行

   ```shell
   jekyll new myblog
   cd myblog
   bundle exec jekyll serve
   ```

7. 这一步一般会出现报错，因为 Jekyll3 默认没有附带 webrick。输入 `bundle add webrick` 下载（注意：这个步骤每次新建一个 Jekyll site 都要再单独给那个 site 添加 webrick）
8. 接下来就可以正常使用了，再次输入 bundle exec jekyll serve，然后在浏览器中打开网址 http://127.0.0.1:4000/ ，即可查看生成的 Jekyll 博客站，到此为止，恭喜你，你已经成功在本地搭建了你的 Jekyll 博客了！

## 2. 如何使用主题

1. 这里以 Jekyll 主题 jekyll-theme-chirpy 的使用为例，介绍使用主题的最简单的步骤
2. 首先，创建一个空文件夹，在该文件夹中打开命令行终端，输入 `git init`，将文件夹变成一个 Git 仓库
3. 然后在终端中输入 `git clone https://github.com/cotes2020/jekyll-theme-chirpy.git`，将 jekyll-theme-chirpy 主题的 Github 仓库克隆到本地
4. 克隆完成后，在该主题文件夹下打开终端，输入 `bundle install` 来安装缺失的 gems
5. 安装完成后，在终端中输入 `bundle exec jekyll serve` 即可在本地预览该主题的博客了！

## 3. Jekyll 的基本操作

```shell
# 清除数据
jekyll clean

# 在本地运行博客
# 以下三种命令作用相同
bundle exec jekyll serve
jekyll serve
jekyll s
```
