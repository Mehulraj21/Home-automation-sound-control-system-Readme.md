Voice-Controlled-Home-automation-System 🎙️🏠⚙️  


A basic voice controlled home automation system by interfacing python with Arduino UNO board.

Experience the future of home management with VoiceHomeLink, an avant-garde home automation system. This cutting-edge solution seamlessly merges Python, Embedded C, and Arduino Uno board technology, transforming your voice commands into orchestrated actions. Interact with your home like never before, using just your voice to control a symphony of devices. With an array of sensors and actuators, VoiceHomeLink ensures precise execution of your commands, creating a harmonious living environment. Simplify your life and amplify your control with VoiceHomeLink, where innovation meets everyday convenience

Problem Statements 📌 & Abstract 📝
The aim of this project is to develop a voice-based home automation system using Arduino with Python using the Standard Firmata library. The system should allow users to control their home appliances and devices using voice commands, providing an intuitive and convenient way to interact with their home automation system. The system should be easy to use and reliable, allowing users to turn on/off lights, fans, ACs, and other home appliances using simple voice commands. The system should be designed to be scalable and flexible, allowing users to add or remove devices as per their requirements. The primary objective of this project is to develop a robust and efficient system that improves the user experience of home automation systems and simplifies the user's interactions with their home appliances.

🎯Objectives ➡️
The objectives of this project are:

To develop a voice-based home automation system that allows users to control their home appliances and devices using simple voice commands.
To develop a scalable and flexible system that can be easily modified or expanded as per user requirements.
To develop a reliable and energy-efficient system that reduces energy consumption and operating costs.
To provide a cost-effective and sustainable solution for home automation that is accessible to a wider range of users.
To showcase the use of Arduino with Python using the Standard Firmata library for developing home automation systems.
To learn and apply the principles of voice recognition, microcontroller programming, and software-hardware integration.

Hardware & Software Requirements (Technology & Tools)💻➡️


Arduino UNO R3 Board

![image](https://github.com/user-attachments/assets/638390d9-0736-4acd-8ec8-4f4600f2272e)


Bread Board




![image](https://github.com/user-attachments/assets/6b9ff050-5020-45bd-a497-c67b7382d79a)


Wire Connectors



![image](https://github.com/user-attachments/assets/2e1a3df4-f2ac-4ca2-b02e-0143c33874cb)



Relay Module



![image](https://github.com/user-attachments/assets/678ef259-4b00-46cf-ac2b-32c4966a4bae)


Sound sensor


![image](https://github.com/user-attachments/assets/baf7ec21-4945-4a75-8a7b-548dbcf69004)



SMD RGB Light Module




![image](https://github.com/user-attachments/assets/f04f497a-aa42-4bb3-a735-4d5f3ec1c649)



Python



![image](https://github.com/user-attachments/assets/7d583efd-9865-4ac2-9ea4-8d38b4ebe2e9)


Arduino IDE



![image](https://github.com/user-attachments/assets/f039a0d9-61dc-4276-b498-9fe904e06bea)


Explanation of codes:


Include SoftwareSerial Library:

#include <SoftwareSerial.h>: Adds support for serial communication via software-defined pins.
Variable Declaration:

String value;: Stores received commands from the Bluetooth module.
int TxD = 11, RxD = 10;: Define pins for Bluetooth TX and RX communication.
SoftwareSerial Object:

SoftwareSerial bluetooth(TxD, RxD);: Creates a SoftwareSerial object named bluetooth.
Setup Function:

pinMode(2, OUTPUT); and pinMode(3, OUTPUT);: Set pins 2 and 3 as outputs for controlling LEDs.
Serial.begin(9600);: Starts serial communication with the computer at 9600 bps.
bluetooth.begin(9600);: Initializes Bluetooth communication at 9600 bps.
Loop Function:

if (bluetooth.available()): Checks if data is received from the Bluetooth module.
value = bluetooth.readString();: Reads the incoming command and stores it in value.
Command Processing: Based on the received value, specific actions are performed:

"all LED turn on": Turns on LEDs connected to pins 2 and 3.
"all LED turn off": Turns off LEDs connected to pins 2 and 3.
"turn on Red LED": Turns on the LED on pin 2.
"turn on green LED": Turns on the LED on pin 3.
"turn off red LED": Turns off the LED on pin 2.
"turn off green LED": Turns off the LED on pin 3.
"turn off all devices": Turns off LEDs on pins 2, 3, and also pin 4 (though pin 4 is not explicitly set up).
"time to party": Creates a blinking pattern where the LEDs alternate between on and off states for 60 iterations with a 250ms delay.
This code allows for controlling LEDs via Bluetooth commands and includes a fun "party mode" with a blinking pattern.

