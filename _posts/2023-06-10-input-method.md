---
layout:      post
title:       更高效的输入方式
author:      Ludwig Huang
categories:  other
tags:        [chinese]
image:       typewriter-1.jpg
toc:         false
description: 输入方法论，Vim、双拼输入法简单介绍。
---

### 输入方法论

不同于上个世纪的纸笔写作，本世纪以来的写作方法逐渐演变为：通过键盘与计算机进行交互。然而，此类写作方法对于［本人的］中文写作产生非常强烈的负面影响。中文写作，所写的是**象形符号**“汉字”。在我看来，用纸笔写作时，写前一个汉字的思绪会自然而然地流向下一个汉字，一个句子的逻辑会流向下一个句子。如果写作时文章思路通畅，一篇中文文章会顺理成章地从笔下出现。然而，使用键盘写作的人会丢失这种若隐若现的「写作感觉」。

本篇文章无意于重新拾起纸笔写作的感觉，而希望建立起另一种「写作感觉」。前者来自于“**象形符号**固有的提示性”，后者来自于“**迅速**输入以抓住转瞬即逝的灵感”。**迅速**来自于熟练的输入经验（例如标准指法、盲打等），以及硬件、软件上的适配。

本文介绍的是：软件上的适配。

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

