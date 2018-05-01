<center>
<H1> 實驗十</br>
伺服馬達(舵機)初動</br>
</h1>
</center>

---

![](https://github.com/cow2166/gitbo/blob/master/re/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7%202018-05-01%20%E4%B8%8B%E5%8D%8810.57.55.png?raw=true)


```
//项目十 - 舵机
#include <Servo.h>      // 声明调用Servo.h库
Servo myservo;          // 创建一个舵机对象
int pos = 0;            // 变量pos用来存储舵机位置
 
void setup() { 
    myservo.attach(9);  // 将引脚9上的舵机与声明的舵机对象连接起来
} 
 
void loop() { 
    for(pos = 0; pos < 180; pos += 1){   // 舵机从0°转到180°，每次增加1°          
        myservo.write(pos);              // 给舵机写入角度   
        delay(15);                       // 延时15ms让舵机转到指定位置
    }
    
    for(pos = 180; pos>=1; pos-=1) {     // 舵机从180°回到0°，每次减小1°                               
        myservo.write(pos);              // 写角度到舵机     
        delay(15);                       // 延时15ms让舵机转到指定位置
    } 
}
```

<iframe width="560" height="315" src="https://www.youtube.com/embed/v1r9RJzjojY" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>