# creative-convergence
창의융합
창의융합 과제1
1. 시나리오 및 작성 소감
저번 시간에 배웠던 센서 2개를 사용하는 것과는 다르게 이번 시간에는 조도센서를 이용하여 빛의 밝기에 따라 색깔이 달라지는 것도 신기했고 Processing 프로그램에 들어가서 코딩에 따라 색깔도 마음대로 바꿀 수 있어서 신기했고 이러한 조도센서를 이용하여 밤의 어두운 거리에 잘 안 보이기 때문에 자동차 앞부분에 조도센서를 달아서 위험한 물체가 있으면 알려주는 그러한 아두이노를 적용하여 실생활에 편리한 아두이노를 만들 것입니다. 앞으로 점점 더 흥미로운 창의 융합 시간이 기대가 됩니다. 아두이노 너무 재밌습니다. ♥


2.아두이노 코딩
void setup() {  

  Serial.begin(9600);
  
}

void loop() {

  int a = analogRead(A0);
  
  Serial.println(a); //a=a+1;
  
  delay(500);
  
  3.프로세싱 코딩
  
  import processing.serial.*;
  
Serial p;

void setup(){

  size(300,300);
  
  p=new Serial(this,"COM10",9600);
  
}

void draw(){

  if(p.available()>0){
  
   String m=p.readString();
    
   int a = int(m.trim());
    
   println(a);
    
   if(a>55) fill(0,255,0);
    
   else      fill(255,0,0);
    
   ellipse(150,150, 200,200);
    
 }
