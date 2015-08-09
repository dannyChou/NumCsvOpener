# NumCsvOpener
避免Excel開啟CSV時截掉左補零的小工具
------------------------------------

使用Excel開啟CSV檔案，會l將純數字組成的字串視為數字型別處理，導致"000123"之類的左補零數字編碼變成"123"(如下圖所示)，對必須補零到固定長度的編碼欄位來說，莫名被截掉部分內容，常會造成困擾。所幸，透過簡單的CSV花式技巧，在CSV中寫成="000123"，就可強迫Excel將其視為文字處理，避免前方的零被截除。

這是一支.NET Windows Form小工具，讓使用者放在桌面上，當需要開啟這類含左補零數字CSV時，不要直接點選CSV開Excel，而是透過小工具選取檔案，小工具會讀取CSV內容，將所有欄位內容重新包裝成="…"格式，全部當成字串，再另存成*.fixed.csv(修正版)，最後啟動Excel開啟修正後的CSV，避開左補零被截除的問題。


[概念介紹](http://blog.darkthread.net/post-2012-04-12-keep-csv-leading-zeros-in-excel.aspx) 

2015-08-09 加入語系編號選擇及欄位內換行支援

[強化版介紹](http://blog.darkthread.net/post-2015-08-09-numcsvopener-support-mutiline.aspx)
