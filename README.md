# EXITRO-Emergency-evacuation-guide-robot
ESP32-based emergency evacuation guide robot with fire detection, buzzer alert, ultrasonic obstacle detection, servo scanning, and autonomous movement.
EXITRO – Emergency Evacuation Guide Robot
EXITRO is a low-cost emergency-safety robot prototype developed using ESP32. It detects fire, provides an audible alert, detects obstacles using an ultrasonic sensor, scans left and right using a servo motor, and controls robot movement through an L298N motor driver.
Features
Flame detection
Buzzer-based emergency alert
Ultrasonic obstacle detection
Servo-based left/right scanning
Automatic directional decision
DC motor control using L298N
ESP32-based embedded control
Components
ESP32
Flame sensor
HC-SR04 ultrasonic sensor
Servo motor
L298N motor driver
2 DC geared motors
Buzzer
Robot chassis
Power supply
Pin Configuration
Component
ESP32 GPIO
Flame Sensor
34
Buzzer
15
Ultrasonic TRIG
5
Ultrasonic ECHO
18
Servo
19
L298N IN1
25
L298N IN2
26
L298N IN3
27
L298N IN4
14
Important: HC-SR04 ECHO may output 5 V. Use a suitable voltage divider/level shifter before connecting it to the ESP32.
Working
ESP32 monitors the flame sensor.
When fire is detected, the buzzer gives an alert.
The robot measures the forward distance using the ultrasonic sensor.
If the path is clear, it moves forward.
If an obstacle is detected, the servo scans left and right.
The robot turns toward the side with greater clearance.
The process repeats while fire detection remains active.
Flow: Fire Detection → Alert → Distance Measurement → Obstacle Check → Direction Scan → Movement
Software
Arduino IDE
Embedded C/C++
ESP32 Arduino Core
ESP32Servo library
Limitations
This is an educational prototype. Navigation is based on simple ultrasonic distance comparison and does not provide certified real-world evacuation guidance, mapping, or shortest-path planning.
Future Scope
Voice guidance
GPS/location integration
Advanced path planning
IoT monitoring
Camera-based environment analysis
