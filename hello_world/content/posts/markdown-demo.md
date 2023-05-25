---
title: "Markdown 示例"
linkTitle: "Markdown 示例"
date: 2023-05-25T13:50:25+08:00
description: >
  本节页面的简短引导描述。这里的文字也可以是 **粗体** 或 _斜体_，甚至可以分成多个段落。
---

# 概述

第一个段落。文字可以是 **bold(粗体)** 、 _italic(斜体)_ 或 ~~strikethrough(删除线)~~。[Links(链接)](https://gohugo.io) 应该是蓝色的，没有下划线 (除非悬停在上方)。

第二个**段落**。

## 第一个二级标题

这是一个标题后面普通的段落。

亲爱的植物和大地，即使你们沉默不变，也请听我说。我被召唤并教授了飞行技能，但我并没有（羽毛和线）这样的供应。

## 第二个二级标题

> 这是一个标题后面的 blockquote(引用) 格式. 应该与标题中间空出一行。

### 三级标题

```bash
这是一个 code block(代码块)。
```

代码块后的段落，跟普通段落也没啥区别

#### 四级标题

##### 五级标题

###### 六级标题

# 引用

> 引用第一行

# unordered list(无序列表)

- Liverpool F.C.
- Chelsea F.C.
- Manchester United F.C.

# ordered list(有序列表)

1. Michael Brecker
2. Seamus Blake
3. Branford Marsalis

# unordered task list(无序任务列表)

- [x] Create a Hugo theme
- [x] Add task lists to it
- [ ] Take a vacation

# 混合任务列表

- [ ] Pack bags
- ?
- [ ] Travel!

# nested list(嵌套列表)

- 第一行
  - 一级缩进
    - 二级缩进
  - Tito
  - Jackie
  - Marlon
  - Jermaine
- TMNT
  - Leonardo
  - Michelangelo
  - Donatello
  - Raphael

定义列表可以使用 Markdown 语法。定义头部是加粗的。

Name
: Godzilla

Born
: 1952

Birthplace
: Japan

Color
: Green

----------------

# 表格

| Artist            | Album           | Year |
|-------------------|-----------------|------|
| Michael Jackson   | Thriller        | 1982 |
| Prince            | Purple Rain     | 1984 |
| Beastie Boys      | License to Ill  | 1986 |

表格过宽的效果

| Artist            | Album           | Year | Label       | Awards   | Songs     |
|-------------------|-----------------|------|-------------|----------|-----------|
| Michael Jackson   | Thriller        | 1982 | Epic Records | Grammy Award for Album of the Year, American Music Award for Favorite Pop/Rock Album, American Music Award for Favorite Soul/R&B Album, Brit Award for Best Selling Album, Grammy Award for Best Engineered Album, Non-Classical | Wanna Be Startin' Somethin', Baby Be Mine, The Girl Is Mine, Thriller, Beat It, Billie Jean, Human Nature, P.Y.T. (Pretty Young Thing), The Lady in My Life |
| Prince            | Purple Rain     | 1984 | Warner Brothers Records | Grammy Award for Best Score Soundtrack for Visual Media, American Music Award for Favorite Pop/Rock Album, American Music Award for Favorite Soul/R&B Album, Brit Award for Best Soundtrack/Cast Recording, Grammy Award for Best Rock Performance by a Duo or Group with Vocal | Let's Go Crazy, Take Me With U, The Beautiful Ones, Computer Blue, Darling Nikki, When Doves Cry, I Would Die 4 U, Baby I'm a Star, Purple Rain |
| Beastie Boys      | License to Ill  | 1986 | Mercury Records | noawardsbutthistablecelliswide | Rhymin & Stealin, The New Style, She's Crafty, Posse in Effect, Slow Ride, Girls, (You Gotta) Fight for Your Right, No Sleep Till Brooklyn, Paul Revere, Hold It Now, Hit It, Brass Monkey, Slow and Low, Time to Get Ill |

----------------

代码还可以使用语法高亮。

```go
func main() {
  input := `var foo = "bar";`

  lexer := lexers.Get("javascript")
  iterator, _ := lexer.Tokenise(nil, input)
  style := styles.Get("github")
  formatter := html.New(html.WithLineNumbers())

  var buff bytes.Buffer
  formatter.Format(&buff, style, iterator)

  fmt.Println(buff.String())
}
```

表格单元格内的内联代码

| Language    | Code               |
|-------------|--------------------|
| Javascript  | `var foo = "bar";` |
| Ruby        | `foo = "bar"{`     |

----------------

小图片应该按照它们的实际大小显示。

![](https://upload.wikimedia.org/wikipedia/commons/thumb/9/9e/Picea_abies_shoot_with_buds%2C_Sogndal%2C_Norway.jpg/240px-Picea_abies_shoot_with_buds%2C_Sogndal%2C_Norway.jpg)

大图片应该始终缩小并适应内容容器。

![](https://upload.wikimedia.org/wikipedia/commons/thumb/9/9e/Picea_abies_shoot_with_buds%2C_Sogndal%2C_Norway.jpg/1024px-Picea_abies_shoot_with_buds%2C_Sogndal%2C_Norway.jpg)

_上面的照片是挪威云杉的枝条和叶芽。照片作者为Bjørn Erik Pedersen，采用CC-BY-SA许可。_

# 测试页面跳转

- [带空格的 页面](/docs/入门指南/带空格的%20页面.md)
- [大小写字母](</docs/入门指南/Aa Bb.md>)
- [URL空格、大小写字母、标题空格](</docs/入门指南/Aa Bb.md#标题二 带空格>)
- [带括号、空格](/docs/入门指南/Ab(Cd).md)
