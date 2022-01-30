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
* USB Cable x 1
* RGB LED x 1
* 220ohm Resistor x 3
* Breadboard jumper wire x 4

## Circuit Diagrams
![xX9cw_3102_1628160649](https://user-images.githubusercontent.com/91405741/137347719-6966c0b1-021d-471c-b0a7-48d0441752d0.png)

![A8a40_3102_1628160631](https://user-images.githubusercontent.com/91405741/137347782-e0a8a008-8706-4b7c-ba31-38ef0ab6ca72.png)

![TefdI_3102_1628167200](https://user-images.githubusercontent.com/91405741/137347822-228ccf9c-3a89-45ba-bb24-c3b0ee587818.png)


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
![IMG_20220128_233655-min_11zon](https://user-images.githubusercontent.com/55591996/151602025-26de7f58-2c93-424c-aa56-eb6f6ec47fbf.jpg)
## Experiment 7 : LDR Light Sensor

> An experiment to understand the working of an LDR light Sensor.
### LDR : Light Dependent Sensor
> Photo Resistor (Photovaristor) is a resistor whose resistance varies from different incident light strength. It's based on the photoelectric effect of semiconductor. If the incident light is intense, its resistance reduces; if the incident light is weak, the resistance increases.
## LDR

![L5Iw9_3102_1628755894](https://user-images.githubusercontent.com/91405741/138436746-d1cfb008-0d90-4754-b4c4-fe133329c8b5.png)

## Components Required

* Arduino Uno Board
* LDR module x 1
* GREEN LED x 1
* Breadboard x 1
* Breadboard Jumper Wire x 6
* USB cable x 1

## Circuit Diagrams
![image](https://user-images.githubusercontent.com/55591996/151673336-172ff2c3-6b7b-4ab3-af6f-ca861e5b4bb1.png)

## Code

```
#define ldr A0
#define led 3
int x;
void setup() {
  pinMode(ldr, INPUT);
  pinMode(led, OUTPUT);
  Serial.begin(9600);
}
void loop() {
  x=analogRead(ldr);
  Serial.println(x);
  if(x>=1000){
    digitalWrite(led,HIGH);
    Serial.println("HIGH");
  }
  else{
    digitalWrite(led,LOW);
    Serial.println("LOW");
  }
  }

```

## Output

![IMG_20220130_000424-compressed](https://user-images.githubusercontent.com/55591996/151673634-3124b838-421a-4318-8939-9015be7af1de.jpg)
![IMG_20220130_000416-compressed](https://user-images.githubusercontent.com/55591996/151673658-89e2b2e0-2731-4378-b996-343d5c90c469.jpg)

## Experiment 8 : Flame Sensor

> An experiment to understand the working of a flame sensor

## Flame Sensor

![IDVWv_3102_1628756405](https://user-images.githubusercontent.com/55591996/151690789-70672b9b-bf4a-4714-8f4c-48bf1995c62d.png)

## Components Required
* Arduino Uno
* Flame sensor x 1
* Breadboard x 1
* Jumper wire x 7
* buzzer x 1
* GREEN LED x 1
* RED LED x 1
* 10k Resistor x 1

## Circuit Diagrams

![gI9NP_3102_1628756600](https://user-images.githubusercontent.com/55591996/151690868-ae0d09fd-c798-42e0-a970-07ab95cede64.png)
![1WFNu_3102_1628756689](https://user-images.githubusercontent.com/55591996/151690874-8cd02018-d350-4e8d-8297-2f5998956fda.png)


## Code

```
#define IR A0
#define buzz 2
#define led1 3
#define led2 4
int x=0;
void setup() {
  pinMode(IR,INPUT);
  pinMode(buzz,OUTPUT);
  pinMode(led1,OUTPUT);
  pinMode(led2,OUTPUT);
  Serial.begin(9600);
  }

void loop() {
  x=analogRead(IR);
  delay(1000);
  Serial.println(x);
  if (x>=200){
    digitalWrite(buzz,HIGH);
    digitalWrite(led1,HIGH);
    digitalWrite(led2,LOW);
  }
  else{
    digitalWrite(buzz,LOW);
    digitalWrite(led2,HIGH);
    digitalWrite(led1,LOW);
  }
}
```

## Output

![IMG_20220130_124940-compressed](https://user-images.githubusercontent.com/55591996/151690975-8bd5f168-60e7-486d-b027-d29bb5c100be.jpg)
![IMG_20220130_125007-compressed](https://user-images.githubusercontent.com/55591996/151690978-21ac7932-87ec-422e-9112-0b6108e3f2ba.jpg)

## Experiment 9 : LDR Light Sensor

> An experiment to understand the working of an LM35 temperature Sensor.
### LM35 : Temperature Sensor
>LM35 is a widely used temperature sensor with many different package types. At room temperature, it can achieve the accuracy of ±1/4°C without additional calibration processing.

LM35 temperature sensor can produce different voltage by different temperature
When temperature is 0 ℃, it outputs 0V; if increasing 1 ℃, the output voltage will increase 10 mv.
## LM35
![ZAgaD_3102_1628756936](https://user-images.githubusercontent.com/55591996/151696955-95fe5f7c-0135-4473-a749-176059182951.png)
![3ZHjl_3102_1628757013](https://user-images.githubusercontent.com/55591996/151696973-b93b9154-405d-4f03-9f4b-5735642f37b1.png)

## Components Required

* Arduino Uno Board
* LM35 x 1
* GREEN LED x 1
* RED LED x 1
* Breadboard x 1
* Conneting wires
* Buzzer x 1

## Circuit Diagrams
![ISH66_3102_1628757240](https://user-images.githubusercontent.com/55591996/151697013-df2d6407-13a9-489c-80ba-d55fb8c82992.png)

## Code

```
#define sensor A0
int LEDR=4;
int LEDG=3;
int BUZZ=1;

void setup()
{
  pinMode(LEDR, OUTPUT);
  pinMode(LEDG, OUTPUT);
  pinMode(BUZZ,OUTPUT);

}
  void loop(){
    int reading = analogRead(sensor);
    float voltage = reading * (5.0 / 1024.0);
    float temp = (voltage - 0.5) * 100;
  
  if(temp<=50)
  {
     digitalWrite(LEDR,LOW);
    digitalWrite(LEDG,HIGH);
    digitalWrite(BUZZ,LOW);
  
  }
  else{
     digitalWrite(LEDG,LOW);
     digitalWrite(LEDR,HIGH);
      digitalWrite(BUZZ,HIGH);
 
   }
}

  
                                 

```

## Output

![1](https://user-images.githubusercontent.com/55591996/151697054-4e2df17b-b741-49d9-823d-d90c32635ae3.PNG)


## Experiment 10 : IR Remote Control Using TSOP

> An experiment to understand the working of TSOP1738.
### TSOP1738 :  IR Receiver Module
>The signal from the infrared remote controller is a series of binary pulse code. To avoid the other infrared signal interference during the wireless transmission, the signal is pre-modulated at a specific carrier frequency and then send out by an infrared emission diode. The infrared receiving device needs to filter out other waves and receive signals at that specific frequency and to modulate it back to binary pulse code, known as demodulation.
## TSOP1738
![image](https://user-images.githubusercontent.com/55591996/151707408-f39d11f9-cd72-40a0-bfc9-263f3508100e.png)

## Components Required

* Arduino Uno Board
* TSOP1738 x 1
* GREEN LED x 2
* RED LED x 2
* YELLOW LED x 2
* Breadboard x 1
* Jumper wires x 10
* Remote x 1

## Circuit Diagrams
![ftiO8_3102_1629369813](https://user-images.githubusercontent.com/55591996/151707484-4938121b-6107-4243-9161-ae8b4b786cf4.png)

## Code

```
#include <IRremote.h>
int RECV_PIN = 11;
int LED1 = 2;
int LED2 = 3;
int LED3 = 4;
int LED4 = 5;
int LED5 = 6;
int LED6 = 7;
long on1  = 0x00FF6897;
long off1 = 0x00FF9867;
long on2 = 0x00FFB04F;
long off2 = 0x00FF30CF;
long on3 = 0x00FF18E7;
long off3 = 0x00FF7A85;
long on4 = 0x00FF10EF;
long off4 = 0x00FF38C7;
long on5 = 0x00FF5AA5;
long off5 = 0x00FF42BD;
long on6 = 0x00FF4AB5;
long off6 = 0x00FF52AD;
IRrecv irrecv(RECV_PIN);
decode_results results;
// Dumps out the decode_results structure.
// Call this after IRrecv::decode()
// void * to work around compiler issue
//void dump(void *v) {
//  decode_results *results = (decode_results *)v
void dump(decode_results *results) {
  int count = results->rawlen;
  if (results->decode_type == UNKNOWN) 
    {
     Serial.println("Could not decode message");
    } 
  else 
   {
    if (results->decode_type == NEC) 
      {
       Serial.print("Decoded NEC: ");
      } 
    else if (results->decode_type == SONY) 
      {
       Serial.print("Decoded SONY: ");
      } 
    else if (results->decode_type == RC5) 
      {
       Serial.print("Decoded RC5: ");
      } 
    else if (results->decode_type == RC6) 
      {
       Serial.print("Decoded RC6: ");
      }
     Serial.print(results->value, HEX);
     Serial.print(" (");
     Serial.print(results->bits, DEC);
     Serial.println(" bits)");
   }
     Serial.print("Raw (");
     Serial.print(count, DEC);
     Serial.print("): ");
 for (int i = 0; i < count; i++) 
     {
      if((i%2)==1){
      Serial.print(results->rawbuf[i]*USECPERTICK, DEC);
     } 
    else  
     {
      Serial.print(-(int)results->rawbuf[i]*USECPERTICK, DEC);
     }
    Serial.print(" ");
     }
      Serial.println("");
     }
void setup()
 {
  pinMode(RECV_PIN, INPUT);   
  pinMode(LED1, OUTPUT);
  pinMode(LED2, OUTPUT);
  pinMode(LED3, OUTPUT);
  pinMode(LED4, OUTPUT);
  pinMode(LED5, OUTPUT);
  pinMode(LED6, OUTPUT);  
  pinMode(13, OUTPUT);
  Serial.begin(9600);
   irrecv.enableIRIn(); // Start the receiver
 }
int on = 0;
unsigned long last = millis();
void loop() 
{
  if (irrecv.decode(&results)) 
   {
    // If it's been at least 1/4 second since the last
    // IR received, toggle the relay
    if (millis() - last > 250) 
      {
       on =!on;
//       digitalWrite(8, on ? HIGH : LOW);
       digitalWrite(13,on?HIGH:LOW);
       dump(&results);
      }
    if (results.value == on1 )
       digitalWrite(LED1, HIGH);
    if (results.value == off1 )
       digitalWrite(LED1, LOW); 
    if (results.value == on2 )
       digitalWrite(LED2, HIGH);
    if (results.value == off2 )
       digitalWrite(LED2, LOW); 
    if (results.value == on3 )
       digitalWrite(LED3, HIGH);
    if (results.value == off3 )
       digitalWrite(LED3, LOW);
    if (results.value == on4 )
       digitalWrite(LED4, HIGH);
    if (results.value == off4 )
       digitalWrite(LED4, LOW); 
    if (results.value == on5 )
       digitalWrite(LED5, HIGH);
    if (results.value == off5 )
       digitalWrite(LED5, LOW); 
    if (results.value == on6 )
       digitalWrite(LED6, HIGH);
    if (results.value == off6 )
       digitalWrite(LED6, LOW);        
    last = millis();      
irrecv.resume(); // Receive the next value
  }
}                          

```

## Output

![IMG_20220130_185551-compressed](https://user-images.githubusercontent.com/55591996/151707820-fd820669-ffcc-4b37-8e13-6f737ce635bf.jpg)

![IMG_20220130_185623-compressed](https://user-images.githubusercontent.com/55591996/151708608-aa11bde5-95df-4295-be71-00c48d27ee14.jpg)

>When I press the 2nd button on the remote the red LED will glow. And when I pess the next button the RED light will turn off. Like wise all the LED can be turned on and off using the IR receiver and transmitter. 

