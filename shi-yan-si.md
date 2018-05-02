<center>
<H1> 實驗四</br>
呼吸燈課後作業</br>
</h1>
</center>

---

![](https://github.com/cow2166/gitbo/blob/master/re/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7%202018-05-02%20%E4%B8%8B%E5%8D%888.13.30.png?raw=true)


```
//项目四 – 呼吸灯 
    int ledPin = 10; 
 
void setup() { 
      pinMode(ledPin,OUTPUT); 
} 
 
void loop(){ 
      fadeOn(1000,5); 
      fadeOff(1000,5); 
} 
 
void fadeOn(unsigned int time,int increament){ 
 for (byte value = 0 ; value < 255; value+=increament){  
     analogWrite(ledPin, value); 
  delay(time/(255/5)); 
        }  
} 
 
void fadeOff(unsigned int time,int decreament){ 
 for (byte value = 255; value >0; value-=decreament){  
     analogWrite(ledPin, value);  
  delay(time/(255/5));  
 } 
} 
```

<iframe width="560" height="315" src="https://www.youtube.com/embed/hBvL4lsQf00" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>