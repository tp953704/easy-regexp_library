## NPM安裝

### npm 是甚麼
在現代的網站中，使用他人開放原始碼的套件輔助開發已經是稀鬆平常的事情，
無論是透過套件加速堆砌產品，或是在開發環境中加上協助工程師的各式工具，
只需要稍加設定，一個專案便能輕易加載了成千上萬的外部程式。
</br>

首先還沒下載的人可以先去官網下載
`node進入點` (https://nodejs.org/en/)

</br>

![node官網](https://raw.githubusercontent.com/tp953704/IT-Contest/master/img/npm/node.png)

</br>

針對LTS / Current 版本，這裡給各位大哥做個整理

- LTS （長期支持，目前v6.11.2） -正如有人評論中提到，將有至少18個月支持和維護。所以最好在Production中將node.js用作後端服務。

- current 穩定 -將有大約8個月支持，釋放更多的時候功能/更新。如果您使用node.js作為前端服務（依賴關係管理等），則該版本對於Production來說可以。
如果您有能力在不中斷環境的情況下輕鬆更新您的應用程序，它也可以在後端使用node.js。
隨著Node.js的團隊描述的，當他們宣布這個功能是2種不同類型的node.js版本將滿足您的node.js需求/
</br>

也就是說，如果你有一個複雜的node.js應用程序，並且你想要穩定性，那麼就留在LTS。
</br>

下載好之後開啟終端機    輸入
`npm -v`和`node -v` 可以看到當前的node 和 npm 版本
</br>

![cmd](https://raw.githubusercontent.com/tp953704/IT-Contest/master/img/npm/%E8%9E%A2%E5%B9%95%E6%93%B7%E5%8F%96%E7%95%AB%E9%9D%A2%20(54).png)

</br>
`小提醒 : 如果想要更新npm的版本建議用  NVM(https://github.com/nvm-sh/nvm)  去做控管喔，畢竟防止意外你我有責。





##### 參考資料
- npm官方文檔(https://docs.npmjs.com/)
- NPM是什麼？了解Node Package Manager套件管理機制(https://tw.alphacamp.co/blog/npm-node-package-manager)

