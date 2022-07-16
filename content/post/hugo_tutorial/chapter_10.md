---
title: "Hugo 架站紀錄 #10 Variables"
date: 2022-07-16T15:54:54+08:00
draft: false
---
## Introduction
以下為常見預設的 variables:
- `{{ .Title }}`: 文章標題
- `{{ .Date }}`: 日期時間
- `{{ .URL }}`: 該網頁的 URL

## Custom Variables

### In Front Matter
我們也可以在 front matter 裡面自己定義 custom variables ，如：
```go
myVar: "myValue"
color: "blue"
```
在 .md 中則是使用：
```go
{{ .Params.myVar }}
```
**Note**: 如果是 custom variables ，需要在前面加上 `.Params`

### In Markdown
用法如下
```go
{{ $myInt := 1}}
{{ $myString := "aString"}}

// To print
{{ $myInt }}
{{ $myString }}

// Use with HTML
<h1>{{ $myInt }}</h1>

// Use with CSS
<h1 style="color: {{ .Params.color}};"> Some text </h1>
```

**Note** 可以到[官方網站](https://gohugo.io/variables/)查看各類 variables 的用法