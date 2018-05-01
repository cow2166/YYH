<center>
<H1> 實驗十四</br>
紅外線遙控燈</br>
</h1>
</center>

---



<img scr="https://github.com/cow2166/gitbo/blob/master/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7%202018-05-01%20%E4%B8%8B%E5%8D%8810.26.09.png?raw=true" alt="14" title="14">
 


<pre><code>
#include <IRremote.h>           //调用IRremote.h库
int RECV_PIN = 11;              //定义RECV_PIN变量为11    
int ledPin = 10;                // LED – digital 10
boolean ledState = LOW;         // ledstate用来存储LED的状态
IRrecv irrecv(RECV_PIN);        //设置RECV_PIN（也就是11引脚）为红外接收端
decode_results results;         //定义results变量为红外结果存放位置

void setup(){
  Serial.begin(9600);          //串口波特率设为9600
  irrecv.enableIRIn();          //启动红外解码
  pinMode(ledPin,OUTPUT);       // 设置LED为输出状态
}

void loop() {
  //是否接收到解码数据,把接收到的数据存储在变量results中
  if (irrecv.decode(&results)) {  
       //接收到的数据以16进制的方式在串口输出   
      Serial.println(results.value, HEX);
    
      //一旦接收到电源键的代码, LED翻转状态，HIGH变LOW，或者LOW变HIGH
      if(results.value == 0xFD00FF){
               ledState = !ledState;             //取反      
               digitalWrite(ledPin,ledState);    //改变LED相应状态        
           }     
   irrecv.resume();  // 继续等待接收下一组信号
   }
}
</pre></code>


<iframe width="560" height="315" src="https://www.youtube.com/embed/wRfbxzkZ2uA" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe> 
