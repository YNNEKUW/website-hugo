---
title: "Hugo 架站紀錄 #11 Functions"
date: 2022-07-16T17:24:27+08:00
draft: false
---
## Introduction
Functions 只能在 `layouts/` 中使用，不能在 `content/` 中使用。語法如下
```go
{{ funcName param1 param2 }}
```

常見的 functions 及其用法如下
```go
{{ add 1 5 }} // 6
{{ sub 1 5 }} // -4
{{ singularize "dogs" }} // dog

// Range function
{{ range .Page }}
    {{ .Title }} <br> // Print out all titles
{{end}}
```
**Note** 可以到[官方網站](https://gohugo.io/functions/)查看各類 functions 的用法