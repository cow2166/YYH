<center>
<H1> 實驗一</br>
LED閃爍</br>
</h1>
</center>

---

![](https://github.com/cow2166/gitbo/blob/master/re/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7%202018-04-29%20%E4%B8%8B%E5%8D%882.36.29.png?raw=true)


```

//項目一 —— LED 閃爍 
/* 
描述:LED 每隔一秒交替亮滅一次 
*/ 

int ledPin = 10;        //設定LED燈的電源接口為10

void setup() {
pinMode(ledPin, OUTPUT);        設定LED燈為輸出值       
}
void loop() {                        開始持續循環以下程式
digitalWrite(ledPin,HIGH);        燈變亮 
delay(1000);                 維持1000毫秒
digitalWrite(ledPin,LOW);         燈變暗
delay(1000);                 維持1000毫秒
}
```

