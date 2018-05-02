<center>
<H1> 實驗八</br>
震動感測器</br>
</h1>
</center>

---

![](https://github.com/cow2166/gitbo/blob/master/re/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7%202018-05-02%20%E4%B8%8B%E5%8D%886.26.10.png?raw=true)

```
//项目八 – 震动传感器
int SensorLED = 13;       //定义LED为数字引脚13
int SensorINPUT = 3;      //连接震动开关到中断1，也就是数字引脚3 
unsigned char state = 0;

void setup() { 
  pinMode(SensorLED, OUTPUT);         //LED为输出模式
  pinMode(SensorINPUT, INPUT);        //震动开关为输入模式

  //低电平变高电平的过程中，触发中断1，调用blink函数
  attachInterrupt(1, blink, RISING);   
 }

void loop(){
      if(state!=0){              // 如果state不是0时
        state = 0;               // state值赋为0
        digitalWrite(SensorLED,HIGH);   // 亮灯
        delay(500);          //延时500ms
      }  
      else 
        digitalWrite(SensorLED,LOW);     // 否则，关灯
} 

void blink(){                //中断函数blink()
state++;             //一旦中断触发，state就不断自加
}
```


<iframe width="560" height="315" src="https://www.youtube.com/embed/_5EYGPXdi6c" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>