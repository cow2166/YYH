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
int rledPin = 12;
int gledPin = 11;
int yledPin = 10;
void setup() {
        pinMode(rledPin, OUTPUT);
        pinMode(yledPin, OUTPUT);
        pinMode(gledPin, OUTPUT);
}
void loop() {
        digitalWrite(rledPin,HIGH);
        delay(5000);
        digitalWrite(yledPin,HIGH);
        delay(2000);        
        digitalWrite(rledPin,LOW);
        digitalWrite(yledPin,LOW);
        digitalWrite(gledPin,HIGH);
        delay(5000);
        digitalWrite(gledPin,LOW);
        digitalWrite(yledPin,HIGH);
        delay(2000);
        digitalWrite(yledPin,LOW); 
}
```


<iframe width="560" height="315" src="https://www.youtube.com/embed/QqQXAyj74xc" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
