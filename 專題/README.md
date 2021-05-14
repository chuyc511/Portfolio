# 簡介
在大三的專題，我和我的夥伴主要以新型階層式仲介架構應用於工廠端。此架構以去中心化、分散式運算、行動節點為特點，除了取代原先智慧工廠所使用的主從式架構(Client-Server model, C/S)，還結合了影像辨識與網頁前端開發，我們將影像辨識技術應用於工廠生產線上，達到產品品質控管。此外，前端網頁介面提供攝影機的即時直播、調閱影片以及影像辨識，使用者也能透過網頁自行蒐集樣本和取得其他節點的樣本來訓練模型。而我主要負責新型階層式架構節點之間溝通以及部分網頁開發。

## 網頁開發都以 Django 架設。

## 攝影機即時辨識畫面
後端使用 Flask 框架將 OpenCV 流(攝影機即時辨識結果、ROI區域)傳輸到 Web 上，並針對 NG情況做出警報。 

![image](https://user-images.githubusercontent.com/68286984/118290053-95a64600-b508-11eb-94f9-9ed5bd340dab.png)

# 監控畫面 
透過後端即時辨識水管品質，如出現NG水管，則向前端發出兩種警報，一是 Line Notify 推播訊息以及圖片，二是在監控畫面顯示紅框並藉由 Bootstrap Modal 彈出視窗觀看NG片段。

![image](https://user-images.githubusercontent.com/68286984/118290709-51677580-b509-11eb-82a9-8dac75165c22.png)

# 影像辨識樣本採集
利用 HTML MouseEvent 監控滑鼠並利用 Div 繪製出紅框，並使用JQuery Ajax 將座標傳至後端，後端則是用 Python OpenCV 處理影像，擷取 ROI 區域。

![image](https://user-images.githubusercontent.com/68286984/118290781-6512dc00-b509-11eb-81fa-a662d696474e.png)

# 樣本分類頁面 & 模型訓練頁面
主要利用 d3.js 拖曳物件搬移圖片以及製作分支樹訓練模型。

![image](https://user-images.githubusercontent.com/68286984/118290857-7a880600-b509-11eb-8379-6fa5903d9bb0.png)
![image](https://user-images.githubusercontent.com/68286984/118290868-7d82f680-b509-11eb-948b-f230e462f6ed.png)









