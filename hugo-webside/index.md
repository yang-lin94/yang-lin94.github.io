# Hugo建立部落格/網站


<!-- <a href="https://imgur.com/OzTCuYT"><img src="https://i.imgur.com/OzTCuYT.png" title="source: imgur.com" /></a> -->

## 一.Hugo 是什麼

> Hugo 是用 go 語言開發的靜態網站的生產器 (Static Site Generator)，有快速的架站速度和高靈活性。

## 二.安裝

Hugo 有很多安裝方式，有 Windows/macOS/Linux，這裡主要介紹 Window 和 macOS 的安裝方法，其他安裝方法請直接到[官網](https://gohugo.io/getting-started/installing)查詢。

### 1.Scoop (Windows)

```cmd
scoop install hugo
scoop install hugo-extended
```

### 2.Homebrew (macOS)

```bash
brew install hugo
```

### 3.透過 github release 下載

下在網站的 [release](https://github.com/gohugoio/hugo/releases) 選擇自己電腦的最新版本，例如:**hugo_0.76.5_Windows-64bit.zip**下載解壓縮，建立 Blog 的資料夾，將 hugo.exe 放入目錄中

### 4.環境變數

啟動環境變數

快捷鍵：`win + R`

輸入：`rundll32.exe sysdm.cpl,EditEnvironmentVariables`

對 PATH 編輯，新增 > 輸入 `hugo.exe` 所在的目錄 > 確定

### 5.安裝確認

開啟命列提示字元 CMD

快捷鍵：`win + R`

輸入 `hugo version`

如有顯示版本代表安裝成功

### 6.建立網站

hugo new site 資料夾名稱
這樣就完成一個簡單的 hugo 網頁啦。

## 三.選擇主題

### 1.下載主題

本人使用 LeaveIt hugo 的主題。

Hugo 沒有預設主題需到[官網 Themes](https://themes.gohugo.io/) 下載。

使用 `git clone` 下載

切換到建立好的網站資料夾底下

下載指令

cd wibside
git init
git submodule add <https://github.com/liuzc/LeaveIt.git>
沒有也沒關係，下載 [LeaveIt Themes](https://github.com/liuzc/LeaveIt/archive/master.zip) 後解壓縮。

到 **themes\LeaveIt**，刪除.git 隱藏資料夾

開啟隱藏項目,打勾 隱藏的項目

將 **LeaveIt/exampleSite** 內的資料複製到根目錄資料夾

根目錄資料夾的 `config.toml` 蓋掉掉

注意：config 資料夾為設定檔

### 2.編輯 config.toml 將主題設為 LeaveIt

開啟 config.toml 輸入

`theme = "LeaveIt"`

## 四.啟動 Hugo 網頁

需再根目錄執行 `hugo server -D`

網頁上輸入：<http://localhost:1313/>

此時你就會發現你的網頁已經啟動了

## 五.資料夾結構

content 文章、頁面
static 圖片、影片之類的
themes 主題
data 讓頁面讀取資料，如 json 檔
layouts 修改主題的地方
詳細內容請參考[官方檔案](https://gohugo.io/content-management/organization/)

## 六.建立文章

文章建立指令：**hugo new content\zh\文章名稱.md**

## 1.文章默認語法

title: 文章名稱
date: 日期 ex:2020-07-07
draft: 草稿 ex:true/false
author: 作者名稱
description: 描述內容
url: /自訂網址
image: /圖片
categories: 設定分類 ex:["abc","edf"]
tags: 設定 tag 標籤 ex:["abc","def"]

---

這些設定都會在文章生成後自動產生，不必在複製貼上，有需也可以加上自己想要的內容。

### 2.圖片放置位置

素材需放在 static 資料夾內

static/images

圖片網址會是 <http://localhost:1313/images/abc.jpg>

圖片也可使用 url 的方式。

[imgur 免費圖片空間 註冊&教學](https://yang-lin94.github.io/free-image-space-imgur/)

## 七.部屬

當網站完成後，產生靜態檔案到 `public` 資料夾下並部屬到遠端主機上。

各平台部署方式[參考](https://gohugo.io/hosting-and-deployment/)。

## 八.相關文章

- [Hugo 使用 Likecoin 教學](https://yang-lin94.github.io/hugo-likecoin/)

- [imgur 免費圖片空間 註冊&教學](https://yang-lin94.github.io/free-image-space-imgur/)

