# Human Follower Robot

## Overview
This project is a simple Human Follower Robot using an ultrasonic sensor and infrared sensors. The robot follows a human within a certain distance range while avoiding obstacles. It is controlled using an Arduino board and DC motors.

## Components Required
- Arduino Uno
- Ultrasonic Sensor (HC-SR04)
- IR Sensors (Left and Right)
- Motor Driver Module (L298N or similar)
- DC Motors (2x)
- Power Supply (Battery pack)
- Jumper Wires

## Circuit Connections
### Motor Driver Connections:
- **EN1 (Enable 1):** Pin 5 (PWM)
- **EN2 (Enable 2):** Pin 6 (PWM)
- **Motor 1 Control:**
  - IN1: Pin 7
  - IN2: Pin 8
- **Motor 2 Control:**
  - IN3: Pin 9
  - IN4: Pin 10

### Ultrasonic Sensor (HC-SR04):
- **Trig Pin:** Pin 11
- **Echo Pin:** Pin 12

### Infrared Sensors:
- **Left Sensor:** A0
- **Right Sensor:** A1

## Code Explanation
- The robot continuously measures the distance from an object using the ultrasonic sensor.
- The IR sensors detect obstacles and human presence.
- Based on sensor readings, the robot decides whether to move forward, turn left, turn right, or stop.

### Movement Logic:
1. **Move Forward:** If both IR sensors detect a person and the distance is within 5-25 cm.
2. **Turn Right:** If only the left IR sensor detects a person.
3. **Turn Left:** If only the right IR sensor detects a person.
4. **Stop:** If no person is detected or if the distance is out of range.

## Installation and Usage
1. Connect all components as per the wiring diagram.
2. Upload the provided Arduino code to your Arduino board.
3. Power the system using a battery pack.
4. The robot will start following a human within the specified range.

## Troubleshooting
- **Robot does not move:** Check motor connections and power supply.
- **Robot does not detect objects:** Ensure the ultrasonic sensor is correctly wired and facing forward.
- **Erratic movement:** Adjust sensor positioning and check sensor values using the Serial Monitor.

## Future Improvements
- Implement PID control for smoother movement.
- Add more sensors for better obstacle detection.
- Integrate a camera module for more accurate human detection.



