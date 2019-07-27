# gds
밝기에 따라 불 깜빡깜빡 하는거
```cpp
void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);
  pinMode(5,OUTPUT);
  digitalWrite(5,HIGH);
}

void loop() {
  // put your main code here, to run repeatedly:
   int value;
   value=analogRead(A0);
   Serial.println(value);

   delay(100);
  if(value<400){
   digitalWrite(5,LOW);
  }else{
   digitalWrite(5,HIGH);
  }
   
   
}
