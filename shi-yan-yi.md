# 實驗一
# LED閃爍

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