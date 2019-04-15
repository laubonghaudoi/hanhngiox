---
layout: page
title: 小狼毫自定义
category: page
sidebar_link: false
---

## 自定义小狼毫显示外观

### 横排显示

1. 右键点击屏幕右下角的小狼毫输入法图标，在弹出菜单中点击“用户文件夹”![](.\win\win33.png)
2. 打开小狼毫的用户文件夹，可以见到有个名为`weasel.custom.yaml`的文件![](.\win\win35.png)
3. 用记事本打开，可以看到里面有一些配置语句![](.\win\win30.png)
4. 我们在最后面加上下面这行字（保持缩进），保存
  ```yaml
  "style/horizontal": true
  ```
  ![](.\win\win28.png)
3. 然后右键打开小狼毫菜单，点“重新部署”![](.\win\win25.png)
4. 再打几个字，可以见到小狼毫变成横排显示了![](.\win\win31.png)

### 更改候选词数量

1. 右键点击屏幕右下角的小狼毫输入法图标，在弹出菜单中点击“用户文件夹”![](.\win\win33.png)
2. 打开小狼毫的用户文件夹，可以见到有个名为`default.custom.yaml`的文件![](.\win\win34.png)
3. 打开这个`default.custom.yaml`，可以见到里面有一些配置语句![](.\win\win29.png)
4. 再最后面加上这行字（**保持原有的两格缩进**，里面的数字10可以改成你想要的数量，但不能超过10），然后保存
  ```yaml
    "menu/page_size": 10
  ```
  ![](.\win\win27.png)

4. 右键打开小狼毫菜单，点“重新部署”![](.\win\win25.png)
5. 可以看到小狼毫的候选词数量变成10个了![](.\win\win26.png)

## 高级定制

小狼毫是一个非常强大的输入法，可以任意配置最适合自己的输入方案，详情请参考Rime官网的[定制指南](https://github.com/rime/home/wiki/CustomizationGuide)。