---
layout: page
title: Linux
category: page
sidebar_link: false
---

# Linux平台安装部署教程（以Ubuntu 18.04为例）

如概述所说，安装过程只有两步：

1. 安装小狼毫输入法
2. 部署方言拼音方案

本章就以Ubuntu 18.04为例手把手教你如何操作。

## 第一步：安装ibus-rime输入法

1. 在终端输入以下命令：
   ```bash
   sudo apt-get update
   sudo apt-get install ibus-rime
   ```
2. 重启电脑
3. 打开系统设置，点“区域和语言”，再点“输入源”下面的+号![](.\linux\linux1.png)
4. 找到汉语，点击![](.\linux\linux2.png)
5. 选择列表中的“汉语(Rime)”，再点添加![](.\linux\linux3.png)
6. 然后可以看到成功添加了输入源![](.\linux\linux4.png)
7. 点击右上角的输入法图标，选择Rime![](.\linux\linux5.png)
8. 然后会显示Rime正在维护，稍等一会之后尝试输入几个字，发现可以使用普通话拼音了![](.\linux\linux6.png)
9. 怎么切换成简体字输入呢？只需要按下`Ctrl`和<code>`</code>（数字1左边那个键，和波浪号<code>~</code>相同）这两个键，就会弹出一个设置菜单![](.\linux\linux7.png)
10. 可以看到按1、3、4、5都是选择不同的输入方案，按2则进入格式设置![](.\linux\linux8.png)
11. 可以看到不只有简繁体切换，还有全半角和中英文切换，按下4，然后就可以用简体字输入了![](.\linux\linux9.png)
12. 且慢，说好的汉语方言拼音呢？刚才的列表里不是普通话拼音就是笔划输入啊？看官莫急，这是因为ibus-rime并不默认自带汉语方言拼音方案。要实现打家乡话拼音，还需接着第二步部署方言拼音方案。

## 第二步 （仅限广州话）启用拼音方案

ibus-rime自带了粤语广州话的拼音方案（粤拼），所以想输入广州话的读者可以免去较繁琐的部署过程，直接启用广州话拼音方案。**非广州话用户请直接跳到本教程下一节**。

1. 在终端中运行以下命令：
   ```bash
   sudo apt-get install librime-data-jyutping
   ```
2. 打开`~/.config/ibus/rime`路径（其中`.config`为隐藏文件夹，需要按`Ctrl`+`H`显示），可以见到如图所示的一些文件![](.\linux\linux10.png)
3. 打开编辑其中的`default.yaml`文件，可以见到里面有一些配置语句![](.\linux\linux11.png)
4. 在`schema-list:`的那一块的后面加上一行字`- schema: jyutping`，注意保持两格缩进，如图![](.\linux\linux12.png)
5. 如果你想把输入法的候选词数量增加到10个（最多10个），则把下面的`page_size: 5`改成`page_size: 10`，另外也可以把不需要的方案删去，只留下粤拼和普通话拼音，如图![](.\linux\linux13.png)
6. 保存后关闭文件，点击右上方的rime输入法图标，点“部署”![](.\linux\linux5.png)
7. 再按下`Ctrl`和<code>`</code>，可以发现粤拼方案已经成功添加![](.\linux\linux15.png)
8. 尝试打几个字，可见部署成功，候选词数量也增加到10个![](.\linux\linux16.png)

***请直接跳到本页最下方“小结”一节继续教程。***

## 第二步（非广州话）部署方言拼音方案

#### 1 找到你的方言拼音方案文件

1. 首先点击[这里](https://github.com/laubonghaudoi/Chinese_Rime/releases/download/v0.1.2/v0.1.2.zip)下载最新版的汉语方言拼音方案合集，打开压缩包可以看到里面有以各大方言区命名的文件夹，如下图![](.\linux\linux17.png)
2. 我们这里以苏州话为例，打开`吴语/苏州话`，可以见到里面有两个文件：`wugniu_soutseu.dict.yaml`和`wugniu_soutseu.schema.yaml`，这就是我们要的拼音方案了。（如果你好奇这两个文件是什么来的，看[这里](../blog/faq.md)）![](.\linux\linux20.png)


#### 2 复制拼音方案文件

1. 打开`~/.config/ibus/rime`路径（其中`.config`为隐藏文件夹，需要按`Ctrl`+`H`显示），可以见到如图所示的一些文件![](.\linux\linux10.png)
2. 把刚才的两个拼音方案文件复制到这个路径下，这里以苏州话为例，我们复制`wugniu_soutseu.dict.yaml`和`wugniu_soutseu.schema.yaml`到这个文件夹下![](.\linux\linux21.png)

#### 3 启用拼音方案

1. 打开该路径下的`default.yaml`文件，可以见到里面有一些配置语句![](.\linux\linux11.png)
2. 在`schema-list:`的那一块的后面加上一行字：`  - schema: ID`（保持缩进对齐），其中把里面的ID替换成你的方案id，也就是`.schema.yaml`文件的文件名。例如我们这里用的是苏州话，所以就加上了`- schema: wugniu_soutseu`，也可以把不需要的方案删去，只留下苏州话方案，如下图![](.\linux\linux18.png)
3. 如果你想把输入法的候选词数量增加到10个（最多10个），则把下面的`page_size: 5`改成`page_size: 10`，如图![](.\linux\linux19.png)
4. 保存后关闭文件，点击右上方的rime输入法图标，点“同步”，然后点击“部署”![](.\linux\linux25.png)
5. 再按下`Ctrl`和<code>`</code>，可以发现苏州话方案已经成功添加![](.\linux\linux22.png)
6. 尝试打几个字，可见部署成功，候选词数量也增加到10个![](.\linux\linux23.png)

## 小结

至此，我们终于实现了在Linux系统下的汉语方言拼音输入。所以以后如果需要添加其他汉语方言的输入方案，只需要记住以下三步就可以了

1. 复制后缀为`.dict.yaml`和`.schema.yaml`的方案文件到用户文件夹
2. 在`default.yaml`中添加方案ID
3. 同步，重新部署

## 但是我只会打普通话拼音，方言拼音该怎么打？

ibus-rime有一个很强大的拼音反查功能，如果你有个字只会普通话拼音，不知道他的方言拼音怎么打，就按下<code>`</code> ，然后打这个字的普通话拼音：![](.\linux\linux24.png)
这样就能像查字典一样查到任何字的方言拼音了。

当然，最重要的还是学会自己母语方言的拼音。所有的汉语方言拼音普通话拼音一样，很快就能掌握，如果你是母语者那就更轻松了。本站的[拼音方案简介](../blog/schema.md)列出了所有方言拼音方案的介绍和教程。只需稍加练习，以后和老乡亲戚聊天就都能舒畅地打家乡话啦！
