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
* Connecting wires

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
* Led X 6
* Arduino board X 1
* 220Ω resistor X 6
* Breadboard X 1
* Connecting wires

## Circuit Diagram

![exp 3](https://user-images.githubusercontent.com/55591996/148656072-3079c4e4-d35c-48d1-9515-521e977dfc3b.PNG)

## Code

```
#define pin 2
#define num 6
void setup()
{
  for(int i=pin;i<pin+num;i++){
   pinMode(i,OUTPUT); 
  }
}

void loop()
{
  for(int i=pin;i<pin+num;i++){
   digitalWrite(i,HIGH);
   delay(200); 
  }
  for(int i=pin;i<pin+num;i++){
   digitalWrite(i,LOW);
   delay(200);
  }
}
```

## Output
# Experiment 4 : Button Controlled LED

> An experiment to light an LED using a Push Button.
## Components Required 
* Arduino Uno
* Button switch x 1
* Red M5 LED x 1
* 220ΩResistor x 1
* 10KΩ Resistor x 1
* Breadboard x 1
* Connection wires

## Circuit Diagrams

![image](https://user-images.githubusercontent.com/55591996/148673943-4e88b419-ef66-4436-bfd3-809f56dfd5e3.png)

![exp4](https://user-images.githubusercontent.com/55591996/148674078-1369d46f-8f98-4c64-bb7b-6f9c8eb29bbf.PNG)
## Code

```
#define led 10
#define button 7
int x;
void setup()
{
  Serial.begin(9600);
  pinMode(led, OUTPUT);
  pinMode(button, INPUT);
}

void loop()
{
  x=digitalRead(button);
  Serial.println(x);
 
  if(x==LOW){
    digitalWrite(led, HIGH);
  }
  else{
    digitalWrite(led, LOW);
  }
}
```
## Output

> When the push button is pressed the LED is turned on otherwise it is off.
<iframe width="560" height="315"
src=

https://user-images.githubusercontent.com/95869156/147783915-ff390cb5-625e-48bd-8ccb-b578c90629de.mp4


frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Experiment 5 : Buzzer

> An experiment to understand the working of a buzzer.
## Components Required
* Arduino Uno
* Buzzer x 1
* Breadboard x 1
* Connecting wires

## Circuit Diagrams

![e9Pdc_3102_1628160446](https://user-images.githubusercontent.com/91405741/137346912-0f871dbf-8e86-4734-a337-fceeff454e33.png)
![exp 5](https://user-images.githubusercontent.com/55591996/148674461-7abb33b8-9be7-4b4e-9edb-6a666fd440e9.PNG)


## Code

```
#define buz 3
void setup()
{
  pinMode(buz, OUTPUT);
}

void loop()
{
  digitalWrite(buz, HIGH);
  delay(1000);
  digitalWrite(buz, LOW);
  delay(1000); 
}
```

## Output

> The Buzzer makes beep sound.
<iframe width="560" height="315"
src=
https://user-images.githubusercontent.com/95869156/147783940-03ee47a1-cac0-42e9-bd27-b81fb6b48179.mp4

frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Experiment 6 : RGB LED

> An experiment to understand the working of a RGB LED.
## Components Required
* Arduino Uno
* USB Cable * 1
* RGB LED * 1
* Resistor *3
* Breadboard jumper wire*5

## Circuit Diagrams
![xX9cw_3102_1628160649](https://user-images.githubusercontent.com/91405741/137347719-6966c0b1-021d-471c-b0a7-48d0441752d0.png)

![A8a40_3102_1628160631](https://user-images.githubusercontent.com/91405741/137347782-e0a8a008-8706-4b7c-ba31-38ef0ab6ca72.png)

![TefdI_3102_1628167200](https://user-images.githubusercontent.com/91405741/137347822-228ccf9c-3a89-45ba-bb24-c3b0ee587818.png)
![IMG_20211231_001727](https://user-images.githubusercontent.com/95869156/147783842-52738376-a9c3-4612-8eec-d67cc0b08d5a.jpg)

## Code

```
int redpin = 11; //select the pin for the red LED
int bluepin =10; // select the pin for the blue LED
int greenpin =9;// select the pin for the green LED
int val;
void setup() {
  pinMode(redpin, OUTPUT);
  pinMode(bluepin, OUTPUT);
  pinMode(greenpin, OUTPUT);
  Serial.begin(9600);
}
void loop() 
{
for(val=255; val>0; val--)
  {
   analogWrite(11, val);
   analogWrite(10, 255-val);
   analogWrite(9, 128-val);
   delay(1); 
  }
for(val=0; val<255; val++)
  {
   analogWrite(11, val);
   analogWrite(10, 255-val);
   analogWrite(9, 128-val);
   delay(1); 
  }
 Serial.println(val, DEC);
}
```

## Output

> The RGB LED blinks.
<iframe width="560" height="315"
src=
https://user-images.githubusercontent.com/95869156/147783968-7e6f1a33-a312-44d9-b7cb-fac464fc960c.mp4

frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

## Experiment 7 : LDR Light Sensor

> An experiment to understand the working of an LDR light Sensor.
### LDR : Light Dependent Sensor
> Photo Resistor (Photovaristor) is a resistor whose resistance varies from different incident light strength. It's based on the photoelectric effect of semiconductor. If the incident light is intense, its resistance reduces; if the incident light is weak, the resistance increases.
## Circuit Diagrams

![L5Iw9_3102_1628755894](https://user-images.githubusercontent.com/91405741/138436746-d1cfb008-0d90-4754-b4c4-fe133329c8b5.png)
![IMG_20211231_005943](https://user-images.githubusercontent.com/95869156/147783874-b2e4e58e-b164-4542-9276-fe35254b3221.jpg)

## Components Required

* Arduino Uno Board
* Photo Resistor*1
* Red M5 LED*1
* 10KΩ Resistor*1
* 220Ω Resistor*1
* Breadboard*1
* Breadboard Jumper Wire*7
* USB cable*1

## Circuit Diagrams
![schema_Myt5vqqplZ](https://user-images.githubusercontent.com/91405741/138436635-60cb2ec4-091d-4f24-bf96-b0289e06fa00.png)

## Procedure

* Connect the 3.3v output of the Arduino to the positive rail of the breadboard
* Connect the ground to the negative rail of the breadboard
* Place the LDR on the breadboard
* Attach the 10K resistor to one of the legs of the LDR
* Connect the A0 pin of the Arduino to the same column where the LDR and resistor is connected (Since the LDR gives out an analog voltage, it is connected to the analog input pin on the Arduino. The Arduino, with its built-in ADC (Analog to Digital Converter), then converts the analog voltage from 0-5V into a digital value in the range of 0-1023). - Now connect the other end of the 10K resistor to the negative rail
* And the the second (free) leg of the LDR to the positive rail
Pretty much this is what we need for the light sensing. Basic circuits like this can be done without an Arduino aswell. However, if you want to log the values and use it to create charts, run other logics etc. I will recomend an Arduino or ESP8266 or may be a ESP32 for this.
Now, as we want our circuit to do something in the real world other than just displaying the values on the computer screen we will be attaching a LED to the circuit. The LED will turn on when its dark and will go off when its bright. To achieve this we will:
* Place the LED on the breadboard
* Connect the 220ohm resistor to the long leg (+ve) of the LED
* Then we will connect the other leg of the resistor to pin number 13 (digital pin) of the Arduino
* and the shorter leg of the LED to the negative rail of the breadboard

## Code

```
const int ledPin = 10;
const int ldrPin = A0;
void setup() {
Serial.begin(9600);
pinMode(ledPin, OUTPUT);
pinMode(ldrPin, INPUT);
}
void loop() {
int ldrStatus = analogRead(ldrPin);
if (ldrStatus >= 500) {
digitalWrite(ledPin, HIGH);
Serial.print("Its DARK, Turn on the LED : ");
Serial.println(ldrStatus);
} else {
digitalWrite(ledPin, LOW);
Serial.print("Its BRIGHT, Turn off the LED : ");
Serial.println(ldrStatus);
}
}
```

## Output

<iframe width="560" height="315"
src=

https://user-images.githubusercontent.com/95869156/147783995-b962eab1-095c-4c26-8885-e16e8e354f0e.mp4

frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

## Experiment 8 : Flame Sensor
