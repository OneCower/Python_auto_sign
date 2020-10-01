# Python封包傳送 刺蝟貓APP自動簽到程式  

## 使用環境  
`夜神模擬器6.6.1.1` `Python` `Packet Capture` `Jupyter Notebook`  

## 功能介紹
基於封包傳送做的簽到程式，開啟後會傳送封包做簽到動作，將所有帳號的簽到一次完成。  

## 使用方法  
使用Jupyter Notebook加載Auto_sign_in.ipynb  
第一次使用，需先使用Packet Capture抓取簽到任務封包  
使用Packet Capture擷取封包後，觀察期中一項發送可看到Post /reader/get_task_bonus_with_sign_recommend的封包，如下圖  
![](/img/封包教學1.png "抓取簽到任務封包")
執行簽到的正確網址便是這個位址前面再加上Host的網址  
也就是[app.hbooker.com/reader/get_task_bonus_with_sign_recommend]  
我們從此得知傳送封包的位址url = r'https://app.hbooker.com/reader/get_task_bonus_with_sign_recommend'  

在heads中填入裝置訊息，裝置訊息格式，如下圖  
![](/img/封包教學2.png "裝置訊息格式")  
程式碼中有範例，數量依帳號數量決定

在accounts_info中填入帳號訊息，帳號訊息格式，如下圖  
![](/img/封包教學3.png "帳號訊息格式")  
程式碼中有範例，數量依帳號數量決定  

StartNum和EndNum是從第StartNum到EndNum個帳號做簽到，預設0~9  


