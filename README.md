# Petfeeder-code
code

#include <Servo.h>
 int pos;
  int servoPin=9;
  int servoDelay=100;
  Servo myPointer;
void setup() {

 Serial.begin(9600);
myPointer.attach(servoPin);
}

void loop() {
  // put your main code here, to run repeatedly:
for(pos=0;pos<=180;pos=pos+5)
{
 Serial.print("current position: ");
 Serial.println(pos);

  myPointer.write(pos);
  delay(servoDelay);
}

for(pos=180;pos>=0;pos=pos-5)
{
 Serial.print("current position: ");
 Serial.println(pos);

 myPointer.write(pos);
 delay(servoDelay);
}
}
