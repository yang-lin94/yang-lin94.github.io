# 0.Docker 前言


最近再網路上看到了 Docker ,也想來學一下,也透過己篇文章來紀錄自己的學習筆記。

## 會想學 Docker 的原因，以及 Docker 的優點

1. 可以省去會因本`地作業系統`的版本 、`機器核心`的不同 、`環境變數`沒設定 or 設正確等……的問題。倒置 server 無法正常啟動 ,還需花時間再前其的佈署上

2. 再程式撰寫中 ,需再不同的版本中境行測試寫的 Code 是否能夠正常再 server 執行 , 需要反覆的安裝和解除安裝 ,可以能會因為沒有解除安裝完成或舊版檔案還在而造成 server 無法啟動

3. 如果有開發一個開源專案 ,希望給很多人使用 , 那就需要一個簡單的安裝方式, Docker 可以把開法完的程式打包程 image 上傳到 Docker Hub 上 ,其他人如果需要使用只需 download , 打上幾行 command 就可以讓程式跑起來

> 再查 Docker 的時候也有查到可以使用 VM 的方式 ,那為什麼以上那些還是比較推荐 Docker 呢？

## VM 和 Docker 的差異

### VirtualBox

- 需要先有 iso 檔
- VM 裡面的作業系統開機需要花一點時間等開機
- 完全的把系統的硬體資源隔離
- 佔用較多的硬碟容量

### Docker

- 直接從 Docker Hub Pull 作業系統的 Image
- 不用等開機，啟動速度比 VM 更快
- 底層還是使用本地作業系統的核心
- 佔用較少的硬碟容量

> Docker 和 VM 都有各自的使用場景 ,還可以搭配來使用 ,如果需要使用完整的作業系統可以使用 VM 安裝作業系統再使用 Docker 啟動需跑的 container

## 預計會紀錄的 Docker 內容

- Docker 架構和安裝
- Docker command 的介紹
- Dockerfile 的撰寫
- Docker Hub 和 Docker Registry 的使用
- Docker 的管理工具

