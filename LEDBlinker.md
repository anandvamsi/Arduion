## LED Blinker Program
To blink the led with delay

```bash
int led1=7;
int led2=8;

void setup() {
  // put your setup code here, to run once:
pinMode(7,OUTPUT);
pinMode(8,OUTPUT);
}

void loop() {
  // put your main code here, to run repeatedly:
digitalWrite(7,HIGH);
delay(100);
digitalWrite(7,LOW);
delay(100);
digitalWrite(8,HIGH);
delay(100);
digitalWrite(8,LOW);
delay(100);
}
```
### PinMode()
The pinMode() function in Arduino is used to configure a specified pin to behave either as an input or an output.
This function is essential when setting up the pins of your Arduino board to interact with sensors, LEDs, buttons, or other device.
```cpp
pinMode(pin, mode);
```

INPUT: Configures the pin as an input (e.g., to read a button or sensor).
OUTPUT: Configures the pin as an output (e.g., to control an LED or relay).
