## farmbot GrANA


Conectando o BLDC Controller no arduino

Import the servo.h library and control it like a servo.
You need to connect ground to a ground pin on your arduino
the signal to one of the digital pins with pwm (should have ~ sign next to it). 
Change the micro seconds to between 1000 (0% throttle) and 2000 (100% throttle) 
the “2” to whichever pin you attach the signal pin to

The code lines you need to include are:

#include <Servo.h>

Servo ESC;

void setup()
{
ESC.attach(2);
}

void loop()
{
ESC.writeMicroseconds(1000);
}
