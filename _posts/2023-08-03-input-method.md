---
layout:      post
title:       更高效的输入方式
author:      Ludwig Huang
categories:  other
tags:        [chinese, guide]
image:       typewriter-1.jpg
toc:         false
description: 输入方法论，Vim、双拼输入法简单介绍，以及键鼠输入概论。
---

### 输入方法论

不同于上个世纪的纸笔写作，本世纪以来的写作方法逐渐演变为：通过键盘与计算机进行交互。然而，此类写作方法对于［本人的］中文写作产生非常强烈的负面影响。中文写作，所写的是**象形符号**“汉字”。在我看来，用纸笔写作时，写前一个汉字的思绪会自然而然地流向下一个汉字，一个句子的逻辑会流向下一个句子。如果写作时文章思路通畅，一篇中文文章会顺理成章地从笔下出现。然而，使用键盘写作的人会丢失这种若隐若现的「写作感觉」。

本篇文章无意于重新拾起纸笔写作的感觉，而希望建立起另一种「写作感觉」。前者来自于“**象形符号**固有的提示性”，后者来自于“**迅速**输入以抓住转瞬即逝的灵感”。**迅速**来自于熟练的输入经验（例如标准指法、盲打等），以及硬件、软件上的适配。

本文介绍的是：软件上的适配，以及简要的硬件知识。

### Vim

