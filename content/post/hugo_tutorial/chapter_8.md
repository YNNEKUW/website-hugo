---
title: "Hugo 架站紀錄 #8 Taxonomies"
date: 2022-07-14T00:25:40+08:00
draft: false
categories: ["Hugo"]
---
## Default Taxonomies
在 front matter 中可以加入一些 keywords 來幫助我們對網站上的文章做分類，最常見的 taxonomies 當屬 `tags` 以及 `categories` ，語法如下：
```yaml
tags: ["tag1", "tag2"]
categories: ["cat1", "cat2"]
```
這邊的 `tags` 以及 `categories` 種類以及數量可以隨個人喜好做改變。如此一來，當訪客造訪網站時只要點選某個 tag 或是某個 category ，即可看到包含該 tag 或是屬於該 category 的所有文章

**Note**: 有些 theme 的設計可能不會把 `tags` 以及 `categories` 顯示出來，若要使用這個功能還需要做一些調整

## Custom Taxonomies
除了預設的 taxonomies ，使用者可以自行定義，但必須要在 `config.toml` 中加入一些程式碼，比如說我們想要自行加入 `mood` 這個 taxonomy:
```toml
[taxonomies]
  tag = "tags"
  catetory = "categories"
  mood = "moods"
```

**Note** 即便 `tags` 與 `categories` 是 Hugo 預設的 taxonomies ，我們在沒有對 `config.toml` 做更動就可以使用，然而一旦我們加入 custom taxonomies ，就需要把這些預設的 taxonomies 一併加入才行

**Note** 同上，有些 theme 不會顯示出 custom taxonomies