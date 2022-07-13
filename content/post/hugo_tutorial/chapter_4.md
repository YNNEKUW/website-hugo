---
title: "Hugo 架站紀錄 #4 Creating & Organizing Contents"
date: 2022-07-13T11:23:37+08:00
draft: false
---
## Create New Post
在 Hugo Website 的資料夾中執行
```bash
hugo new --kind content/post/YOUR_FILE_NAME.md
```
即可產生一份新的 .md ，這份檔案會是我們撰寫文章內容的地方

## Preview the Website
創建完檔案後，若想要在網站正式上線前先預覽，可以執行
```bash
hugo server -D
```
接著用瀏覽器打開`localhost:1313`即可預覽

**Note**: `-D` 可以讓我們用開發者模式預覽網站，每篇被新增的 .md 最上方一開始都會有 `draft=true` ，若沒有加上 `-D` 則無法看到這些草稿

## List Page vs Single Page
```
Hugo Website
│   config.toml
│   archtypes
│   layouts
│   ...
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
我們使用指令創建的 .md 為 Single Page ，而這些放在 `/content`裡面的 Single Page 也可以被放在各種 subfolders 下面，以便做歸納與整理。

至於 List Page ，則是 Hugo 自動創建出來的。舉例來說，打開瀏覽器輸入：
- `localhost:1313`: 會進入網站主頁，可以看到所有貼文
- `localhost:1313/subfolder_1/`: 可以看到 `file_3` 與 `file_4` 兩則貼文
- `localhost:1313.subfolder_2/`: 因為 `subfolder_2` 下面只有一個檔案， Hugo 預設是不會產生 List Page 的，若希望這邊能產生一頁 List Page ，必須要手動設定

> Create list page manually :
>
> ```bash
> hugo new content/subfolder_2/_index.md
> ```

**Note**: 在 `_index.md` 裡面可以任意加上內容，這些內容會被呈現在 List Page 的頁面中

**Note**: 這個方法也可以用來覆寫那些被自動創建出來的 List Page (e.g. `subfolder_1`)

**Note**: 某些 theme 會對於 `content` 內部的資料夾做一些規定，要求 .md 必須放在特定位置 （e.g. content/post/)