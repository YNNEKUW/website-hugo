---
title: "Hugo 架站紀錄 #3 Installing & Using Themes"
date: 2022-07-12T16:40:14+08:00
draft: false
---
## Introduction
上一章節說到，我們通常不會自己從頭開始設計網站，而會選擇套用別人做好的 themes ，我們可以前往[**官方網站**](https://themes.gohugo.io/)挑選自己喜歡的款式，點進去後點選 **Download** 就可以進到該主題的 Github repo ，這邊介紹三種安裝 theme 的方法

### Method 1
在 Hugo Website 的資料夾中執行
```bash
git clone https://github.com/YOUR_HUGO_THEME themes/YOUR_HUGO_THEME --depth=1
```

**Note**: 這邊可以在上述 command 的末端加上 ` --branch v1.0` 來指定想要下載的 themes 的版本
**Note**: ```depth=1``` 可以讓我們從特定的一個 branch 只抓取最新的一個 commit (default: master branch)

> Updating theme :
>
> ```bash
> cd themes/YOUR_HUGO_THEME
> git pull
> ```

### Method 2
可以使用 [submodule](https://www.atlassian.com/git/tutorials/git-submodule) 來安裝
```bash
git submodule add --depth=1 https://github.com/YOUR_HUGO_THEME.git themes/YOUR_HUGO_THEME
git submodule update --init --recursive # 可以 recursively 的更新 submodule (某些 submodules 裡面可能還有包含其他的 submodules)
```

**Note**: 這邊可以在上述 command 的末端加上 ` --branch v1.0` 來指定想要下載的 themes 的版本
**Note**: 可以使用 `git rm PATH_TO_YOUR_HUGO_THEME` 來移除不要的 Hugo Theme

> Updating theme :
>
> ```bash
> git submodule update --remote --merge
> ```

### Method 3
選取好 Hugo Theme 後，進到作者的 GitHub repo ，點選右上角的下載，將下載完成的 .zip 放到 `/themes` 資料夾中解壓縮即可

### Finally...
在 `config.toml` 中加入一行
```toml
theme = 'YOUR_HUGO_THEME'
```