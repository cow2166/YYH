<center>
<H1> 實驗十五</br>
紅外線遙控七段顯示器</br>
</h1>
</center>
 
---


<img src="https://github.com/cow2166/gitbo/blob/master/re/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7%202018-05-01%20%E4%B8%8B%E5%8D%8810.17.39.png?raw=true" alt="程式" title="程式">

![](https://github.com/cow2166/gitbo/blob/master/re/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7%202018-05-02%20%E4%B8%8B%E5%8D%885.40.55.png?raw=true)

```
//项目15 – 数码管显示
void setup(){
  for(int pin = 2 ; pin <= 9 ; pin++){       // 设置数字引脚2~9为输出模式
      pinMode(pin, OUTPUT);
      digitalWrite(pin, HIGH);
  }
}

void loop() { 
     // 显示数字0          
    int n0[8]={0,0,0,1,0,0,0,1}; 
    for(int pin = 2; pin <= 9 ; pin++){        // 数字引脚2~9依次按数组n0[8]中的数据显示 
       digitalWrite(pin,n0[pin-2]);
    }
    delay(500);
    
    // 显示数字1 
    int n1[8]={0,1,1,1,1,1,0,1};
    for(int pin = 2; pin <= 9 ; pin++){        // 数字引脚2~9依次按数组n1[8]中的数据显示 
       digitalWrite(pin,n1[pin-2]);
    }
    delay(500);
    
    // 显示数字2
    int n2[8]={0,0,1,0,0,0,1,1};
    for(int pin = 2; pin <= 9 ; pin++){       // 数字引脚2~9依次按数组n2[8]中的数据显示
       digitalWrite(pin,n2[pin-2]);
    }
    delay(500);   
    // 显示数字3
    int n3[8]={0,0,1,0,1,0,0,1};
    for(int pin = 2; pin <= 9 ; pin++){       // 数字引脚2~9依次按数组n3[8]中的数据显示
       digitalWrite(pin,n3[pin-2]);
    }
    delay(500);  
    
    // 显示数字4
    int n4[8]={0,1,0,0,1,1,0,1};
    for(int pin = 2; pin <= 9 ; pin++){      // 数字引脚2~9依次按数组n4[8]中的数据显示
       digitalWrite(pin,n4[pin-2]);
    }
    delay(500);  
    
    // 显示数字5 
    int n5[8]={1,0,0,0,1,0,0,1};
    for(int pin = 2; pin <= 9 ; pin++){      // 数字引脚2~9依次按数组n5[8]中的数据显示
       digitalWrite(pin,n5[pin-2]);
    }
    delay(500); 
    
    // 显示数字6 
    int n6[8]={1,0,0,0,0,0,0,1};
    for(int pin = 2; pin <= 9 ; pin++){     // 数字引脚2~9依次按数组n6[8]中的数据显示
       digitalWrite(pin,n6[pin-2]);
    }
    delay(500); 
    
    // 显示数字7 
    int n7[8]={0,0,1,1,1,1,0,1};
    for(int pin = 2; pin <= 9 ; pin++){     // 数字引脚2~9依次按数组n7[8]中的数据显示
       digitalWrite(pin,n7[pin-2]);
    }
    delay(500); 
    
    // 显示数字8
    int n8[8]={0,0,0,0,0,0,0,1};
    for(int pin = 2; pin <= 9 ; pin++){     // 数字引脚2~9依次按数组n8[8]中的数据显示
       digitalWrite(pin,n8[pin-2]);
    }
    delay(500); 
    
    // 显示数字9
    int n9[8]={0,0,0,0,1,1,0,1};
    for(int pin = 2; pin <= 9 ; pin++){    //  数字引脚2~9依次按数组n3[9]中的数据显示
       digitalWrite(pin,n9[pin-2]);
    }
    delay(500);
}
```


<iframe width="560" height="315" src="https://www.youtube.com/embed/0QCLB2zCom0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>


<h1>紅外線遙控七段顯示器</h1>

<img src="https://github.com/cow2166/gitbo/blob/master/re/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7%202018-05-01%20%E4%B8%8B%E5%8D%8810.20.04.png?raw=true" alt="程式" title="程式">


<pre><code>
 
#include <IRremote.h>      //调用IRremote.h库
int RECV_PIN = 11;         //定义RECV_PIN变量为11
IRrecv irrecv(RECV_PIN);   //设置RECV_PIN（也就是11引脚）为红外接收端
decode_results results;    //定义results变量为红外结果存放位置
int currentNumber = 0;     //该变量用于存放当前数字

long codes[12]=             //该数组用来存放红外遥控器发出的红外码
{
   0xFD30CF,0xFD08F7,               // 0 ,1
   0xFD8877,0xFD48B7,               // 2 ,3
   0xFD28D7,0xFDA857,               // 4 ,5
   0xFD6897,0xFD18E7,               // 6 ,7
   0xFD9867,0xFD58A7,               // 8 ,9
   0xFD20DF,0xFD609F,               // 前进 ,后退
};

int number[10][8] =            //该数组用来存放数码管显示的数字
{
  {0,0,0,1,0,0,0,1},//0
  {0,1,1,1,1,1,0,1},//1
  {0,0,1,0,0,0,1,1},//2
  {0,0,1,0,1,0,0,1},//3
  {0,1,0,0,1,1,0,1},//4
  {1,0,0,0,1,0,0,1},//5
  {1,0,0,0,0,0,0,1},//6
  {0,0,1,1,1,1,0,1},//7
  {0,0,0,0,0,0,0,1},//8
  {0,0,0,0,1,1,0,1} //9
};

void numberShow(int i) {                  //该函数用来让数码管显示数字
  for(int pin = 2; pin <= 9 ; pin++){
     digitalWrite(pin, number[i][pin - 2]);
  }
}

void setup(){
  Serial.begin(9600);            //设置波特率为9600
  irrecv.enableIRIn();           //启动红外解码
  
  for(int pin = 2 ; pin <= 9 ; pin++){   //设置数字引脚2~9为输出模式
      pinMode(pin, OUTPUT);
      digitalWrite(pin, HIGH);
  }
}

void loop() {
  //判断是否接收到解码数据,把接收到的数据存储在变量results中
  if (irrecv.decode(&results)) {
      for(int i = 0; i <= 11; i++){
         //判断是否接收到0~9按键的红外码
         if(results.value == codes[i]&& i <= 9){
               numberShow(i);  //在数码管上对应显示0~9
               currentNumber = i;  //把当前显示的值赋给变量currentNumber
               Serial.println(i);
               break;        
         }
         
         //判断是否接收到递减的红外码，并且当前值不为0
         else if(results.value == codes[10]&& currentNumber != 0){
               currentNumber--;                 //当前值递减
               numberShow(currentNumber);       //数码管显示递减后的值
               Serial.println(currentNumber);  //串口输出递减后的值
               break;        
         }
         
         //判断是否接收到递增的红外码，并且当前值不为9
         else if(results.value == codes[11]&& currentNumber != 9){
               currentNumber++;                 //当前值递增
               numberShow(currentNumber);       //数码管显示递增后的值
               Serial.println(currentNumber);  //串口输出递增后的值
               break;            
         }
    } 
    
   Serial.println(results.value, HEX);  //串口监视器查看红外码
   irrecv.resume();   //等待接收下一个信号 
  }
}

</code></pre>

<iframe width="560" height="315" src="https://www.youtube.com/embed/O8L2SVGJ5GI" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>


