---
title: "Hugo 架站紀錄 #6 Archetypes"
date: 2022-07-13T17:10:57+08:00
draft: false
---
```
Hugo Website
│   config.toml
└───archtypes
│       default.md
│       subfolder_1.md
│       subfolder_2.md
│
└───content
    │   file_1.md
    │   file_2.md
    │
    └───subfolder_1
    │       file_3.md
    │       file_4.md
    │   
    └───subfolder_2
            file_5.md

```

- `archetypes/default.md` 會包含產生文章時的 front matter 預設值（`title`, `date`, `draft`）
- 若我們想要對 `content/`中不同資料夾客製化不同的 front matter 預設值，可以藉由在 `archetypes/`中建立多個檔案來達成。如 `archtypes/subfolder_1.md` 以及 `subfolder_2.md` 分別會對應到產生在 `content/subfolder_1` 以及 `content/subfolder_2` 中的文章
