---
title: "Hugo 架站紀錄 #5 Front Matter"
date: 2022-07-13T16:13:53+08:00
draft: false
---
Front matter 又可以叫做 metadata ，當我們新建立了一則貼文，它會出現在 .md 的最前面，用來描述該篇貼文的資訊、細節。 front matter 可以用三個語言來撰寫：
- YAML: 用 `---` 上下包住，中間的 key value pair 則是用 `:`
- TOML: 用 `+++` 上下包住，中間的 key value pair 則是用 `=`
- JSON

網站的訪客在點進去該篇文章之前可以看到這些 front matter ，而 front matter 的內容我們也可以依需求來做增減（e.g. author, language, ...）