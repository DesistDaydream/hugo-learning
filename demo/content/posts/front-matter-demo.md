---
title: "FrontMatter 示例"
date: 2023-05-24T13:50:25+08:00
description: >
  本节页面的简短引导描述。作用于 .Description 变量
---

这是我的第一篇文章，我想要展示一些 Hugo 的特性。

这是我的网站的描述：{{ .Site.Params.description }}

这是我的网站的作者：{{ .Site.Params.author }}

这是我的文章的标题：{{ .Title }}

这是我的文章的日期：{{ .Date.Format "2006-01-02" }}

这是我的文章的分类：{{ range .Params.categories }}{{ . }} {{ end }}

这是我的文章的标签：{{ range .Params.tags }}{{ . }} {{ end }}

这是一张图片：![Hugo Logo](/images/hugo-logo.png)

这是一个链接：[Hugo 官网](https://gohugo.io/)

这是一段代码：

```go
package main

import "fmt"

func main() {
  fmt.Println("Hello, Hugo!")
}
