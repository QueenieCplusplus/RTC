# RTC
FirebaseRTC on Google

![](https://raw.githubusercontent.com/QueenieCplusplus/RTC/main/RTC_Architecture.png)

# Firebase 

   * Firebase Hosting 託管 Web App 的 靜態資產
   
   * Cloud Firestore 可將結構化數據保存在雲端，並在數據更新時獲得即時通知 類似 Firebase Messaging
   
         注意：用於發信號的另一個選項可以是Firebase Cloud Messaging。但是，Chrome目前僅支持該功能，
              在此代碼實驗室中，我們將重點介紹一種可在所有支持WebRTC的瀏覽器上使用的解決方案。
   
   * FirebaseRTC 聊天室 API (SDP)
   
# Applied Industry

Actutally, the FB messenger & Google meet & Grome Remote Desktop Apps use WebRTC instead of VNC / RDP.

* Gaming

* Science

* Retail

# Nodejs APP

    git clone https://github.com/QueenieCplusplus/ChatRoom_Nodejs_App.git
    
    cd ChatRoom_Nodejs_App
    
# Firebase Shell

    npm -g install firebase-tools
    
    check the version is v6.7.1
    
    firebase login
    
    firebase use --add
    
    firebase serve --only hosting
    
    [output]
    hosting: Local server: http://localhost:5000
    
    您應該看到已連接到 Firebase 項目的 FirebaseRTC republicate。
    該應用程序已自動連接到您的 Firebase 項目。

# Chat Room

在此應用程序中，每個視頻聊天會話稱為一個房間。
用戶可以通過單擊應用程序中的按鈕來創建新房間。這將生成一個ID，供遠程方加入同一房間。
該ID用作Cloud Firestore中每個房間的密鑰。

每個房間都將包含要約 Invitation 和答案 Answer 的 RTCSessionDescriptions 會議描述，
以及來自各方的帶有 ICE 候選人的兩個單獨的集合。

該ID用作Cloud Firestore中每個房間的密鑰。

# RTC Concept

to be continued...
