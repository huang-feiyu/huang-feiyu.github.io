---
layout:      post
title:       标点与符号说明
author:      Ludwig Huang
categories:  other
tags:        [chinese]
image:       paper-1.jpg
---

### 标点说明

> 中文文章不区分全角或半角，采用微软输入法默认的标点形式。

> Punctuation mark used in English articles generally can be able to be typed directly via keyboard.

* 冒号 **：**：用于提示性词语后，提示下文；总结上文；用在需要说明的词语后，表示注释和说明
* 分号 **；**：并列关系；非并列关系间的停顿，主要是选择、转折等关系；分项列举
* 破折号 **——**：标示注释内容或补充说明；标示插入语；总结上文或提示下文；标示话题的转换；标示引用内容来源
* 半引号 **「」**：标示特殊名词或术语
* 半空引号 **『』**：标示特殊名词或术语，用于「」内部<sup>[1]</sup>
* 方括号 **［］**：对正文的补充或订正；国际音标/古文注音

注释：

* [0]：微软输入法使用特殊字符的教程 - [telegram comment](https://t.me/huangblog/31?comment=110)
* [1]：正确用法为『』为第一层，类似于《》第一层。但是，本博客不再以其为第一层，而是以「」为第一层。

### 符号说明

**上角标与下角标：**

* 上角标：对某个 词语 或 整段话 进行简要注解<br><br>
  *例*：nostalgia<sup>乡愁</sup>
* 下角标：画外音<br><br>
  *例*：您是不是讲过，您不知道在一桩兽性的淫行和任何丰功伟绩，即使是为人类牺牲性命之间，从美的角度来看有何区别？您是不是在这两种极端相反的行为中发现了相通的美，找到了同样的快感？<sub>背弃良知的狂想</sub>

**引用：**

* 中文：使用书名号标记<br><br>
  *例*：[《宗教大法官》](https://huangfeiyu.blogspot.com/2021/08/blog-post.html)
* 英文：使用斜体<br><br>
  *例*：[*Valentine's Day*](https://youtu.be/teBSOhu93sg)

**它、他、她、祂：**

* 它：非人性化的他者
* 他：男性的他者
* 她：女性的他者
* 祂：神圣化的他者<br><br>
  *例*：[旧日支配者](https://zh.wikipedia.org/w/index.php?title=%E5%85%8B%E8%98%87%E9%AD%AF%E7%A5%9E%E8%A9%B1&oldformat=true&variant=zh-cn#%E8%88%8A%E6%97%A5%E6%94%AF%E9%85%8D%E8%80%85%EF%BC%88Great_Old_Ones%EF%BC%89)
* Ta：表示无性别的人类<br><br>
  *另*：TA: [Teaching Assistant](https://en.wikipedia.org/wiki/Teaching_assistant)
* 它们：一切“它”的集合
* 他们：宽泛的人性化的他者集合
* 她们：仅在强调“他们”全部为**女性**时使用

---

### Other

> 不太常用的 HTML/Markdown 元素.

##### Tables

Title 1               | Title 2               | Title 3               | Title 4
--------------------- | :-------------------: | :-------------------- | --------------------:
lorem                 | lorem ipsum           | lorem ipsum dolor     | lorem ipsum dolor sit
lorem ipsum dolor sit | lorem ipsum dolor sit | lorem ipsum dolor sit | lorem ipsum dolor sit
lorem ipsum dolor sit | lorem ipsum dolor sit | lorem ipsum dolor sit | lorem ipsum dolor sit
lorem ipsum dolor sit | lorem ipsum dolor sit | lorem ipsum dolor sit | lorem ipsum dolor sit

##### Embedding

Plenty of social media sites offer the option of embedding certain parts of their site on your own site, such as YouTube:

<iframe width="560" height="315" src="https://www.youtube.com/embed/744DJ3OAcOQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

##### MathJax Example

The [Schrödinger equation](https://en.wikipedia.org/wiki/Schr%C3%B6dinger_equation) is a partial differential equation that describes how the quantum state of a quantum system changes with time:

$$
i\hbar\frac{\partial}{\partial t} \Psi(\mathbf{r},t) = \left [ \frac{-\hbar^2}{2\mu}\nabla^2 + V(\mathbf{r},t)\right ] \Psi(\mathbf{r},t)
$$

[Joseph-Louis Lagrange](https://en.wikipedia.org/wiki/Joseph-Louis_Lagrange) was an Italian mathematician and astronomer who was responsible for the formulation of Lagrangian mechanics, which is a reformulation of Newtonian mechanics.

$$ \frac{\mathrm{d}}{\mathrm{d}t} \left ( \frac {\partial  L}{\partial \dot{q}_j} \right ) =  \frac {\partial L}{\partial q_j} $$


### Code and Syntax Highlighting

Markdown code blocks:

```ruby
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
```

js native `{% highlight go%} {% endhighlight %}`:

{% highlight go %}
package main

import (
    "fmt"
)

func main() {
    fmt.Printf("Hello, World!")
}
{% endhighlight %}
