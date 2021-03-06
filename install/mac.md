---
layout: page
title: macOS
category: page
sidebar_link: false
---

# macOS平台安装部署教程（以High Sierra 10.13为例）

## 目录

- [第一步：安装鼠须管输入法](#第一步安装鼠须管输入法)
- [第二步 部署方言拼音方案](#第二步-部署方言拼音方案)
  - [1 找到你的方言拼音方案文件](#1-找到你的方言拼音方案文件)
  - [2 复制拼音方案文件](#2-复制拼音方案文件)
  - [3 启用拼音方案](#3-启用拼音方案)
- [小结](#小结)
- [但是我只会打普通话拼音，方言拼音该怎么打？](#但是我只会打普通话拼音方言拼音该怎么打)
- [（可选步骤）自定义鼠须管外观](#可选步骤自定义鼠须管外观)
  
如概述所说，安装过程只有两步：

1. 安装鼠须管输入法
2. 部署方言拼音方案

本章就以High Sierra 10.13系统为例手把手教你如何操作。

## 第一步：安装鼠须管输入法

1. 首先前往[rime官网](https://rime.im/)，下载鼠须管输入法![](.\mac\mac1.png)
2. 下载完成后，双击安装![](.\mac\mac2.png)![](.\mac\mac3.png)
3. 安装过程中会提醒安装完成后需要注销并重新登录![](.\mac\mac4.png)
4. 安装成功后，注销并重新登录![](.\mac\mac5.png)
5. 点击右上角切换输入法，发现已成功安装了鼠须管![](.\mac\mac6.png)
6. 尝试打几个字，可以见到安装成功，且输入的是繁体中文![](.\mac\mac7.png)
7. 怎么切换成简体字输入呢？只需要按下`Ctrl`和<code>`</code>（数字1左边那个键，和波浪号<code>~</code>相同）这两个键，就会弹出一个设置菜单![](.\mac\mac8.png)
8. 可以看到按1、3、4、5都是选择不同的输入方案，按2则进入格式设置![](.\mac\mac9.png)
9. 可以看到不只有简繁体切换，还有全半角和中英文切换，按下4，然后就可以用简体字输入了![](.\mac\mac10.png)
10. 且慢，说好的方言拼音呢？刚才的列表里不是普通话拼音就是笔划输入啊？这是因为鼠须管并不默认自带汉语方言拼音方案。要实现打家乡话拼音，还需接着第二步部署方言拼音方案。

## 第二步 部署方言拼音方案

#### 1 找到你的方言拼音方案文件

1. 首先点击[这里](https://www.icloud.com/iclouddrive/0avr_qtfuyJ2i5CHseRsR9yZg#download)下载最新版的汉语方言拼音方案合集，打开压缩包可以看到里面有两个`default.custom.yaml`、`default.yaml`文件和以各大方言区命名的文件夹![](.\mac\mac13.png)
2. 我们这里以苏州话为例，打开`吴语/苏州话`，可以看见里面有两个文件`wugniu_soutseu.dict.yaml`和`wugniu_soutseu.schema.yaml`，如下图，这就是我们要的拼音方案了。（如果你好奇这两个文件是什么来的，看[常见问题解答](../blog/faq.md)）![](.\mac\mac14.png)

#### 2 复制拼音方案文件

1. 点击右上角的鼠须管图标，可以看到弹出一个菜单，点击“用户设定”![](.\mac\mac15.png)
2. 这时会自动打开一个文件夹，然后把刚才的`default.custom.yaml`和`wugniu_soutseu.dict.yaml`和`wugniu_soutseu.schema.yaml`和这**三个文件**复制到这个文件夹内![](.\mac\mac16.png)

#### 3 启用拼音方案

1. 打开刚才复制进来的下的`default.custom.yaml`文件，可以见到里面有一些配置语句![](.\mac\mac22.png)
2. 在`schema-list:`的那一块的后面加上一行字：`  - schema: ID`（保持缩进对齐），其中把里面的ID替换成你的方案id，也就是`.schema.yaml`文件的文件名。例如我们这里用的是苏州话，所以就加上了`- schema: wugniu_soutseu`，如下图![](.\mac\mac17.png)
3. 保存后关闭文件，点击右上方的rime输入法图标，点“同步用户数据”，然后点击“重新部署”![](.\mac\mac11.png)
4. 再按下`Ctrl`和<code>`</code>，可以发现苏州话方案已经成功添加![](.\mac\mac18.png)
5. 尝试打几个字，可见部署成功![](.\mac\mac19.png)
6. 如果你想修改鼠须管的**候选词数量**，点[这里](./mac_custom.md)阅读教程。

## 小结

至此，我们终于实现了在Mac系统下的汉语方言拼音输入。所以以后如果需要添加其他汉语方言的输入方案，只需要记住以下三步就可以了

1. 复制后缀为`.dict.yaml`和`.schema.yaml`的方案文件到用户文件夹
2. 在`default.custom.yaml`中添加方案ID
3. 同步，重新部署

## 但是我只会打普通话拼音，方言拼音该怎么打？

鼠须管有一个很强大的拼音反查功能，如果你有个字只会普通话拼音，不知道他的方言拼音怎么打，就按下<code>`</code> ，然后打这个字的普通话拼音：![](.\mac\mac23.png)
这样就能像查字典一样查到任何字的方言拼音了。

当然，最重要的还是学会自己母语方言的拼音。所有的汉语方言拼音普通话拼音一样，很快就能掌握，如果你是母语者那就更轻松了。本站的[拼音方案简介](../blog/schema.md)列出了所有方言拼音方案的介绍和教程。只需稍加练习，以后和老乡亲戚聊天就都能舒畅地打家乡话啦！

## （可选步骤）自定义鼠须管外观

如果你想修改小狼毫的**皮肤外观、候选词数量、横排显示**等，点[这里](./mac_custom.md)阅读教程。