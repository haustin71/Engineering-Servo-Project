# Engineering-Servo-Project

## Description
The Project that we are making is a box with a hidden compartment that is powered by a servo.
The compartment will be activated through a servo powered gear system connected to two buttons.
There will be two buttons on a side pannel adn when one button is pressed the compartment will open and if the other button is pressed the compartment will close. 

## Pre Planning
We used a document to preplan the project adn we used some similar designs for the gears on onshape.
Originally we planned on making the compartment on the side and it would slide out but that was too complicated for s to do in the time period so we decided to use a simpler design where the entire one side pops with the compartment.
[Pre Planning Document](https://docs.google.com/document/d/17IYX1eEDWpDlWgT7lWwBEruMU07gdO1zY4ygfG1bPyM/edit)


## Finished Project

## Psuedo Code 
```C++
#include <Servo.h>
Servo myServo;
const int buttonPin1 = 7; // Pin for the Button #1
const int buttonPin2 = 6; // Pin for the button #2
const int servoPin = 9; //Pin for the Servo
int buttonState1 = 0;
int buttonState2 = 0;
int pos;
void setup() {
  Serial.begin(9600);
  pinMode(7, INPUT);
  pinMode(6, INPUT);
  myServo.attach(9); // attaching the servo to the pin
}

void loop() {
  buttonState1 = digitalRead(buttonPin1);
  buttonState2 = digitalRead(buttonPin2);
  if (buttonState1 == HIGH && pos < 180) {
    myServo.write(pos++);
    Serial.println("Button 1 is on");
  }
  if (buttonState2 == HIGH && pos > 0) {
    myServo.write(pos--);
    Serial.println("Button 2 is on");
  }



}
```
## Finished Circuit
![alt text](https://raw.githubusercontent.com/haustin71/Engineering-Servo-Project/main/Circuit.PNG)
## Opening Mechanism CAD File
![alt text](https://raw.githubusercontent.com/haustin71/Engineering-Servo-Project/main/Opening%20mechanism.PNG)
## Box CAD File 
![alt text](https://raw.githubusercontent.com/haustin71/Engineering-Servo-Project/main/Box.PNG)

## Reflections


