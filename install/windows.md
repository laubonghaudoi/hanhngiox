---
layout: page
title: Windows
category: page
sidebar_link: false
---

# Windows平台安装部署教程（以Win 10为例）

如概述所说，安装过程只有两步：

1. 安装小狼毫输入法
2. 部署方言拼音方案

本章就以Windows 10系统为例手把手教你如何操作（别担心Win7也一样的，不行的话尽管[邮件](mailto:laubonghaudoi@qq.com)骂我）。

注：有的版本Windows系统会检测到小狼毫为恶意软件和木马，这是Windows Defender自身的误判问题。小狼毫是一个开源的输入法软件，不含任何恶意程序。如果安装包被系统检测为恶意程序，请先参考[这篇文章](https://zhuanlan.zhihu.com/p/30675056)的第一步**关闭实时保护**，再开始安装。

## 第一步：安装小狼毫输入法

1. 首先前往[rime官网](https://rime.im/)，下载小狼毫输入法![](.\win\win1.png)
2. 下载完成后，双击安装![](.\win\win2.jpg)
3. Win10可能会弹出安全提醒，这时点击“更多信息→仍要运行”，然后通过管理员权限![](.\win\win3.jpg)![](.\win\win4.jpg)
4. 正式进入小狼毫安装界面，点击“我接受”，然后选择安装路径，再点击“安装”![](.\win\win5.jpg)![](.\win\win6.png)
5. 安装成功后，出现安装选项界面![](.\win\win7.jpg)
6. 选择好输入大陆或台湾字体后点击“安装”，即出现安装成功界面![](.\win\win8.png)![](.\win\win9.png)
7. 这时再点击任务栏右下角的输入法图标，就可以看到小狼毫输入法![](.\win\win12.png)
8. 点击切换到小狼毫输入法，随便打几个字，可以发现默认用的是普通话拼音输入，而且是繁体字![](.\win\win13.png)
9. 怎么切换成简体字输入呢？只需要按下`Ctrl`和<code>`</code>（数字1左边那个键，和波浪号<code>~</code>相同）这两个键，就会弹出一个设置菜单![](.\win\win14.png)
10. 可以看到按1、3、4、5都是选择不同的输入方案，按2则进入格式设置![](.\win\win15.png)
11. 可以看到不只有简繁体切换，还有全半角和中英文切换，按下4，然后就可以用简体字输入了![](.\win\win16.png)
12. 再打开开始菜单，可以见到新添加的一系列小狼毫输入法程序，点击“【小狼毫】输入法设定”![](.\win\win11.png)
13. 进入输入法设定界面后可以看到有各种可选的输入方案，勾选自己想要的然后点“中”![](.\win\win36.png)
14. 然后进入皮肤选择界面，选择自己喜欢的皮肤，再点“中”，就大功告成啦![](.\win\win18.jpg)![](.\win\win18.png)
15. 且慢，说好的方言拼音呢？刚才的列表里不是普通话拼音就是笔划输入啊？这是因为小狼毫并不默认自带汉语方言拼音方案。要实现打家乡话拼音，还需接着第二步部署方言拼音方案。

## 第二步 （仅限部分语言）快捷启用拼音方案

小狼毫默认自带了部分语言的拼音方案，可以免去较繁琐的部署过程直接启拼音方案。**如果你的想输入的语言在以下列表**中，可继续阅读本节快速启用方言拼音，**否则直接跳到下一节使用通用方法部署拼音方案**。

- 中原官话
  - 洛阳话：洛陽羅馬字　`Patricivs/lakyang`
  - 郑州话：中州羅馬字　`lotem/rime-zhung`
  - 枣庄话：嶧州話傳統羅馬字 `tsauibusato/yihdjoouhuah`
- 江淮官话
  - 南京话：南京話拼音输入法 `uliloewi/lang2jin1`
  - 黄冈话 - 黄孝片 `yuxifongfei/hubehua`
  - 鄂城话 - 黄孝片 `yuxifongfei/hubehua`
- 西南官话
  - 通用四川话 - 蜀拼通音 `Papnas/shupin`
  - 成都话 - 蜀拼-成都 `Papnas/shupin`
  - 重庆话 - 蜀拼-重慶 `Papnas/shupin`
  - 宜宾话 - 蜀拼-宜賓 `Papnas/shupin`
  - 贵阳话 - 蜀拼-貴陽 `Papnas/shupin`
  - 自贡话 - 蜀拼-自貢 `Papnas/shupin`
  - 武汉话 - 武漢 `yuxifongfei/hubehua`
- 吴语
  - 苏州话：吳語（蘇州） `NGLI/rime-wugniu_soutseu`
  - 上海话：吳語（上海） `NGLI/rime-wugniu_zaonhe`
  - 松江话：吳語（松江） `NGLI/rime-wugniu_zaonhe`
  - 宁波话：吳語（寧波） `NGLI/rime-wugniu_gninpou`
  - 桐乡话：吳語（桐鄉） `NGLI/rime-wugniu_kashin`
  - 海宁话：吳語（海寧） `NGLI/rime-wugniu_kashin`
  - 海盐话：吳語（海鹽） `NGLI/rime-wugniu_kashin`
  - 嘉兴话：吳語（嘉興） `NGLI/rime-wugniu_kashin`
  - 嘉善话：吳語（嘉善） `NGLI/rime-wugniu_kashin`
- 粤语
  - 广州话：粤拼 `jyutping`
  - 南宁话：南寧白話輸入方案 `leimaau/naamning_jyutping`
  - 藤县话：粵語勾漏片藤县白话 `cryptogun/gaulau_jyutping`
- 客家话
  - 通用客家话：客語 `syndict/hakka`
  - 梅县话：客語-梅縣 `syndict/hakka`
- 莆仙语（兴化语）
  - 莆田话：興化語莆田城關話 `Yaryou/HinghuaFactory`
- 闽南语（河洛话）
  - 厦门话：閩南語廈門音 `a-thok/rime-hokkien`
  - 台湾话：閩南語臺灣音 `a-thok/rime-hokkien`
  - 漳州话：閩南語漳州音 `a-thok/rime-hokkien`
  - 泉州话：閩南語泉州音 `a-thok/rime-hokkien`
  - 潮州话：潮語拼音（潮州） `Kahaani/dieghv`
  - 汕头话：潮語拼音（汕頭） `Kahaani/dieghv`
  - 潮阳话：潮語拼音（潮陽） `Kahaani/dieghv`
  - 揭阳话：潮語拼音（揭陽） `Kahaani/dieghv`
  - 澄海话：潮語拼音（澄海） `Kahaani/dieghv`
  - 饶平话：潮語拼音（饒平） `Kahaani/dieghv`

上面的列表中，每门语言之后的是拼音方案名称，后面一串字母是方案代号。有的语言例如潮汕话，是多个方音共用一个方案代号`Kahaani/dieghv`。找到自己语言的方案名称和代号之后开始以下步骤启用方案：
1. 打开“【小狼毫】输入法设定”![](.\win\win11.png)
2. 点击左下方的“獲取更多輸入方案”![](.\win\win37.png)
3. 这时会弹出一个命令行界面![](.\win\win38.png)
4. 然后把你想输入的语言的方案代号复制进去，再按回车。例如要输入广州话，则复制`jyutping`再按回车，然后可以见到方案部署成功![](.\win\win39.png)
5. 关闭命令行界面，回到小狼毫设定界面，可以见到方案列表可以勾选拼音方案了![](.\win\win40.png)
6. 点“中”完成配置后，重复刚才的步骤按`Ctrl`和<code>`</code> （数字1左边那个键，和波浪号<code>~</code>相同）两个键，选择粤拼方案，就可以打广州话拼音了！![](.\win\win41.png)![](.\win\win42.png)

***请直接跳到本页最下方“小结”一节继续教程。***


## 第二步（通用方法）部署方言拼音方案

#### 1 找到你的方言拼音方案文件

1. 首先点击[这里](https://www.icloud.com/iclouddrive/0dPS83mznhuPpzlDYc8SrWTpA#download)下载最新版的汉语方言拼音方案合集，打开压缩包可以看到里面有一个`default.custom.yaml`和`default.yaml`文件（这两个文件是给其他平台用户的，我们Windows忽略它就行了）和以各大方言区命名的文件夹。![](.\win\win2.png)
2. 我们这里以苏州话为例，打开`吴语/苏州话`，可以看见里面有两个文件：`wugniu_soutseu.dict.yaml`和`wugniu_soutseu.schema.yaml`，如下图，这就是我们要的拼音方案了。（如果你好奇这两个文件是什么来的，看[这里](../blog/faq.md)）
   ![](.\win\win10.png)

#### 2 复制拼音方案文件

1. 右键点击任务栏右下角的小狼毫图标，可以看到弹出一个菜单
![](.\win\win17.png)
2. 点击“用户文件夹（C）”，这时会自动打开`C:\Users\用户名\AppData\Roaming\Rime`下的文件夹，可以看到里面有几个文件和文件夹
![](.\win\win19.png)
3. 然后把`wugniu_soutseu.dict.yaml`和`wugniu_soutseu.schema.yaml`这两个文件复制到这里，如下图
![](.\win\win20.png)

好，方案部署完了，然后我们启用这个方案，就能用它来打字啦。

#### 3 启用拼音方案

1. 右键小狼毫图标，点“用户资料同步”
![](.\win\win21.png)
2. 再从开始菜单打开“【小狼毫】输入法设定”，可以看到现在能勾选苏州话拼音方案了
![](.\win\win22.png)
3. 点“中”完成配置后，重复刚才的步骤按`Ctrl`和<code>`</code> （数字1左边那个键，和波浪号<code>~</code>相同）两个键，选择苏州话拼音方案，就可以打苏州话拼音了！
![](.\win\win23.png)![](.\win\win24.png)

## 小结

至此，我们终于实现了在Windows系统下的汉语方言拼音输入。所以以后如果需要添加其他汉语方言的输入方案，只需要记住以下三步就可以了

快捷方式（仅限部分语言）：
1. 打开小狼毫输入法设定界面，点“獲取更多輸入方案”
2. 输入方案代号后回车，直接下载部署拼音方案
3. 回到界面勾选输入方案

通用方式（适用于全部语言）： 
1. 复制后缀为`.dict.yaml`和`.schema.yaml`的方案文件到用户文件夹
2. 用户资料同步
3. 小狼毫输入法设定勾选方案

## 但是我只会打普通话拼音，方言拼音该怎么打？

小狼毫有一个很强大的拼音反查功能，如果你有个字只会普通话拼音，不知道他的方言拼音怎么打，就按下<code>`</code> ，然后打这个字的普通话拼音：![](.\win\win32.png)
这样就能像查字典一样查到任何字的方言拼音了。

当然，最重要的还是学会自己母语方言的拼音。所有的汉语方言拼音普通话拼音一样，很快就能掌握，如果你是母语者那就更轻松了。本站的[拼音方案简介](../blog/schema.md)列出了所有方言拼音方案的介绍和教程。只需稍加练习，以后和老乡亲戚聊天就都能舒畅地打家乡话啦！

## （可选步骤）自定义小狼毫外观

如果你想修改小狼毫的**皮肤外观、候选词数量、横排显示**等，点[这里](./windows_custom.md)阅读教程。
