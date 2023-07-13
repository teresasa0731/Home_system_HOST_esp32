# Home system design
## Defining the scope & target outcomes  
為了學習開發一套居家系統，這次專案從建立整個系統的控制中心 System Host開始，配合基本的三個功能來架設，分別為：  
1. Control：以LED燈呈現對開關的控制，  
2. Monitor：分別以switch+LED燈呈現靜態訪問的訊號；以HC-SR501來呈現及時狀態的偵測  
3. live streaming：以影像串流呈現  

## Scheduled Milestone
1. 了解網路傳輸協定與模式
2. 掌握esp32 wifi connection & HTTP 協定
3. 修正對CPU的效能分配  
4. 建立file system  
5. 學習HTML文本

### Ver.1  
使用web server技術做單向連接。   
(details under the folder ver1/)  

### Ver.2
使用web socket技術 + SPIFFS做雙向溝通。
(details under the folder ver2/) 

## Future Work
1. 完善網頁架構
2. 硬件方面修正與設計
    a. 更換人體感應模組：
    b. 實際連接居家電器(ex.電風扇/檯燈等)
3. 影像串流掛上web socket：目前僅ver.1以polling詢問esp32 eye伺服器的影像，ver.2尚未想到與host esp32資訊隔離的解法
4. 學習影像辨識，取得所需資訊(ex.人體偵測/環境辨識等)，並與此居家系統結合