# Vue-export-MicroSoft-Word-file

export word file 會用到以下套件，下表為套件評估:

套件名稱                          |   功能                                                |npm週下載次數 | 最後更新時間| 備註
---------------------------------|-------------------------------------------------------|-------------|------------|--------------------------------------------------------------------------------------
docxtemplater                    |  依據本地端的word範本格式，將網頁資料匯出成文字或表格資料  |  31,142     |  23天前    |需標註MIT License 。 網站: https://docxtemplater.com/
docxtemplater-image-module-free  |  將網頁圖片轉入word檔案中                               |  1,175      |  3年前     |此套件付費版，週下載人次為6人，最後更新時間為半年前，但須購買950€/年的方案才能用。免費版則需標註MIT License
JSZip                            |  處理壓縮檔                                            |  4,141,241  |  7個月前   |需標註MIT License
JSZipUtils                       |  搭配JSZip使用的跨瀏覽器工具                            |  56,510     |  3年前     |需標註MIT License
file-saver                       |  前端檔案下載                                          |  1,414,030  |  1年前     |需標註MIT License

評估後認為，套件皆有一定使用人數，且主要的docxtemplater及JSZip都有在持續維護，因此有一定安全性。



使用此套件組，需要在專案的public資料夾內，設置word範本檔案，在word範本檔內先規劃好排版及文字格式樣式後，再於程式中匯入相應的資料。word範本格式請參考本專案範本或是以下連結: 
<br>
1. https://docxtemplater.com/docs/tag-types/ 
2. https://local.blog.csdn.net/article/details/108246098?spm=1001.2101.3001.6650.2&utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-2.pc_relevant_default&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-2.pc_relevant_default&utm_relevant_index=4

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
