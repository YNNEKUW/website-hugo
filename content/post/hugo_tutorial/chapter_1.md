---
title: "Chapter_1"
date: 2022-07-11T14:30:26+08:00
draft: true
---
## Abstract
Hugo 可以用來快速的創建 static website ，好處是我們既可以不用自己寫 HTML 的程式碼，也不用使用 WordPress 或是 Wix 這類幫忙架設網站的付費平台。另外， Hugo 的速度非常快，不像一些傳統的網站架設工具，它是用 Golang 撰寫的（支援 multi-thread）。

## Dynamic Website vs Static Website
- Dynamic Website: 就像是我們平常使用的 Facebook ，不同使用者看到的頁面內容不會相同，此外，當我們按下重新整理之後，可能也會出現不一樣的貼文。若我們要架設這類型的網站可能會需要一些額外的費用，因為我們會需要一個地方來讓我們架設網站，且這類網站的速度會比較慢，因為針對每個不同的使用者，我們會需要為他載入為他量身打造的內容。
- Static Website: 網頁內容是固定的，不同使用者在不同時間前往該網站，看到的內容都會是相同的，按下重新整理之後內容也不會改變。這類型的網站維護起來會相對困難，因為我們會需要把所有的內容都 hardcode 在程式碼裡面，也不會用 conditional logic, functions, or variables 這些平常寫程式常用的東西。此外， Static Webiste 的速度非常快，因為當使用者造訪網站時他們不需要載入任何東西，我們不需要產生任何新的資訊，也不需要連到任何的 Database ，透過 HTTP/HTTPS 即可快速傳送網頁內容給該網站的訪客。
