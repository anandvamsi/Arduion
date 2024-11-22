# Implement Blinking of 3 LEB with Timer

```cpp
int led1=7;
int led2=6;
int led3=5;

void setup() {
  // put your setup code here, to run once:
pinMode(7,OUTPUT);
pinMode(6,OUTPUT);
pinMode(5,OUTPUT);
}

void loop() {
  // put your main code here, to run repeatedly:
digitalWrite(7,HIGH);
delay(9000);
digitalWrite(7,LOW);
delay(1000);
digitalWrite(6,HIGH);
delay(9000);
digitalWrite(6,LOW);
delay(1000);
digitalWrite(5,HIGH);
delay(9000);
digitalWrite(5,LOW);
delay(1000);

}
```
