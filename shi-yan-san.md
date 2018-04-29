<center>
<H1> 實驗三</br>
互動交通信號燈課後作業</br>
</h1>
</center>

---

![](https://github.com/cow2166/gitbo/blob/master/re/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7%202018-04-29%20%E4%B8%8B%E5%8D%882.52.49.png?raw=true)

---

<ol type="1">
<h3><li>選擇任意顏色 LED 6 個,做一個流水燈的效果,6 盞燈從左至右依次點亮,然後再 從右至左依次熄滅。</li></h3>

<img src="https://github.com/cow2166/gitbo/blob/master/re/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7%202018-04-29%20%E4%B8%8B%E5%8D%885.38.37.png?raw=true" alt="程式" title="程式">



<pre><code>
int led13 = 13 ;</br>
int led12 = 12 ;</br>
int led11 = 11 ;</br>
int led10 = 10 ;</br>
int led9 = 9 ;</br>
int led8 = 8 ;</br>
void setup() {</br>
  pinMode(led13, OUTPUT);</br>
  pinMode(led12, OUTPUT);</br>
  pinMode(led11, OUTPUT);</br>
  pinMode(led10, OUTPUT);</br>
  pinMode(led9, OUTPUT);</br>
  pinMode(led8, OUTPUT);</br>

}</br>

void loop() {</br>
  digitalWrite(led13, HIGH);</br>
  delay(400);</br>
  digitalWrite(led12, HIGH);</br>
  delay(400);</br>
  digitalWrite(led11, HIGH);</br>
  delay(400);</br>
  digitalWrite(led10, HIGH);</br>
  delay(400);</br>
  digitalWrite(led9, HIGH);</br>
  delay(400);</br>
  digitalWrite(led8, HIGH);</br>
  delay(1000);</br>
  digitalWrite(led8, LOW);</br>
  delay(400);</br>
  digitalWrite(led9, LOW);</br>
  delay(400);</br>
  digitalWrite(led10, LOW);</br>
  delay(400);</br>
  digitalWrite(led11, LOW);</br>
  delay(400);</br>
  digitalWrite(led12, LOW);</br>
  delay(400);</br>
  digitalWrite(led13, LOW);</br>
  delay(1000);</br>
}</br>
</code></pre>


<iframe width="560" height="315" src="https://www.youtube.com/embed/Wb8W63FOoro" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

<HR color="#ffd000">


<h3><li>如果上面那個你已經完成了的話,可以嘗試一下,先從中間的燈開始亮起,依次向 兩邊擴開。下圖是個變換過程的示意圖。</li></h3>


<img src="https://github.com/cow2166/gitbo/blob/master/re/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7%202018-04-29%20%E4%B8%8B%E5%8D%885.41.11.png?raw=true" alt="程式" title="程式">

<pre><code>
int led13 = 13 ;
int led12 = 12 ;
int led11 = 11 ;
int led10 = 10 ;
int led9 = 9 ;
int led8 = 8 ;
void setup() {
  pinMode(led13, OUTPUT);
  pinMode(led12, OUTPUT);
  pinMode(led11, OUTPUT);
  pinMode(led10, OUTPUT);
  pinMode(led9, OUTPUT);
  pinMode(led8, OUTPUT);

}

void loop() {
  digitalWrite(led11, HIGH);
  digitalWrite(led10, HIGH);
  delay(400);
  digitalWrite(led12, HIGH);
  digitalWrite(led9, HIGH);
  delay(400);
  digitalWrite(led13, HIGH);
  digitalWrite(led8, HIGH);
  delay(1000);
  digitalWrite(led13, LOW);
  digitalWrite(led8, LOW);
  delay(400);
  digitalWrite(led12, LOW);
  digitalWrite(led9, LOW);
  delay(400);
  digitalWrite(led11, LOW);
  digitalWrite(led10, LOW);
  delay(1000);

}

</code></pre>

<iframe width="560" height="315" src="https://www.youtube.com/embed/NwWbz7tk1ag" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

<HR color="#ffd000">

<h3><li>再比如,從左至右,依次亮起 1 個,2 個,3 個......</li></h3>


<img src="https://github.com/cow2166/gitbo/blob/master/re/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7%202018-04-29%20%E4%B8%8B%E5%8D%885.43.19.png?raw=true" alt="程式" title="程式">


<pre><code>
int led13 = 13 ;
int led12 = 12 ;
int led11 = 11 ;
int led10 = 10 ;
int led9 = 9 ;
int led8 = 8 ;
void setup() {
  pinMode(led13, OUTPUT);
  pinMode(led12, OUTPUT);
  pinMode(led11, OUTPUT);
  pinMode(led10, OUTPUT);
  pinMode(led9, OUTPUT);
  pinMode(led8, OUTPUT);

}

void loop() {
  digitalWrite(led13, HIGH);
   delay(400);
  digitalWrite(led12, HIGH);
  delay(400);   
  digitalWrite(led11, HIGH);
  delay(400);   
  digitalWrite(led10, HIGH);
  delay(400);
  digitalWrite(led9, HIGH);
  delay(400);   
  digitalWrite(led8, HIGH);
  delay(400);

  digitalWrite(led13, LOW);
  digitalWrite(led12, LOW); 
  digitalWrite(led11, LOW);
  digitalWrite(led10, LOW);
  digitalWrite(led9, LOW);
  digitalWrite(led8, LOW);
 

}

</code></pre>


<iframe width="560" height="315" src="https://www.youtube.com/embed/jk1a_RDkoFM" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

<HR color="#ffd000">

<h3><li>再結合按鈕,用按鍵開關和 LED 互動。</li></h3>

<img src="https://github.com/cow2166/gitbo/blob/master/re/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7%202018-04-29%20%E4%B8%8B%E5%8D%885.46.01.png?raw=true" alt="程式" title="程式">



<pre><code>
int led13 = 13 ;

int button = 12;
void setup() {
  pinMode(led13, OUTPUT);

  pinMode(button, INPUT);

}

void loop(){
  if(digitalRead(button) == HIGH){
    digitalWrite(led13, HIGH);
    delay(10000);
  }else{
  digitalWrite(led13, LOW);
}
}

</code></pre>



<iframe width="560" height="315" src="https://www.youtube.com/embed/TqE5Kzkg3mQ" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

</ol>






