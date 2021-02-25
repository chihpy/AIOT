# D07 Docker軟體容器平台介紹與安裝使用
###### tags: `homework`
[TOC]
- 作業：安裝Docker，下載映像檔後，建立容器並將實體主機和容器的資料夾互連
## 目標
- 成功安裝 Docker
- 可以從 Docker Hub 下載映像檔到電腦中
- 能夠使用映像檔建立容器
- 連接本機的資料夾和容器中的資料夾
- 使用 docker exec 指令進入到容器中
## 重點
- 了解映像檔(Image)和容器(Container) 之間的關係
- 能夠使用指令進到容器中
## 作業1
- 將此映像檔下載至電腦: alpine
### sol:
- `docker pull alpine`
- [alpine linux](https://hub.docker.com/_/alpine)
## 作業2
- 使用下載的映像檔建立容器，並選定本機中的一個資料夾與容器中的資料夾做連結
- 在本機與容器做連結的資料夾裡建立一個檔案
- 使用指令進到容器內，查看與外部連結的資料夾，即可看到剛剛在本機建立的檔案
### sol:
- `docker run -it -v [host_dir]:[container_dir] alpine:latest /bin/sh`

## 注意事項
- 此映像檔比我們簡報範例使用的 ubuntu 更輕量化，所以在作業的部分我們採用此映像檔做練習，需要注意的是此映像檔並沒有 bash 套件，所以進入容器的指令和簡報介紹的稍有不同，您可以參考以下指令執行進入容器
    - `docker exec -it [container id] /bin/sh`
## reference
- [ ] [sh 和 bash 之間的差異](https://clay-atlas.com/blog/2020/07/08/linux-cn-note-sh-bash-dash-point/)