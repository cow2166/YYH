<center>
<H1> 實驗十三</br>
自製風扇</br>
</h1>
</center>

---
![](https://github.com/cow2166/gitbo/blob/master/re/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7%202018-05-01%20%E4%B8%8B%E5%8D%8810.53.46.png?raw=true)



```
//项目十三 – Arduino控制风扇转动
int buttonPin = 2;                          // button连接到数字2
int relayPin = 3;                           // 继电器连接到数字3
int relayState = HIGH;                       // 继电器初始状态为HIGH
int buttonState;                            // 记录button当前状态值
int lastButtonState = LOW;                  // 记录button前一个状态值
long lastDebounceTime = 0;                  
long debounceDelay = 50;                    //去除抖动时间

void setup() {
  pinMode(buttonPin, INPUT);
  pinMode(relayPin, OUTPUT);

  digitalWrite(relayPin, relayState);       // 设置继电器的初始状态
}
void loop() {
  int reading = digitalRead(buttonPin);   //reading用来存储buttonPin的数据
  
  // 一旦检测到数据发生变化，记录当前时间
  if (reading != lastButtonState) {   
    lastDebounceTime = millis();
  } 
  
  // 等待50ms，再进行一次判断，是否和当前button状态相同
  // 如果和当前状态不相同，改变button状态
  // 同时，如果button状态为高（也就是被按下），那么就改变继电器的状态
  if ((millis() - lastDebounceTime) > debounceDelay) {
    if (reading != buttonState) {
      buttonState = reading;
      
      if (buttonState == HIGH) {
        relayState = !relayState;
      }
    }
  }
  digitalWrite(relayPin, relayState);

  // 改变button前一个状态值
  lastButtonState = reading;
}


```




<iframe width="560" height="315" src="https://www.youtube.com/embed/_b3uNk0HMOs" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>