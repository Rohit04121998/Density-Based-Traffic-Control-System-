#define con 15
#define trig1 9
#define echo1 8
#define trig2 5
#define echo2 4
#define trig3 3
#define echo3 2
void setup() {
 Serial.begin(38400);
 pinMode(13,OUTPUT);//red1     // 13 12   9 8
 pinMode(12,OUTPUT);//green1
 pinMode(11,OUTPUT);///red2         
 pinMode(10,OUTPUT);//green2    //  11 10  5  4
 pinMode(9,OUTPUT);//1
 pinMode(8,INPUT);//1
 pinMode(7,OUTPUT);///red3      // 3 4 7 6
 pinMode(6,OUTPUT);//green3
 pinMode(5,OUTPUT);//2
 pinMode(4,INPUT);//2
 pinMode(3,OUTPUT);//3
 pinMode(2,INPUT);//3

 
}

int i = 0;
int a =1;
int dur[3];
int d[3] = {1000,1000,1000};
void loop() {
  
 if(i==10) 
 {
    
  Serial.println("YAY");
    
   digitalWrite(9,LOW);
   delay(5);
   digitalWrite(9,HIGH);
   delay(10);
   digitalWrite(9,LOW);
   dur[0] = pulseIn(echo1,HIGH);
   d[0] = dur[0]/58;
   //Serial.println(d[0]);

   
   digitalWrite(5,LOW);
   delay(5);
   digitalWrite(5,HIGH);
   delay(10);
   digitalWrite(5,LOW);
   dur[1] = pulseIn(echo2,HIGH);
   d[1] = dur[1]/58;
   //Serial.println(d[1]);
 
   
   digitalWrite(3,LOW);
   delay(5);
   digitalWrite(3,HIGH);
   delay(10);
   digitalWrite(3,LOW);
   dur[2] = pulseIn(echo3,HIGH);
   d[2] = dur[2]/58;
   Serial.println(d[0]);
   Serial.println(d[1]); 
   Serial.println(d[2]);
    if((d[2]<=d[0])&&(d[2]<=d[1])&&(d[2]<con))
      {  Serial.println("WP");
           a = 2;}
     else  if((d[1]<d[2])&&(d[1]<=d[0])&&(d[1]<con))
        {a = 1;
        Serial.println("WM");}
    else if((d[0]<d[2])&&(d[0]<d[1])&&(d[0]<con))
        a = 0;        
    else
    { 
      Serial.println("WA");
       a++;
     if(a>2)
      {a =0;
      }
    d[0] =1000;
    d[1] =1000;
    d[2] =1000;
   }
   i=0;
   Serial.println(a);
 }
 else
{
  Serial.println(i);
  
  if(a==1)
   { 
    Serial.println("AAAAAA");
    digitalWrite(13,HIGH);
    digitalWrite(12,LOW);
    digitalWrite(11,LOW);
    digitalWrite(10,HIGH);
    digitalWrite(7,HIGH);
    digitalWrite(6,LOW);}
    else if(a==2)
  {
    Serial.println("EEEEEEE");
    digitalWrite(13,HIGH);
    digitalWrite(12,LOW);
    digitalWrite(11,HIGH);
    digitalWrite(10,LOW);
    digitalWrite(7,LOW);
    digitalWrite(6,HIGH);
    
  }
   else if(a==0)
   {
     Serial.println("DDDDDD");
     digitalWrite(11,HIGH);
     digitalWrite(10,LOW);
     digitalWrite(13,LOW);
     digitalWrite(12,HIGH);
     digitalWrite(7,HIGH);
     digitalWrite(6,LOW);
   }
   i++;
}

   delay(500);
} 
