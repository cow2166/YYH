<center>
<H1> 實驗六</br>
警報器</br>
</h1>
</center>

---

![](https://github.com/cow2166/gitbo/blob/master/re/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7%202018-05-02%20%E4%B8%8B%E5%8D%885.04.33.png?raw=true)

```
//项目六 报警器
float sinVal;
int toneVal;

void setup(){
     pinMode(8, OUTPUT);
}

void loop(){
     for(int x=0; x<180; x++){
            sinVal = (sin(x*(3.1412/180)));
            toneVal = 2000+(int(sinVal*1000));
            tone(8, toneVal);
            delay(2); 
     }   
}
```


<iframe width="560" height="315" src="https://www.youtube.com/embed/pQYlbng2o-Y" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

---

<h1>結合lde燈</h1>

![](https://github.com/cow2166/gitbo/blob/master/re/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7%202018-05-02%20%E4%B8%8B%E5%8D%885.02.47.png?raw=true)



```
float sinVal;
int ledPin = 10;
int toneVal;

void setup(){
     pinMode(8, OUTPUT);
     pinMode(ledPin, OUTPUT);
}

void loop(){
     for(int x=0; x<180; x++){
            sinVal = (sin(x*(3.1412/180)));
            toneVal = 1000+(int(sinVal*1000));
            tone(8, toneVal);
            delay(2); 
     }
 digitalWrite(ledPin,HIGH); 
   delay(2); 
 
  
digitalWrite(ledPin,LOW);
   delay(2); 
     }   
```

<iframe width="560" height="315" src="https://www.youtube.com/embed/55mazXew_YE" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>