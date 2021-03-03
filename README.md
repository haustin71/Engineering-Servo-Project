# Engineering-Servo-Project

## Description
The Project that we are making is a box with a hidden compartment that is powered by a servo.
The compartment will be activated through a servo powered gear system connected to two buttons.
There will be two buttons on a side pannel adn when one button is pressed the compartment will open and if the other button is pressed the compartment will close. 

## Pre Planning
We used a document to preplan the project adn we used some similar designs for the gears on onshape.
Originally we planned on making the compartment on the side and it would slide out but that was too complicated for s to do in the time period so we decided to use a simpler design where the entire one side pops with the compartment.
[Pre Planning Document](https://docs.google.com/document/d/17IYX1eEDWpDlWgT7lWwBEruMU07gdO1zY4ygfG1bPyM/edit)

## TimeLine

Jan. 20th - We started our preplanning for the project
Jan. 25th - we continued to preplan the opening mechanism
Jan. 27th - we started working on the box and specifically the walls
Feb. 1st -  We started working on the code and we finished the walls
Feb. 3rd - We continued to work on the code and we started working on the opening mechanism
Feb. 8th - we had to go back and fix the walls and the code
Feb. 10th - we finally finished the code
Feb. 15th - we fixed some minor issues with the code and the CAD
Feb. 17th - we finally finished the opening mechanism code
Feb. 22nd - we started assembling the CAD box parts and the opening mechanism
Feb. 24th - we finished the CAD assembly and we imputted the code
Mar. 1st - we updated the github and put the finishing touches on the Final Assembly

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
[Servo Code](https://create.arduino.cc/editor/rgabram93/1ecdbab5-daf2-4df3-809b-e3f6be188656/preview)

## Finished Circuit
![alt text](https://raw.githubusercontent.com/haustin71/Engineering-Servo-Project/main/Circuit.PNG)
[TinkerCAD Circuit Link](https://www.tinkercad.com/things/e483rMkaV7q-arduino-button-controlled-servo/editel)
## Opening Mechanism CAD File
![alt text](https://raw.githubusercontent.com/haustin71/Engineering-Servo-Project/main/Opening%20mechanism.PNG)
[Opening Mechanism CAD File](
## Box CAD File 
![alt text](https://raw.githubusercontent.com/haustin71/Engineering-Servo-Project/main/Box.PNG)
[Box CAD File](https://cvilleschools.onshape.com/documents/c06286c78337f0c5580730c4/w/975c7451cdb69a17290a3b26/e/252b33aa0cf3708a31f8a50d)
## Reflections
Overall we think that this project went very well but I personally think that we were a little rushed with the deadline but now we get an extension so we should finish on time. We both struggled with certain parts of the CAD and coding but we worked through those problems. We think that we work well together and when one of us had a problem we both tried to work on that problem together. Some problems that we ran into was that one of the buttons wasnt moving the servo which was fixed because the button pins were the same for both buttons so the servo only responded to the one button. The major Problem with the CAD was lining up the gear rack and the gear together with the servo and its holder. We overcame this problem by fixing the mates and adding the correct mates.  

