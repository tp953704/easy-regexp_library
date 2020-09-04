## npm介紹

### npm 做甚麼??
- 在線存儲庫的Node.js包/模塊，可搜索 search.nodejs.org
- 命令行實用程序來安裝Node.js的包，做版本管理和Node.js包依賴管理。


### npm常用指令

1. 專案初始化
利用 npm 指令，可以協助我們建立 Node.js 專案的描述檔，或稱為初始化專案，命令如下：
`
//協助我們建立 Node.js 專案的描述檔
npm init
`
在打入 npm init 後，會被要求輸入幾個欄位

```

package name: 你這個 Project 要叫什麼名字
version: 你決定這個 Project 現在該是第幾版
description: Project 基本介紹
entry point: 進入點，如果要跑你的 Project 應該要執行哪個檔案
author: 作者(自己)
license: 你這個 Project 是採用什麼授權的
test command: 這個不太重要，待會會說明

```

基本上結束後，你可以看到這個資料夾底下，新增了一個 Package.json

2. 安裝第三方套件
npm install <套件名稱>

3. npm常用縮寫

#### 補充 npm ci vs npm i 
有時我們輸入npm i 的時候 Npm會幫我們做小更新，(邪惡的npm 怒)，
因此在專案執行期間，我們會以npm ci來代替npm i，以避免某個套件新，照成其他套件的不相容。

```
//是npm install 的縮寫
npm i // npm ci

//是npm install -save
npm i -S

//是npm install -save-dev
npm i -D  

```
4. save 與 save-dev
   - save 
   
   > 在 package.json裡，分別是指到 dependencies 與 devDependencies 下
  
   - save-dev
   
   > 在 package.json裡，只有寫入 devDependencies 下
  
   - dependencies : 使用在已經發布的環境下，換句話說，是指發布後仍然需要依賴使用的 plug-in。舉個例子來說，如果我需要使用 jQuery 與 AngularJs 來開發，就算開發完之後發佈到伺服器，我仍然需要依      賴    jQuery 與 AngularJs 的套件，這些套件會在發布後繼續使用。
     用法：當我執行 npm install –production 或是註明 NODE_ENV 變量值为為 production 時，只會下載 dependencies 中的套件。
   - devDependencies : 使用在開發中的環境下，意思是指——只單純會在開發時應用到的 plug-in。同樣舉個例子，如果我在開發時需要使用 Js ES6 並使用 babel 轉換成 ES5，或是我希望可以使用 gulp-stylus      的套件來使用，但在發佈之後，我們並不會在用到 gulp-stylus 這個套件。換句話說，他只需要存在於開發環境中，而不需要繼續放到發布環境裏。
 
   - 用法：鍵入 npm install 時，會同時抓下來 dependencies & devDependencies 兩個節點之中的套件。
   
5. 更新套件與解除安裝
```
//更新套件：npm update 可一次更新專案中的所有套件 
npm update

//可加入 -g 參數，更新全域套件
npm update -g

//刪除套件：npm uninstall 套件名稱，以下解除安裝 express 範例
npm uninstall express

//使用 -g 安裝的套件，刪除時，也必須加入 -g 參數
npm uninstall firebase-tools -g
```
6. 全域安裝與局部安裝

   - 全域性安裝方式 :
     1. 安裝方式:
     ```
      npm install <套件名稱> -g 或npm install <套件名稱>
     ```
     2. 安裝位置:
     
     </br>
     
        > 包安裝在Node安裝目錄下的node_modules資料夾中，一般在 \Users\使用者名稱\AppData\Roaming\ 目錄下，可以使用npm root -g檢視全域性安裝目錄
     
   - 局部安裝:
     1. 安裝方式:
      ```
      npm install <套件名稱> 或npm install <套件名稱> –save-dev
     ```
     2. 安裝位置:
     </br>
     
        > 其中引數–save-dev的含義是代表把你的安裝包資訊寫入package.json檔案的devDependencies欄位中，包安裝在指定專案的node_modules資料夾下。
        
### 話說全域安裝就好了啊

1. 僅全局安裝是夠嗎
</br>

   - 在js實例代碼中，默認下node.js會在NODE_PATH和目前js所在項目下的node_modules文件夾下去尋找模塊，因此，如果只是全局安裝，不能直接通過require的方式去引用模塊，需要手動解決包路徑的配置問題，     當然你也可以複製全局安裝的node_modules文件夾到項目下，還有辦法可以選擇將環境變量的NODE_PATH設置為C:\Program Files\nodejs。 
   
 </br>
 
   - 對於包的更新不好管理，可能你需要為每個包重新命名，如gulp@3.8.1、gulp@3.9.1...，為了區別不同項目使用指定的包，保證模塊之間的相互依賴（這塊下面會介紹），區別每個項目正常運行。
     因此，不推薦只全局安裝。
     
   - 另外，據node團隊介紹，本地安裝包對於專案的載入會更快。
   
### 備註
今天先說到這裡，


##### 參考資料
npm 官網(https://docs.npmjs.com/getting-started/)
npm介紹(http://tw.gitbook.net/nodejs/nodejs_npm.html)
npm常用指令教學-Node.js套件管理工具(https://www.ucamc.com/e-learning/computer-skills/324-npm%E5%B8%B8%E7%94%A8%E6%8C%87%E4%BB%A4%E6%95%99%E5%AD%B8-node-js%E5%A5%97%E4%BB%B6%E7%AE%A1%E7%90%86%E5%B7%A5%E5%85%B7)
弄懂 npm install 的 –save 與 –save-dev(https://chriskang028.wordpress.com/2017/07/05/%E5%BC%84%E6%87%82-npm-install-%E7%9A%84-dependencies-v-s-devdependencies/)
Nodejs全域性安裝和本地安裝的不同之處(https://codertw.com/%E5%89%8D%E7%AB%AF%E9%96%8B%E7%99%BC/263549/)
