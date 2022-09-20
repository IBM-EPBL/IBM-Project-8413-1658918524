int t=2;  

int e=3;  

void setup() {   

Serial.begin(9600);   

pinMode(t,OUTPUT);    

pinMode(e,INPUT);    

pinMode(12,OUTPUT);  

}  void loop() {    

digitalWrite(t,LOW);    

digitalWrite(t,HIGH);    

delayMicroseconds(10);    

digitalWrite(t,LOW);   

float dur=pulseIn(e,HIGH); 

float dis=(dur*0.0343)/2;    

Serial.print("Distance is: ");    

Serial.println(dis);            

if(dis>=100)   {      

digitalWrite(8,HIGH);     

digitalWrite(7,HIGH);   

}  

if(dis>=100)   

{   

for(int i=0; i<=30000; i=i+10)    

{    

tone(12,i);    

delay(1000);   

noTone(12);    

delay(1000);    

}   

}

double a= analogRead(A0);    

double t=(((a/1024)*5)-0.5)*100;    

Serial.print("Temp Value: ");    S

Serial.println(t);    

delay(1000); 

if(t>=100)   { 

digitalWrite(8,HIGH);      

digitalWrite(7,HIGH);    

}

if(t>=100)   

{   

for(int i=0; i<=30000; i=i+10)    

{    

tone(12,i);    

delay(1000);    

noTone(12);    

delay(1000);    

}    

}

if(t<100)   

{      

digitalWrite(7,LOW);    

} 

} 

digitalWrite(8,LOW);
