## 新世代的框架庫需求--文檔
一個完整的開源庫必須包含
* 文檔
* 好的編譯需求
* 規範
* 測試
* 持續集成
* 其他內容()

### 文檔
一個開源代碼庫除了代碼效能好，開發者用的順手，最重要的就是要讓開發人員簡單的看懂，
因此文黨非常重要。
而一個項目的文檔包刮:
1. README.md
   - README是一個項目的門面，應該簡單明了的呈現用戶最關心的問題，一個開源庫的用戶包括使用者和貢獻者，所以一個文檔應該包括項目簡介，使用者指南，貢獻者指南三部分
  項目簡介用該簡單介紹項目功能，使用場景，兼容性的相關知識，這裡重點介紹下徽章，相信大家都見過別人項目中的徽章，如下所示
  </br>
  
  ![VueReadme](https://raw.githubusercontent.com/tp953704/IT-Contest/master/img/vuereadme.png)
  
  
2. TODO.md
   - TODO應該記錄項目的未來計劃，這對於貢獻者和使用者都有很重要的意義，下面是TODO的例子
   </br>
   
   ```   
    - [X] 已完成
    - [ ] 未完成
    ```
  
3. CHANGELOG.md
   - CHANGELOG記錄項目的變更日誌，對項目使用者非常重要，特別是在升級使用版本時，CHANGELOG需要記錄項目的版本，發版時間和版本變更記錄
   
   </br>
   
   ![VeturChangelog](https://raw.githubusercontent.com/tp953704/IT-Contest/master/img/vetur.png)
   
4. LICENSE
   - 開源項目必須要選擇一個協議，因為沒有協議的項目是沒有人敢使用的，關於不同協議的區別可以看下面這張圖（出自阮老師博客），建議是選擇MIT或者BSD協議
   
   </br>
   
   ![阮老師博客](https://raw.githubusercontent.com/tp953704/IT-Contest/master/img/ke8qottjwo.png)
   
5. doc
   - 開源項目還應該提供詳細的使用文檔
   - 可以去閱讀 裡面有很詳細的介紹
     - (https://devdocs.io/jsdoc/)
