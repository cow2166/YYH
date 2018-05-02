<center>
<H1> 實驗五</br>
炫彩 RGB LED</br>
</h1>
</center>

---

![](https://github.com/cow2166/gitbo/blob/master/re/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7%202018-05-02%20%E4%B8%8B%E5%8D%884.55.46.png?raw=true)




```
//项目五 – 炫彩RGB灯
int redPin = 9;
int greenPin = 10;
int bluePin = 11;

void setup(){
     pinMode(redPin, OUTPUT);
     pinMode(greenPin, OUTPUT);
     pinMode(bluePin, OUTPUT);

}
void loop(){
    colorRGB(random(0,255),random(0,255),random(0,255)); //R:0-255 G:0-255 B:0-255
    delay(1000);
}

void colorRGB(int red, int green, int blue){
     analogWrite(redPin,constrain(red,0,255));
     analogWrite(greenPin,constrain(green,0,255));
     analogWrite(bluePin,constrain(blue,0,255));
}
```

<iframe width="560" height="315" src="https://www.youtube.com/embed/bZUXosmOKXE" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>