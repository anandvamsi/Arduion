# How to Integrate IR sensor and Servo Motor.


```cpp
#include <Servo.h>

Servo s1;
int x;

void setup() {
  // put your setup code here, to run once:
Serial.begin(9600);
s1.attach(6);
pinMode(8,INPUT);
}

void loop() {
  // put your main code here, to run repeatedly:
x=digitalRead(8);
Serial.println(x);
if (x==0)
{
s1.write(0);
delay(1000);
s1.write(90);
delay(1000);
s1.write(0);
}
}
```
