---
title: "Chapter_2 (Directory Structure)"
date: 2022-07-11T23:31:37+08:00
draft: false
---
## Bais Architecture
```console
hugo new site YOUR_SITE_NAME
```
透過這個指令可以先創造出基本的資料夾，資料夾內部則會包含：
- ```/archetypes```: 裡面用來存放網站的 metatdata ，對於初心者來說不太會用到這個資料夾裡面的東西
- ```/content```: 網站的貼文、文章等等都會存放於此
- ```/data```: Static Website 雖然不會有 database ，但如我我們有大筆資料（e.g. .json) 需要被網站內容存取，一般來說會放在此資料夾
- ```/layouts```: 若我們要對網站做一些排版的工作，會將程式碼放在這，如我們想要在每個頁面加上 header 或 footer 等等
- ```/static```: 有些固定不會變更的檔案，如不同篇貼文都會使用到或讀取到的檔案，則會被放在這邊 (e.g. image, CSS files, JavaScript files...)
- ```/themes```: 一般來說要使用 Hugo 創建一個個人網站時，我們不會想要從頭開始處理排版這些瑣碎的事，而是會套用別人已經做好，現成的主題。 Hugo 的網站上有提供各式各樣的 themes 可供下載、使用
- ```config.toml```: 可以被視為網站的設定檔，就像 iPhone 裡面的 Settings 一樣

## Summary
雖然這邊提及了數個資料夾，但對於最基本的使用者來說，只要知道 ```/content``` 以及 ```/themes``` 就可以做出網站了