> 编辑方式 - [Vim](https://www.vim.org/)

Vim（**V**i **im**proved）是一款软件，其中蕴含着至关重要的文本编辑哲学——**尽可能少地离开主输入区**，无论是鼠标还是方向键。其重要作用体现在文本编辑的易操作性，但也有着令人生畏的[学习曲线](https://www.reddit.com/r/ProgrammerHumor/comments/9d3j49/text_editor_learning_curves/)。事实上，就像语言一样，Vim 并不难学习，关键在于克服**惰性与挫败感**。学习 Vim 是一本万利的打算，它能够让一个人了解到 only 主键盘区输入的魅力。

网络上已有大量的[输入方法教程](https://www.bilibili.com/video/BV1UQ4y1z7q5/)，本段不再赘述，而是介绍几个对 Windows 至关重要的配置。

* [**PowerToys**](https://github.com/microsoft/PowerToys)：使用其内部的 Keyboard Manager 工具，将 `CapsLock` 映射为 `Esc`。

  如果希望在日常写作中融入 Vim，可以将 `Win + H/J/K/;` 映射为 `Left/Down/Up/Right`。由于 Windows 限制了 `Win + L` 的使用，需要先[将其禁用](https://stackoverflow.com/questions/301053/re-assign-override-hotkey-win-l-to-lock-windows)。

* [**Vimium**](https://chrome.google.com/webstore/detail/vimium/dbepggeogbaibhgnhhndojpepiihcmeb)：Chromium 内核浏览器的插件，同样遵循于 Vim 的文本编辑哲学——使用主键盘区对浏览器窗口等进行操作。

### 双拼输入法

> 现代中文最优解 - [双拼](https://zh.wikipedia.org/wiki/%E5%8F%8C%E6%8B%BC)

智能拼音输入法的输入效率已经不低于五笔输入（虽然重码率仍有待改善），但是全拼输入有大量无效的击键。双拼输入法的输入哲学在于**尽可能地减少击键次数**。

一个汉字拼音一般可分为声母与韵母。例如，“黄”的拼音是 huang，声母为 h，韵母为 uang。声母与韵母都是有限的，双拼方案正是借助这一点将一切的汉字分为两次击键：声母+韵母。

市面上有众多的双拼输入方法，本文章推荐使用[自然码](https://zh.wikipedia.org/wiki/%E8%87%AA%E7%84%B6%E7%A0%81)或[小鹤双拼](https://baike.baidu.com/item/%E5%B0%8F%E9%B9%A4%E5%8F%8C%E6%8B%BC/6025941)。微软输入法可直接使用前者，后者需要遵循以下教程：

```
1. win + R，输入 regedit，打开注册表
2. 找到 计算机\HKEY_CURRENT_USER\Software\Microsoft\InputMethod\Settings\CHS 项
3. 新建一个名为 UserDefinedDoublePinyinScheme0 的字符串值，值为 
     小鹤双拼*2*^*iuvdjhcwfg^xmlnpbksqszxkrltvyovt
4. 打开控制面板--微软拼音输入法设置，把 小鹤双拼 设置为双拼的默认选择即可。
```

学习方法也非常简单，设置后在 [双拼练习@BlueSky](https://api.ihint.me/shuang/) 中练习半个小时后，再写作一篇千字文章即可达到全拼正常输入速度。后续更加熟悉后，输入速度会大幅度提升。

另：[17 键乱序双拼 - 手机双拼方案](https://www.bilibili.com/read/cv13043066/)。由于手机屏幕过小，容易误触，26 键拼音输入被排除在外。同时，由于九宫格输入重码率过高，也被排除在外。由此衍生出众多手机双拼方案，有 12 键、14 键、17 键的，我个人选择 17 键输入方案。

### 键鼠输入

在许多场景下，纯键盘输入是无法满足我们对鼠标的需求的，例如某个需要精确右击的场景。而这类场景又可在大体上分为：1) 少量鼠标操作；2) 大量鼠标操作。

对于**少量鼠标操作**，我们同样遵循 Vim 文本编辑哲学：尽可能少地离开主输入区。比较简单的解决方案是：[联想的小红点键盘](https://tk.lenovo.com.cn/product/1009664.html)。但是，因为对一根手指过度的依赖，此类键盘不适合大量鼠标操作。

<details><summary>联想小红点键盘 - 图示</summary><img src="https://www.biaodianfu.com/wp-content/uploads/2022/07/red-point.jpg"/></details>

下面提供一个最简略不过的使用教程：

```
- 小红点：摇杆操纵以精确移动
- 类鼠标三键：左键 | 中键 | 右键
- 其他
	- 中键与小红点组合：滚动效果
	- 个人适配：灵敏度调节 & 键帽更换
```

----

对于**大量鼠标操作**，键盘区不再是主要输入手段，而是用作辅助。此类场景常常是：剪辑、作图、设计、娱乐等。由于我并非此类专业领域从事者，故仅仅面向非专业领域鼠标操作（某些处理逻辑适用于专业领域）。

鼠标硬件是此场景的重中之重，长时间使用的舒适感压倒后续所有内容。而舒适感需要考虑到：0) 长时间使用后果；1) 握持手感；2) 重量；3) 续航；4) 可用性（能否自定义等）。考虑到这些，我本人选择的鼠标为：微软的 [Sculpt Ergonomic Mouse](https://www.microsoftstore.com.cn/accessories/ms-sculpt-ergonomic-mouse)。

<details><summary>Sculpt Ergonomic Mouse - 图示</summary>
<div style="display: flex">
<div><img src="https://cdn.microsoftstore.com.cn/media/product_long_description/0436-00000/pdp_image/1.jpg"/></div>
<div><img src="https://cdn.microsoftstore.com.cn/media/product_long_description/0436-00000/pdp_image/2.jpg"/></div>
</div>
</details>
下面针对该鼠标提供操作指南：

```
- 左键 & 右键：普普通通
- 中键：详见 https://sspai.com/post/70372
	- 浏览器中具现化滚动
	- 浏览器中中键点击超链接，打开网页而不跳转
	- 具有标签的软件中，中键关闭标签
	
=== 软件：Microsoft Mouse and Keyboard Center ===
- 侧键（蓝色）：用于关闭标签或软件
	- Basic Settings: Ctrl + W
	- App-Specific Settings: Alt + F4 或 Ctrl + Shift + W
- 侧键（突起）：用于切换软件标签
	- Basic Settings: Ctrl + Tab
```

----

由于 Windows 触控板体验并没有很好，钻研配置的性价比不高。此处仅仅贴出我的简单配置以供参考：

```
- 三指：
	- 点击：中键
	- 上滑：任务视图
	- 下滑：显示桌面
	- 左右滑：应用切换
- 四指：
	- 点击：F11
	- 上下滑：Win + Up/Down
	- 左右滑：桌面切换
```

