---
title: "Hugo 架站紀錄 #12 If Statements"
date: 2022-07-16T20:11:54+08:00
draft: false
---
條件式基本的用法如下
```go
{{ $var1 := "dog" }}
{{ $var2 := "cat" }}

{{ if eq $var1 $var2 }}
    True
{{else}}
    False
{{end}}
```
與一般的程式語言不同，這邊需要把 operator 放在變數的最前面。此外，如果要用複數個條件式，範例如下
```go
{{ $var1 := 1 }}
{{ $var2 := 2 }}
{{ $var3 := 3 }}

{{ if and (lt $var1 $var2) (lt $var1 $var3) }}
    Text1
{{else if and (lt $var2 $var1) (lt $var2 $var3)}}
    Text2
{{else}}
    Text3
{{end}}
```

也可以搭配其他的 functions 使用（當點擊到某篇貼文時標題的背景顏色會改變）
```go
{{ $title := .Title }}
{{ range .Site.Pages }}
    <li><a href="{{ .URL }}" style="{{ if eq .Title $title }} background-color:yellow;{{end}}">{{ .Title }}</a></li>
{{end}}
```