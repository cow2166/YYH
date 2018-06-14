# **ESP32溫溼度數據上傳練習**

![](/assets/44464.jpg)

## 1.首先要先要將arduino IDE 安裝 ESP32擴充模組![](/assets/esp32-1.png)安裝連接線驅動器![](/assets/esp32-2.png)下載ESP32模組並安裝

### 教學網址:[http://wangwangtc.blogspot.com/2017/09/arduino.html](http://wangwangtc.blogspot.com/2017/09/arduino.html)

## 2.設定WiFi服務器

### 利用範例中的SimpleWiFiServer進行設定

### 設定ESP32要連線的WiFi 名稱與密碼![](/assets/esp-3.png)

### 上傳至板子,開啟監視視窗,將會顯示這台電腦的IP,進入IP位址即可與板子互動

![](/assets/10.png)

## 3.將溫溼度程式加入上列

### **注意**:不但要下載DHT數據庫,還要安裝Adafruit\_Sensor數據庫,否則無法編譯![](/assets/esp-4.png)

## 數據回傳實際練習影片:

1.練習1
<iframe width="560" height="315" src="https://www.youtube.com/embed/LwXqC03Qoys" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

2.練習2

<iframe width="560" height="315" src="https://www.youtube.com/embed/fAT-DEcROKE" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

