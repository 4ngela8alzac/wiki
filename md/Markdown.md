---
title: Markdown Manual
tags: []
notebook: Man
---

<a name="top"></a>

# Markdown Manual

[TOC]

## Overview
Markdown is a lightweight markup language with plain text formatting syntax.

## Tool
+ On Windows: Sublime-text/Atom w/ plug-ins, MarkdownPad
+ On Mac: Mou
+ Online: [马克飞象](https://maxiang.io), [作业部落CmdMarkdown](https://www.zybuluo.com/mdeditor)

## Syntax
### 1. 段落
More # ## ### #### ##### ###### for deeper level

Paragraphs are separated by a blank line.

Two spaces at the end of a line leave a   
line break.

Horizontal rule: 

***

---

### 2. 文字样式
_italic_, *italic*, __bold__, **bold**, ***italic&bold***, ~~delete~~, `monospace`, <kbd>ctrl</kbd>, :blush:​

特殊符号转义用 \ 或者 用 \`\`   \`\` 包括

### 3. 列表
Bullet list:
* apples
- oranges
+ pears

Numbered list:
1. apples
2. oranges
3. pears

Checkbox:
- [x] finished
- [x] todo-list 1
- [ ] todo-list 2

### 4. 引用
> How are you
>
>> Fine. Thank you! and you ?
>>
>>> Fine. Thank you!

### 5. 超链接
#### 内联式
This is an [example link](http://example.com/).   
This is an [example link](http://example.com/ "title") with title.

#### 引用式
I prefer [Google][1] to [Yahoo][2], [MSN][3] and [Baidu][]. 
[1]: http://www.google.com/ "Google"
[2]: http://search.yahoo.com/ "Yahoo Search"
[3]: http://search.msn.com/ "MSN Search"
[Baidu]: http://www.baidu.com/ "Baidu"

#### 自动链接
<http://example.com/>
<address@example.com>

#### 脚注
Syntax by John Gruber[^syntax] and Chinese version[^syntax-ch]

[^syntax]: https://daringfireball.net/projects/markdown/syntax 

[^syntax-ch]: http://wowubuntu.com/markdown/#list 

#### 锚点
Take me to [top](#top)

### 6. 图片
#### 内联式
![icon of mou](http://25.io/mou/Mou_128.png)

#### 引用式
![icon of mou][Mou]
[Mou]: http://25.io/mou/Mou_128.png

### 7. 代码框
#### 单行
`function()`

#### 多行
    Markdown is intended to be as easy-to-read and easy-to-write as is feasible.

```python
@requires_authorization
def somefunc(param1='', param2=0):
    '''A docstring'''
    if param1 > param2: # interesting
        print 'Greater'
    return (param2 - param1 + 1) or None

class SomeClass:
    pass

>>> message = '''interpreter
... prompt'''
```

### 8. 表格
| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

### 9. LaTex公式
基于MathJax实现

$E=mc^2$

$\Gamma(n) = (n-1)!\quad\forall n\in\mathbb N$

$$ x = \dfrac{-b \pm \sqrt{b^2 - 4ac}}{2a} $$

### 10. 绘图
基于UML实现

#### 流程图
``` flow
st=>start: Start
e=>end
op=>operation: My Operation
cond=>condition: Yes or No?

st->op->cond
cond(yes)->e
cond(no)->op
```

#### 序列图
```sequence
Alice->Bob: Hello Bob, how are you?
Note right of Bob: Bob thinks
Bob-->Alice: I am good thanks!
```

## Reference
+ Markdown Syntax by John Gruber https://daringfireball.net/projects/markdown/syntax
+ 中文版语法 http://wowubuntu.com/markdown/#list