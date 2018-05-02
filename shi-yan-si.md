<center>
<H1> 實驗四</br>
呼吸燈課後作業</br>
</h1>
</center>

---

<h1>呼吸燈</h1>

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


---

<h1>通過兩個按鍵,一個按鍵控制 LED 逐次變亮,另一個按鍵 控制 LED 逐次變暗。</h1>
![](https://github.com/cow2166/gitbo/blob/master/re/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7%202018-05-02%20%E4%B8%8B%E5%8D%888.44.51.png?raw=true)



```
int n=0;
void setup ()
{
  pinMode(4,INPUT);
  pinMode(6,OUTPUT);      //该端口需要选择有#号标识的数字口
  pinMode(10,INPUT);
}

void loop()
{
  int up =digitalRead(4);          //读取4号口的状态
  int down = digitalRead(10);      //读取10号口的状态   
  if (up==HIGH)                    //判断4号口目前是否是高电平
  { 
   n=n+5;                         //每次累加值为5
    if (n>=255) { n=255;
    }            //限定最大值为255   
analogWrite(6,n);               //使用PWM控制6号口输出，变量n的取值范围是0-255 
    delay (300);
  }
  if (down==HIGH)                    //减少亮度
  {
   n=n-5;
    if (n<=0) {
      n=0;
    }
analogWrite(6,n);
    delay (300);
  }
}
```

<iframe width="560" height="315" src="https://www.youtube.com/embed/6IWAxmxYEhQ" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>