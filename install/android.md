---
layout: page
title: Android
category: page
sidebar_link: false
---

# Android平台安装部署教程（以Android 8.1为例）

如概述所说，安装过程只有两步：

1. 安装同文输入法
2. 部署方言拼音方案

本章就以Android为例手把手教你如何操作。

## 第一步：安装同文输入法

1. 前往[Google Play下载安装](https://play.google.com/store/apps/details?id=com.osfans.trime)同文输入法（英文名为TRIME），或前往[此处](https://www.coolapk.com/apk/com.osfans.trime)下载apk安装包安装![](.\android\an2.png)
2. 安装成功后需要前往系统设置页面启用同文输入法，具体设置页面因系统而异，下图为Android One 8.1系统的输入法启用页面![](.\android\an6.png)
3. 然后打开同文输入法，在主页点击“选取”，选择同文输入法![](.\android\an3.png)
4. 切换到同文输入法尝试打几个字，这时会发现只能输入英文，无法使用任何拼音方案![](.\android\an7.png)
5. 这是因为同文输入法不默认自带汉语方言拼音方案。要实现打家乡话拼音，还需接着第二步部署方言拼音方案。

## 第二步：部署方言拼音方案

#### 1 找到你的方言拼音方案文件

首先点击[这里](https://www.icloud.com/iclouddrive/07J9Id9RquQsrdMag25JlG9bA#latest)下载最新版的汉语方言拼音方案合集，打开压缩包可以看到里面有一个`default.yaml`文件和以各大方言区命名的文件夹。
![](.\ios\ios9.png)
找到你想要输入的方言。我们这里以苏州话为例，打开`吴语/苏州话`，可以见到里面有两个文如下图有两个文件：`wugniu_soutseu.dict.yaml`和`wugniu_soutseu.schema.yaml`，这就是我们要的拼音方案了。（如果你好奇这两个文件是什么来的，看[这里](..\blog\faq.md)）
![](.\win\win10.png)

#### 2 复制拼音方案文件

1. 先在手机的文件管理器上找到rime文件夹，其具体路径因不同手机而异，一般就在系统储存目录下，打开rime文件夹可以见到一个opencc文件夹、`installation.yaml`和`trime.yaml`等扩展名为`.yaml`的文件，如下图![](.\android\an14.png)
2. 用电脑连接手机，把上一步中的**两个拼音方案文件和`default.yaml`，总共三个文件**复制到刚才手机中的的rime文件夹下。这里以苏州话为例，故复制`wugniu_soutseu.dict.yaml`、`wugniu_soutseu.schema.yaml`、`default.yaml`这三个文件到rime文件夹里。

#### 3 启用拼音方案

1. 回到同文输入法主页，点击“输入”![](.\android\an15.png)
2. 然后点击“同步”![](.\android\an16.png)
3. 回到主页，点击“部署”![](.\android\an17.png)
4. 再点击“输入”，进入刚才的界面，点“方案”，就能见到自己想使用的方案了，勾选方案后点确定![](.\android\an9.png)
5. 再尝试打几个字，大功告成![](.\android\an8.png)

## 小结

至此，我们终于实现了在Android系统下的汉语方言拼音输入。所以以后如果需要添加其他汉语方言的输入方案，只需要记住以下两步就可以了

1. 用电脑连接手机，把后缀为`.dict.yaml`和`.schema.yaml`的两个方案文件上传（`default.yaml`已经有了就不用再传了）
2. 点击同步、部署，再选择方案

### 但是我只会打普通话拼音，方言拼音该怎么打啊？

不用担心，方言拼音就和普通话拼音一样，很快就能掌握，如果你是母语者那就更轻松了。本站的[拼音方案简介](../blog/schema.md)列出了所有方言拼音方案的介绍和教程。只需稍加练习，以后和老乡亲戚聊天就都能舒畅地打家乡话啦！

## （可选步骤）自定义同文输入法外观

1. 在键盘里，先按“符号”，再长按“数字/配色”，就会出现一个主题色菜单：![](.\android\an18.jpg)
2. 选取自己喜欢的主题，确认后就可以见到新的皮肤主题了：![](.\android\an19.jpg)
3. 如果你想修改同文输入法的皮肤外观、键位等，点[这里](https://github.com/osfans/trime/wiki/trime.yaml%E8%A9%B3%E8%A7%A3)阅读教程。
