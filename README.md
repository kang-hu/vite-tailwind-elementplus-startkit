# AT後台專案-google-dashboard

### 簡介

前端以Vite`(發音[veet]，在法語中是輕量、輕快的意思)`，進行開發和打包實現前後端分離。
搭配elementplus 和 tailwind進行實作

### 檔案結構

```
project/                           // 專案全資源 config root資料夾
project/ packages.json             // 前端開發環境相關設定
project/ vite.config.js            // vite開發及打包的設定
Dockerfile                         // 負責產出環境image，install完packages
docker-compose.yml                 // 負責啟動服務執行腳本
```

```
project

- src
  |-- assets
  |-- router
  |-- stores
  |-- services
  |-- styles
  |-- components
  |-- pages //各別頁面
  |   |-- index //各頁面入口資源
  |       |-- App.vue
  |       |-- index.js
  |       |-- index.scss
- package.json
- tailwind.config.js
- postcss.config.js
- vite.config.js
- index.html
- .gitignore
```


### 開發環境：Docker及設定說明介紹

Dockerfile 用含 node.js 的 image 產生安裝好 node_modules 共用 image，使用者自行啟動自己的 container server

1. 172.31.0.198使用個人AD帳號 172.31.0.223 需要管理員打開Docker個人權限設定 // 開過請省略至 2.
2. 一般開發參考 6.，啟動/關閉開發機
3. Node.js 需要更新時，重新pull node image 更新 Dockerfile 重製 image
4. packages.json 需要更新時，Dockerfile，重新build image，更新 docker-compose.yml
5. image 需要更新時，docker-compose.yml也要注意對應
6. docker-compose up down 預設執行 yarn run dev
    > 需要測試可以修改 docker-compose.yml 或進入 container 內進行指令

* 指令

```
$ COMPOSE_PROJECT_NAME=<name> docker-compose up -d  // 啟動Container
$ COMPOSE_PROJECT_NAME=<name> docker-compose down -v  // 關閉Container
    -d , --detach : 讓 Container 處於背景執行狀態並印出 Container ID
    -v, --volumes : 移除volumes
$ docker build -t repo_name:tag_name . //建立image
    --tag , -t // Name and optionally a tag in the 'name:tag' format
$ docker images //查現有image
$ docker image rm <repo:tag> // 移除image
$ docker ps //查詢執 行中的container
$ docker exec -it <container> /bin/sh
    -i , --interactive : 讓 Container 的標準輸入保持打開
    -t , --tty : 讓Docker分配一個虛擬終端（pseudo-tty）並綁定到 Container 的標準輸入上
```

### 未完待續
test
