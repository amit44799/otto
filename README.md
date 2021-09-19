# otto
#include <Servo.h>
Servo rightLeg, leftLeg, rightFoot, leftFoot;
 int trig = 9;
  int Echo = 10;
  long duration;
  int distance;
void setup() 
{
  Serial.begin(115200);
  rightLeg.attach(5);
  leftLeg.attach(4);
  rightFoot.attach(7);
  leftFoot.attach(6);
 
  #define PIN_Buzzer 8;
  #define MAXIMUM_DISTANCE 100
 
  pinMode(trig, OUTPUT);
  pinMode(Echo, INPUT);
  rightLeg.write(90);
  leftLeg.write(90);
  rightFoot.write(90);
  leftFoot.write(90);
  
}

void loop() {
digitalWrite(trig, LOW);
delay(2);
digitalWrite(trig, HIGH);
delayMicroseconds(10);
digitalWrite(trig, LOW);
duration = pulseIn(Echo, HIGH);
Serial.print("Distance: ");
Serial.println(duration);
if ( duration <= 300   )

  {
  rightLeg.write(90);
  leftLeg.write(90);
  rightFoot.write(85);
  leftFoot.write(125);
  delay(1000);

  rightLeg.write(90);
  leftLeg.write(90);
  rightFoot.write(55);
  leftFoot.write(85);
  delay(1000);

    rightLeg.write(120);
  leftLeg.write(90);
  rightFoot.write(85);
  leftFoot.write(95);
  delay(1000);

    rightLeg.write(90);
  leftLeg.write(60);
  rightFoot.write(85);
  leftFoot.write(95);
  delay(1000);

     rightLeg.write(90);
  leftLeg.write(90);
  rightFoot.write(85);
  leftFoot.write(125);
  delay(1000);

   rightLeg.write(90);
  leftLeg.write(90);
  rightFoot.write(55);
  leftFoot.write(95);
  delay(1000);
  
    rightLeg.write(120);
  leftLeg.write(90);
  rightFoot.write(85);
  leftFoot.write(95);
  delay(1000);

   rightLeg.write(60);
  leftLeg.write(90);
  rightFoot.write(85);
  leftFoot.write(95);
  delay(1000);
  
     rightLeg.write(90);
  leftLeg.write(90);
  rightFoot.write(85);
  leftFoot.write(55);
  delay(1000);

   rightLeg.write(90);
  leftLeg.write(90);
  rightFoot.write(125);
  leftFoot.write(95);
  delay(1000);
  
    rightLeg.write(120);
  leftLeg.write(90);
  rightFoot.write(85);
  leftFoot.write(95);
  delay(1000);

   rightLeg.write(60);
  leftLeg.write(90);
  rightFoot.write(85);
  leftFoot.write(95);
  }
  else
  {
    rightLeg.write(90);
  leftLeg.write(90);
  rightFoot.write(85);
  leftFoot.write(95);
  delay(1000);

   rightLeg.write(90);
  leftLeg.write(90);
  rightFoot.write(85);
  leftFoot.write(95);
  delay(1000);
  
 
  
  }
  
}
