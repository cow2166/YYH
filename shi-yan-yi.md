# 實驗一
# LED閃爍


![](https://github.com/cow2166/gitbo/blob/master/re/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7%202018-04-29%20%E4%B8%8B%E5%8D%882.36.29.png?raw=true)


```

//项目一 —— LED 闪烁 
/* 
描述:LED 每隔一秒交替亮灭一次 */ 
int ledPin = 10;
void setup() {
        pinMode(ledPin, OUTPUT);
}
void loop() {
} 
digitalWrite(ledPin,HIGH); delay(1000); digitalWrite(ledPin,LOW); delay(1000); 

```