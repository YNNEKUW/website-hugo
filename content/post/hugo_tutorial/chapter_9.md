---
title: "Hugo 架站紀錄 #9 Template Basics"
date: 2022-07-14T10:13:10+08:00
draft: false
---
## Introduction
前面章節提到的 list page 或是 single page ，它們的背後都有各自的 template ，在沒有任何內容或是刻意做修改的情況下， list page 以及 single page 會有一個預設的格式架構，這就是所謂的 template

```
Hugo Website
│
└───layouts
    │   index.html
    │
    └───_default
    │       list.html
    │       single.html
    │   
    └───subfolder_1
            list.html
            single.html
```

- List Page Template: 如 `layouts/_default/list.html`
- Single Page Template: `layouts/_default/single.html`
- Home Page Template: 如 `layouts/index.html` ， 是 list page 中一個特別的存在，為整個網站的首頁
- Section Template: 如 `layouts/subfoler_1/list.html` ，可以將該 template 只套用在特定資料夾內的檔案而非所有檔案

**Note**: `layouts/` 裡面檔案的優先級比 `themes/` 高

## Base Templates & Blocks
```
Hugo Website
│
└───layouts
    │
    │
    └───_default
            baseof.html
            single.html
            list.html
```
Base template 有點類似繼承的概念，我們會在 `baseof.html` 中定義一些 blocks ，在 `single.html` 以及 `list.html` 中，若我們沒有特別再定義一次這些 blocks ，它就會顯示出 `baseof.html` 中的內容。舉例來說，在 `baseof.html` 中：

```go
<html>
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
    Top of baseof
    <hr>
    {{ block "main" . }}
        This is the default baseof
    {{end}}
    <br>
    {{ block "func1" .}}
        This is the default baseof
    {{end}}
    <hr>
    Bottom of baseof
</body>
</html>
```

若我們沒有在 `list.html` 以及 `single.html` 中特別再寫一次 main 以及 func1 的話，則會看到兩次 **This is the default baseof** 。然而，若我們在 `list.html` 或是 `single.html` 中寫了 main 或是 func1 ，則他會覆蓋 `baseof.html` 中的內容，進而顯示在所有的 list pages 以及 single pages 上，如
```go
{{ define "func1"}}
    This is the single template rather than the baseof
{{end}}
```

以這邊為例， main 的內容會是 `baseof.html` 中的內容，而 func1 的內容則會是 `single.html` 或是 `list.html` 定義的內容