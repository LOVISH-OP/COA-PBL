# COA-PBL
Here's my computer architecture and organisation lab PBL (project based learning) which i have maded in semester 5 


🌟 Overview

This project implements a real-time, three-tiered proximity detection system using an Arduino Uno and an HC-SR04 ultrasonic sensor. Its primary function is to continuously measure the distance to the nearest obstacle and provide immediate, color-coded visual and audible alerts to the user, enhancing safety and situational awareness in close quarters.

The system classifies proximity into three distinct safety zones:

    Green: Safe Distance

    Yellow: Warning/Caution Distance

    Red + Buzzer: Critical Danger Zone

⚙️ How It Works (Working Principle)

The system operates using the principle of sonar (Sound Navigation and Ranging), specifically measuring the Time-of-Flight (ToF):

    The Arduino sends a brief electrical pulse (Trigger).

    The HC-SR04 sensor converts this pulse into an 8-cycle burst of 40 kHz ultrasonic sound.

    The sound wave travels to the nearest object and reflects back (Echo).

    The Arduino measures the total time (t) the sound took for the round trip.

    The distance (D) is calculated using the formula:
    D=2t×Speed of Sound​

    (In the code, this is simplified to Distance(cm)=Time(μs)/58)

    This calculated distance is compared against the pre-set thresholds to activate the corresponding outputs.

🛠️ Components and Materials

Hardware Requirements

Component	Quantity	Purpose
Arduino UNO R3	1	Microcontroller (The brain)
HC-SR04 Ultrasonic Sensor	1	Distance Measurement
LEDs (Red, Yellow, Green)	3	Visual Status Indicators
Piezo Buzzer (5V)	1	Audible Alarm
Resistors (220Ω)	3	Current limiting for LEDs
Mini Breadboard	1	Prototyping
Jumper Wires (M-M)	∼10	Connections
