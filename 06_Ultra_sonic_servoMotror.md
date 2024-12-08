## Ultra sonic Intergration with Servo Motor.


```bash
#include <Servo.h>
Servo s1;

#define echoPin 7               // CHANGE PIN NUMBER HERE IF YOU WANT TO USE A DIFFERENT PIN
#define trigPin 6               // CHANGE PIN NUMBER HERE IF YOU WANT TO USE A DIFFERENT PIN
long duration, distance;
void setup(){
  Serial.begin (9600);
  pinMode(trigPin, OUTPUT);
  s1.attach(4);
  pinMode(echoPin, INPUT);
}
void loop(){
  digitalWrite(trigPin, LOW);
  delayMicroseconds(2);
  digitalWrite(trigPin, HIGH);
  delayMicroseconds(10);
  digitalWrite(trigPin, LOW);
  
  duration = pulseIn(echoPin, HIGH);
  distance = duration / 58.2;
  String disp = String(distance);

  Serial.print("Distance: ");
  Serial.print(disp);
  Serial.println(" cm");
  delay(1000);

  if (distance < 5)
  {
  s1.write(0);
  delay(1000);
  s1.write(90);
  delay(3000);
  s1.write(0);
  s1.write(180);
  }
}
```
