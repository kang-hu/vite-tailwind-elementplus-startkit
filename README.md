# vite-tailwind-elmentplus-startkit

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
