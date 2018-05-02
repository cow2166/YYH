<center>
<H1> 實驗九</br>
感光燈</br>
</h1>
</center>

---

![](https://github.com/cow2166/gitbo/blob/master/re/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7%202018-05-02%20%E4%B8%8B%E5%8D%885.13.10.png?raw=true)


```
//项目九 – 感光灯
int LED = 13;                     //设置LED灯为数字引脚13
int val = 0;                      //设置模拟引脚0读取光敏二极管的电压值

void setup(){
     pinMode(LED,OUTPUT);         // LED为输出模式
     Serial.begin(9600);        // 串口波特率设置为9600
}

void loop(){
     val = analogRead(0);         // 读取电压值0~1023
     Serial.println(val);         // 串口查看电压值的变化
     if(val<1000){                // 一旦小于设定的值，LED灯关闭
          digitalWrite(LED,LOW);
     }else{                        // 否则LED亮起
          digitalWrite(LED,HIGH);
     }
     delay(10);                   // 延时10ms
}
```


<iframe width="560" height="315" src="https://www.youtube.com/embed/hESpI9IWVOE" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

---
<h1>感光警報器</h1>

![](https://github.com/cow2166/gitbo/blob/master/re/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7%202018-05-02%20%E4%B8%8B%E5%8D%888.28.30.png?raw=true)

```
int val = 0; 
float sinVal; 
float sinVal2; 
int toneVal; 
 
void setup(){ 
     pinMode(8,OUTPUT);         
     Serial.begin(9600);        
} 
 
void loop(){ 
     val = analogRead(0);         
     Serial.println(val);        
     sinVal = val;  
     if(val<1000){                
          digitalWrite(8,LOW);
          digitalWrite(sinVal,LOW); 
     }else{
          digitalWrite(8,HIGH);
          digitalWrite(sinVal,HIGH);
     } 
}
```



<iframe width="560" height="315" src="https://www.youtube.com/embed/dNFZH34YOEc" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
