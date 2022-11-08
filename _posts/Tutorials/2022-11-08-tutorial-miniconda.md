---
title: Miniconda 的安装和使用
date: 2022-11-08
tags: [tutorial, miniconda, python]
categories: [Tutorials]
---

# Miniconda 的安装和使用

## Miniconda 的安装

系统：Windows10

注意项：
1. 不要安装最新版本的 miniconda，可能会出现问题
2. 建议安装 Miniconda3-py37_4.9.2-Windows-x86_64 版本
3. 选择 Just Me
![1]({{ site.url }}/assets/images/001/1.png)
4. 将默认安装位置修改为非 C 盘的位置，因为后续此软件的所有下载内容都会保存在此目录下
![2]({{ site.url }}/assets/images/001/2.png)
5. 下一步这样勾选
![3]({{ site.url }}/assets/images/001/3.png)
6. Install

## Miniconda 的使用

1. 查看 conda 相关信息

   ```t
   # 查看conda相关信息
   # 在命令终端中输入
   conda info
   ```

2. 查看 conda 的下载源

   ```t
   # 查看conda现有的下载源
   # 在命令终端中输入
   
   conda config --show channels
   ```

3. 创建一个新的 Python 环境

   ```t
   # 创建一个新的 python 环境
   # 在命令终端中输入
   
   conda create -n python_3.8 python=3.8
   ```

4. 激活另一个 Python 环境

   ```t
   # 在命令终端中输入以下代码，来激活 python_3.6 环境
   
   conda activate python_3.6
   
   # 在命令终端中输入以下代码,来激活 base 环境
   
   conda activate base
   ```

5. 查看已安装 Python 环境

   ```t
   # 查看已安装的Python环境
   
   conda info --envs
   ```

6. 更新 conda

   ```t
   # Please update conda by running
   # 在CMD中输入
   
   conda update -n base -c defaults conda
   ```

7. 删除已安装的 Python 环境

   ```t
   # 假设你的环境名字叫: octopus
   
   conda remove -n octopus --all
   
   # Another example
   
   conda remove -n python_3.7.10 --all
   
   # 注意：Miniconda的base环境无法删除
   ```

8. 添加conda下载源

   ```t
   Example：
   给 conda 添加清华镜像源
   （用清华镜像源下载可以跑满网速）
   
   操作方式如下：
   1. 在命令行终端中输入 conda info
   2. 然后 Ctrl+鼠标左键，点击 user config file 的链接
   3. 在 VScode 中打开该文件，并参考文件中的格式添加上以下链接：
   http://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/win-64
   ```
