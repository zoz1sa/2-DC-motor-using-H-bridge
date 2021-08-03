# 2-DC-motor-using-H-bridge

![image](https://user-images.githubusercontent.com/86917834/127993673-126dc613-8f18-48e7-b71d-adf2c72ef0c5.png)


//M1:
#define Ena 10
#define IN1 9
#define IN2 8
//M2:
#define Enb 11
#define IN3 12
#define IN4 13  
int speeda=120;
int speedb=120;
void setup(){
  pinMode(Ena,OUTPUT);
  pinMode(IN1,OUTPUT);
  pinMode(IN2,OUTPUT);
  pinMode(Enb,OUTPUT);
  pinMode(IN3,OUTPUT);
  pinMode(IN4,OUTPUT);
}
void loop(){
  //M1:
  digitalWrite(IN1,HIGH);
  digitalWrite(IN2,LOW);
  analogWrite(Ena,speeda);
  //M2:
  digitalWrite(IN3,HIGH);
  digitalWrite(IN4,LOW);
  analogWrite(Enb,speedb);
  }
