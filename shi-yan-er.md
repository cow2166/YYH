<center>
<H1> 實驗二
</br>
sos求救訊號器課後作業
</br>
</h1>
</center>

---


![](https://github.com/cow2166/gitbo/blob/master/re/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7%202018-04-29%20%E4%B8%8B%E5%8D%882.29.13.png?raw=true)


![](https://github.com/cow2166/gitbo/blob/master/re/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7%202018-04-29%20%E4%B8%8B%E5%8D%885.48.25.png?raw=true)

```
int rledPin = 12;  //設定紅色LED燈的電源接口為12
int gledPin = 11;  //設定綠色LED燈的電源接口為11
int yledPin = 10;  //設定黃色LED燈的電源接口為10
void setup() {
        pinMode(rledPin, OUTPUT);  //設定紅色LED燈為輸出值
        pinMode(yledPin, OUTPUT);  //設定黃色LED燈為輸出值
        pinMode(gledPin, OUTPUT);  //設定綠色LED燈為輸出值
}
void loop() {
        digitalWrite(rledPin,HIGH);  //紅色燈變亮
        delay(5000);                 //持續5000毫秒
        digitalWrite(yledPin,HIGH);  //黃色燈變亮
        delay(2000);                 //持續2000毫秒
        digitalWrite(rledPin,LOW);   //紅色燈變暗
        digitalWrite(yledPin,LOW);   //黃色燈變暗
        digitalWrite(gledPin,HIGH);  //綠色燈變亮
        delay(5000);                 //持續5000毫秒
        digitalWrite(gledPin,LOW);   //綠色燈變暗
        digitalWrite(yledPin,HIGH);  //黃色燈變亮
        delay(2000);                 //持續2000毫秒
        digitalWrite(yledPin,LOW);   //黃色燈變暗
}
```


<iframe width="560" height="315" src="https://www.youtube.com/embed/QqQXAyj74xc" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
