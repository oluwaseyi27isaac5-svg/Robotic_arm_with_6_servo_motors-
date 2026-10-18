#include <Servo.h>

Servo servo1;
Servo servo2;
Servo servo3;
Servo servo4;
Servo servo5;
Servo servo6;

const int servoPin1 = 13;
const int servoPin2 = 12;
const int servoPin3 = 11;
const int servoPin4 = 7;
const int servoPin5 = 6;
const int servoPin6 = 5;

const int potPin1 = A0;
const int potPin2 = A1;
const int potPin3 = A2;
const int potPin4 = A3;
const int potPin5 = A4;
const int potPin6 = A5;

void setup() {
 
  servo1.attach(servoPin1);
  servo2.attach(servoPin2);
  servo3.attach(servoPin3);
  servo4.attach(servoPin4);
  servo5.attach(servoPin5);
  servo6.attach(servoPin6);

  Serial.begin(9600);
  Serial.println("6-Knob control ready");
}

void loop() {
 
  int pot1 = analogRead(potPin1);
  int pot2 = analogRead(potPin2);
  int pot3 = analogRead(potPin3);
  int pot4 = analogRead(potPin4);
  int pot5 = analogRead(potPin5);
  int pot6 = analogRead(potPin6);

  int angle1 = map(pot1, 0, 1023, 0, 180);
  int angle2 = map(pot2, 0, 1023, 0, 180);
  int angle3 = map(pot3, 0, 1023, 0, 180);
  int angle4 = map(pot4, 0, 1023, 0, 180);
  int angle5 = map(pot5, 0, 1023, 0, 180);
  int angle6 = map(pot6, 0, 1023, 0, 180);

  servo1.write(angle1);
  servo2.write(angle2);
  servo3.write(angle3);
  servo4.write(angle4);
  servo5.write(angle5);
  servo6.write(angle6);
<img width="935" height="512" alt="image" src="https://github.com/user-attachments/assets/2899e0b1-3e55-4638-80be-eaea4081b7ba" />
<img width="935" height="512" alt="image" src="https://github.com/user-attachments/assets/e5c5c235-1775-4c92-b392-0ea64418a812" />



  
}
