# System host ver.2
## Introduction
改成使用 web socket + SPIFFS的模式，除了將發送文檔打包而非內嵌於程式碼，在對HTML文本進行優化時能獨立處理，也實現client與server的雙向溝通機制，可以即時的交換資訊，不用等待client端發出請求，或使用佔用資源的輪詢方式來實現，同時因Handshake後會保持連線狀態，所以每次通訊時所發出的請求就可省略掉一些關於連線狀態的資訊，提高連線效率。

