---
layout: category
title: 常见问题解答
sidebar_sort_order: 6
---

# 常见问题解答

### 1 那两个拼音方案文件是什么来的

这两个以`.dict.yaml`和`.schema.yaml`为扩展名的文件，就是专为中州韵系列输入法编写的拼音方案文件。如果你好奇地打开他们看一下，会发现前者是一个字表，后者是输入方案定义文件。

一般来讲这两个文件的前缀名都一样，就是这个方案的ID。例如我们用的苏州话方案文件都叫`wugniu_soutseu`。但有一些输入方案会共享一个字表文件，例如闽南语下的漳州话、泉州话、厦门话、台湾话的字表文件都是`banlam.dict.yaml`。这时你可以打开`.schema.yaml`文件，就会见到有一行字显示`schema_id: XXX`，这里的XXX就是方案ID了。我们在`default.custom.yaml`添加这个ID名就是为了让输入法知道我们要用这个方案。

### 2 暂未支持的语言

从首页的列表可以看到，我们暂未支持以下语言：

- 湘语
- 徽语
- 赣语
- 官话
  - 兰银官话
  - 胶辽官话
- 闽语
  - 闽北语
  - 闽中语
  - 莆仙语

请有编写上述语言拼音方案的作者尽快[联系我](mailto:laubonghaudoi@icloud.com)，以添加上述语言的支持，非常感谢你的帮助和贡献。

### 3 这个汉语方言项目很有意思！我想为它贡献一点自己的力量，我可以做些什么吗？

首先很感激你对我们项目的兴趣和支持！如果你想为我们的事业贡献自己的一份力量的话，可以：

1. 多多向亲戚朋友们分享这个网站：www.hanhngiox.net，让更多的人知道我们这项事业。
2. 按照本网站的教程安装使用中州韵系列输入法，平时多用方言拼音打字，
3. 对于输入法，向我[反馈](mailto:laubonghaudoi@icloud.com)各种bug。对于项目和网站本身，提任何改进意见。如果你会用GitHub的话，可以直接在我的[项目仓库](https://github.com/laubonghaudoi/Chinese_Rime/issues)里新开一个issue
4. 如果你愿意为扩展方言拼音词库贡献自己的用户词库，让输入法更智能好用，欢迎[联系我](mailto:laubonghaudoi@icloud.com)。
5. 如果你懂语言学或会编程，想为这个项目做更高级的贡献，也请[联系我](mailto:laubonghaudoi@icloud.com)。