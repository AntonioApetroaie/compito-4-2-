# compito-4-2-
variante con if:
#define led1 5
#define led2 6
#define led3 7
#define led4 8
#define button1 12
#define button2 13

int num = 0;

void setup() {
  
  Serial.begin(9600);
  pinMode(led1, OUTPUT);
  pinMode(led2, OUTPUT);
  pinMode(led3, OUTPUT);
  pinMode(led4, OUTPUT);
  pinMode(button1,INPUT);
  pinMode(button2, INPUT);
}
  
void loop() {


  int b1 = digitalRead(button1);
  int b2 = digitalRead(button2);

  if (b1 == HIGH); {
    num++;
  }
  if (b2 == HIGH); {
    num--;
  }

  Serial.println();
  delay(300);
    
if (num = 0);{
  digitalWrite(led1, LOW);
  digitalWrite(led2,LOW);
  digitalWrite(led3, LOW);
  digitalWrite(led4,LOW);}

if (num =1);{
  digitalWrite(led1, HIGH);}
  
  if( num = 2);{
    digitalWrite(led2,HIGH);}
  
  if (num = 3);{
    digitalWrite(led1,HIGH);
    digitalWrite(led2,HIGH);}
  
  if ( num = 4);{
    digitalWrite(led3, HIGH);}
  
  if(num = 5);{
    digitalWrite(led3, HIGH);
    digitalWrite(led1, HIGH);}
  
if( num = 6);{
  digitalWrite(led2,HIGH);
  digitalWrite(led3, HIGH);}
  
  if( num = 7){
    digitalWrite(led1, HIGH);
  digitalWrite(led2, HIGH);
  digitalWrite(led3, HIGH);}

  if( num = 8);{
  digitalWrite(led4, HIGH);}

  if (num = 9);{
    digitalWrite(led1, HIGH);
    digitalWrite(led4, HIGH);}
     
    
  if(num = 10){
    digitalWrite(led4, HIGH);
    digitalWrite(led2, HIGH);}
    
if( num = 11){
  digitalWrite(led4, HIGH);
  digitalWrite(led2, HIGH);
  digitalWrite(led1, HIGH);}
if(num = 12){
  digitalWrite(led4, HIGH);  
  digitalWrite( led3, HIGH);}
  
if(num = 13){
  digitalWrite(led4, HIGH);
  digitalWrite(led3, HIGH);
  digitalWrite(led1, HIGH);}
  
if(num = 14){
  digitalWrite(led4, HIGH);
  digitalWrite(led2, HIGH);
  digitalWrite(led3, HIGH);}
if (num = 15);{
  digitalWrite(led4, HIGH);
  digitalWrite(led3, HIGH);
  digitalWrite(led2, HIGH);
  digitalWrite(led1, HIGH);}
  
 }
 
 
 
 
 variante con for:
 #define increase 7
#define decrease 6
#define led1 2
#define led2 3
#define led3 4
#define led4 5
#define button1 6
#define button2 7
#define DELAY 200
int loc = 0; //posizione

void setup()
{
  Serial.begin(9600);
  pinMode(led1, OUTPUT);
  pinMode(led2, OUTPUT);
  pinMode(led3, OUTPUT);
  pinMode(led4, OUTPUT);
  pinMode(button1, INPUT);
  pinMode(button2, INPUT);
}

void loop()
{
  int b1 = digitalRead(button1);
  int b2 = digitalRead(button2);

  if (b1 == HIGH && loc != 15)
    loc++;
  if (b2 == HIGH && loc != 0)
    loc--;
	
  delay(200);
  Serial.println(loc);
  
  for(int i=0; i<=3; i++){
    digitalWrite(led1+i,((loc >> 1) & 0x01));
  }
}
