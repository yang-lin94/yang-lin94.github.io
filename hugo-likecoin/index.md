# Hugo使用Likecoin教學


## 一.什麼是 Likecoin

Likecoin 是什麼? 它是它是一種虛擬貨幣，是以太坊區域鍊延伸出來的，透過點讚，轉化成優質創作者的實質贊助，並且擁有去中心化的特性。

[去中心化](https://zh.wikipedia.org/wiki/%E5%8E%BB%E4%B8%AD%E5%BF%83%E5%8C%96)是什麼? 簡單來說，就是將中央處理中心移除，透過點對點的方式進行交易，讓帳本公開給每個人。

**詳細說明請參考 LikeCoin 的 [計畫介紹白皮書](https://like.co/in/whitepaper)**

## 二.如何在 Hugo 上插入 Likecoin

Hugo 可以透過自訂 layouts 的方式，再不改變網頁原先的設計，在我們的每篇文章下插入 Likebutton。

先將目錄切到 themes 的 layout 資料夾下。

**/cd theme/your_theme/layouts/**
使用 Hugo 中的 Partial 的功能，建立模板在網頁中。 在 layouts 裡的 partials 資料夾中建立 likecoin.html，並寫入以下內容。 寫在要給讀著看的位置。 [參考資料](https://gohugo.io/templates/partials/)。

```html
<iframe
  class="LikeCoin"
  height="235"
  src="https://button.like.co/in/embed/{{ .Site.Params.likerID }}/button?referrer={{ .Permalink }}"
  width="100%"
  frameborder="0"
></iframe>
```

接下來在 `config.toml` 中加入

[[params]]
`likerID = "your liker id`"
接著編輯文章的模板，默認位置通常在`\_default/single.html`。 接著在你想插入 Button 的地方寫上以下內容。

`{{ partial "likecoin.html" . }}`
記得執行 **hugo server** 預覽你的網站

最後執行 hugo 在部屬到 github 上即可

## 三.相關文章

[Hugo 建立部落格/網站](https://yang-lin94.github.io/hugo-webside/)

