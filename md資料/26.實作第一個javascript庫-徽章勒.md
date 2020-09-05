## 實作第一個javascript庫-徽章勒

前幾天 小明小華有一個對話如下
...

```
小明說:在前面幾個章節我們有提過 ` "沒有單元測試的庫，就代表有一定的風險" `
小華說: 為甚麼呢?
小明說:你想想喔，如果今天一個庫有局部的修改，但是要怎麼知道 修改完，所有的function都沒有壞呢
~~~~如此如此這般這般~~~
```


那問題來了，即使我們這種偉大又有愛心(?????)的庫開發者做了很完整的測試和持續部屬

</br>
要怎麼讓使用的工程師知道呢



### 燈燈燈燈~~徽章

這裡給你們Vue2的徽章參考 (https://github.com/vuejs/vue)

![vue2參考](https://raw.githubusercontent.com/tp953704/IT-Contest/master/img/%E5%BE%BD%E7%AB%A0/1598675436480.jpg)


</br>

我們可以由上圖得到很多資訊，例如
- 我們可以由 `build | passing` 標籤得到他有座持續部屬與測試，進而得知目前這一版是沒有問題的
- `downloads 7.4/month` 可以得知這個月的下載量
- .....

</br>

接下來我們一起去獲得徽章八

### 取得徽章

> shields.io (https://shields.io/#/) 這是一個專門做徽章的免費網站，而我們先點進去 license 做出我們的第一個徽章

![徽章網站](https://raw.githubusercontent.com/tp953704/IT-Contest/master/img/%E5%BE%BD%E7%AB%A0/%E5%BE%BD%E7%AB%A0%E7%B6%B2%E7%AB%99.jpg)
    
 
 
 點進license 之後會看到很多不同的環境名稱，由於我們的庫已經上傳npm 了 所以我們可以直接點擊第一個npm ，
 </br>
 然後裡面輸入我們npm package的名稱，再把得到的標籤網址複製下來，貼上自己庫的readme.md即可，生成如圖
 
 ![生成徽章](https://raw.githubusercontent.com/tp953704/IT-Contest/master/img/%E5%BE%BD%E7%AB%A0/%E7%94%9F%E6%88%90URL.jpg) 
 
 
 ### 總結
 目前我們的小庫庫已經完成了，之後我們會繼續探討有關大型庫的管理模式。那今天就先到這裡摟，各位晚安。
