---
title: "Hugo 架站紀錄 #13 Data Files"
date: 2022-07-16T23:06:57+08:00
draft: false
---
在 `data/` 裡面我們通常會放一些 `.json`, `.yaml`, 或是 `.toml` ，假設我們有一個檔案 `data/states.json`
```json
{
    "AL": {
        "name": "Alabama",
        "capital": "Montgomery",
        "lat": "32.361538",
        "long": "-86.279118"
    },
    "AK": {
        "name": "Alaska",
        "capital": "Juneau",
        "lat": "58.301935",
        "long": "-134.419740"
    },
    "AZ": {
        "name": "Arizona",
        "capital": "Phoenix",
        "lat": "33.448457",
        "long": "-112.073844"
    }
}
```
而在 `layouts/` 中若我們想要取得 `data/` 中的資料，可以使用下列語法
```go
{{ range .Site.Data.states}}
    {{.name}} <br>
    {{.capital}} <br>
{{end}}
```