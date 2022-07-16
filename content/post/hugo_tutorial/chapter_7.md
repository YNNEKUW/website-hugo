---
title: "Hugo 架站紀錄 #7 Shortcodes"
date: 2022-07-14T00:03:09+08:00
draft: false
categories: ["Hugo"]
---
若要在網頁中插入某些外部資源，可以使用 Hugo shortcodes 來達成，格式如 
```go
{{</* SHORTCODE_NAME parameter_1 parameter_2 */>}}
```
e.g. 
```go
{{</* youtube WRz2MxhAdJo */>}}
``` 
可以鑲入 YouTube 影片，實際結果如下：
{{< youtube WRz2MxhAdJo >}}


**Note**: 後面的 ID 為 YouTube 網址 `=` 後的字串

**Note**: Hugo 官方網站上有各式各樣的 shortcodes 範例可供參考