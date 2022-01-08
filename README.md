# Kerala_IOT_Challenge
Foxlab Makerspace in association with GTech - Group of Technology Companies in Kerala is launching our prestigious program “Kerala IoT Challenge 2021”, with a vision to mould 100 IoT experts in Kerala, hosting on the µLearn platform. Kerala IoT Challenge is a program designed in 4 levels followed by a hackathon to identify and train quality industry leaders in the IoT domain, while any novice learner can start with layer 1 and others can enter laterally to the desired layer after an evaluation
# About Me
Hello friends! My name is SHARAN KS and I am currently doing B.Tech in ELECTRONICS AND COMMUNICATION ENGINEERING on KMEA ENGINEERING COLLEGE EDATHALA ERNAKULAM. My areas of interests are EMBEDDED SYSTEMS, MICROCONTROLLERS, IOT, ENTREPRENEURSHIP, INNOVATIOS, MENTORING etc. I used to do small projects using Arduino and nodeMCU boards. I have filed patent on a product called Electrostatic air purifier and currently it was published. 
# Experiment 1 : Hello World LED Blinking
A basic program similar to printing "Hello World" in any programming language. The aim is to blink an LED using Arduino Uno Board. Currently I am using tinkercad an online stimulator for doing the experiments.   

Arduino Uno is an open-source microcontroller board developed by Arduino.cc. It has several advantages over the conventional microcontrollers. It comes with a pre-tested software and hardware libraries and has its own integrated development environment (IDE). Also it is less expensive & beginner friendly.

## Components Required  
* Arduino Uno Board 
* LED (Any Color) x 1 Nos
* 220 OHM Resistor X 1 Nos
* Breadboard 
* Connecting wires

## Circuit Diagram
![exp1](https://user-images.githubusercontent.com/55591996/148651893-1275868e-ccea-4fe4-81ed-7f3aa0ae51a3.PNG)



## Code

```
#define LED 8
void setup()
{
  pinMode(LED, OUTPUT);
}

void loop()
{
  digitalWrite(LED, HIGH);
  delay(1000); // Wait for 1000 millisecond(s)
  digitalWrite(LED, LOW);
  delay(1000); // Wait for 1000 millisecond(s)
}
```

## Output
 The LED is blinked with a time interval of 1 second
<iframe width="560" height="315"
src=
 https://user-images.githubusercontent.com/95869156/146654302-7499a267-e699-4476-86a8-3204b2d5c383.mp4
       
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe> 
# Experiment 2 : Traffic Light

> In the previous program, we have done the LED blinking experiment with one LED. Now, it’s time to up the stakes and do a bit more complicated experiment-traffic lights. Actually, these two experiments are similar. While in this traffic lights experiment, we use 3 LEDs with different colors rather than 1 LED. 
## Components Required 
* Arduino board X 1
* Red LED X 1
* Yellow M5 LED X 1
* Green M5 LED X 1
* 220Ω resistor X 3

## Circuit Diagram

![exp2](https://user-images.githubusercontent.com/55591996/148655120-3609e8f5-ad4a-4433-a2ca-038ed789753a.PNG)

## Code

```
#define led1 13
#define led2 12
#define led3 11
void setup()
{
  pinMode(led1, OUTPUT);
  pinMode(led2, OUTPUT);
  pinMode(led3, OUTPUT);
}

void loop()
{
  digitalWrite(led1,HIGH);
  delay(5000);
  digitalWrite(led1,LOW);
  for(int i=0;i<3;i++){
    delay(500);
    digitalWrite(led2,HIGH);
    delay(500);
    digitalWrite(led2,LOW);
    delay(500);
  }
  digitalWrite(led3,HIGH);
  delay(5000);
  digitalWrite(led3,LOW);
  delay(500);
}
```

## Output

> In Traffic light the green LED blink about 5 second, then it is turnoff. Then the yellow LED blinks 3 times with a time interval of 0.5 second.Then the red LED blink about 5 seconds. This process continues.
# Experiment 3 : LED Chasing Effect

> We often see billboards composed of colorful LEDs. They are constantly changing to form various light effects. In this experiment, we compile a program to simulate LED chasing effect. The long lead of LED is the positive side; short lead is negative.
## Components Required
* Led *6
* Arduino board *1
* 220Ω resistor *6
* Breadboard *1
* USB cable*1
* Breadboard wire *13

## Circuit Diagram

![s5yR0_3102_1627567167](https://user-images.githubusercontent.com/91405741/137292096-feb60c91-1a9a-474b-a596-300285f7b011.png)

## Code

```
int BASE = 2 ;  // the I/O pin for the first LED
int NUM = 6;   // number of LEDs
void setup()
{
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     pinMode(i, OUTPUT);   // set I/O pins as output
   }
}
void loop()
{
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     digitalWrite(i, LOW);    // set I/O pins as “low”, turn off LEDs one by one.
     delay(200);        // delay
   }
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     digitalWrite(i, HIGH);    // set I/O pins as “high”, turn on LEDs one by one
     delay(400);        // delay
   }  
}
```

## Output
