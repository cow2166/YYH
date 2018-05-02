<center>
<H1> 實驗七</br>
溫度警報器</br>
</h1>
</center>

---

![](https://github.com/cow2166/gitbo/blob/master/re/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7%202018-05-02%20%E4%B8%8B%E5%8D%885.09.10.png?raw=true)


```
//项目七 – 温度报警器
float sinVal;            
int toneVal;
unsigned long tepTimer ;    

void setup(){ 
    pinMode(8, OUTPUT);        // 蜂鸣器引脚设置
    Serial.begin(9600);        //设置波特率为9600 bps
}

void loop(){ 
    int val;               // 用于存储LM35读到的值
    double data;          //用于存储已转换的温度值
    val=analogRead(0);   //LM35连到模拟口，并从模拟口读值
    data = (double) val * (5/10.24);  // 得到电压值，通过公式换成温度
     
    if(data>27){        //  如果温度大于27，蜂鸣器响   
          for(int x=0; x<180; x++){
            //将sin函数角度转化为弧度
            sinVal = (sin(x*(3.1412/180)));
            //用sin函数值产生声音的频率
            toneVal = 2000+(int(sinVal*1000));
            //给引脚8一个
            tone(8, toneVal);
            delay(2); 
     }   
    } else {    // 如果温度小于27，关闭蜂鸣器
           noTone(8);          //关闭蜂鸣器 
    }
     
    if(millis() - tepTimer > 500){     // 每500ms，串口输出一次温度值
             tepTimer = millis();
             Serial.print("temperature: ");     // 串口输出“温度”
             Serial.print(data);               // 串口输出温度值
             Serial.println("C");              // 串口输出温度单位
       } 
}
```

<iframe width="560" height="315" src="https://www.youtube.com/embed/EmBtX2208sg" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>