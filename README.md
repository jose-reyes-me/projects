# Jose Reyes – Engineering Portfolio

Welcome to my engineering portfolio. This repository documents my work on autonomous robotic systems, with a focus on sensing, control, and mechanical integration. The primary project highlighted here is **PlowZilla**, an autonomous robot designed for the EGME 456 Messy Room Competition.

---

## 🔧 Project: PlowZilla – Messy Room Competition Robot

### Course
**EGME 456 – Introduction to Mechatronics**  
California State University, Fullerton  
Instructor: Dr. Weiss  

### Team
- Katia Maldonado  
- Isaac Hernandez  
- Jose Reyes  

---

## 📌 Project Objective
Design and program an autonomous robot capable of clearing 1 in × 1 in foam blocks from its assigned side of a 4 ft × 4 ft field within a 60-second match. The robot must:
- Detect field boundaries
- Identify its assigned side (red or blue)
- Locate and push blocks efficiently
- Operate fully autonomously

---

## 🧠 System Overview

### Mechanical System
- Aluminum chassis provided by course kit  
- Two Parallax continuous rotation servos (rear-wheel drive)  
- 3D-printed bulldozer plow designed in SolidWorks  
- Plow geometry optimized to guide blocks outward and toward the opponent side  

### Electrical System
- Arduino Uno as main controller  
- Power supplied by AA battery pack and 9V battery  
- Sensors:
  - QTI sensor for black border detection
  - TCS3200 color sensor for side identification
  - Ultrasonic sensor for block detection  

### Software System
- State-based control architecture:
  - **Roam** – patrol and search for blocks
  - **Push** – drive forward to move blocks
  - **Retreat** – back away and reorient
- Priority-based safety handling for boundary detection
- Timing-based logic for reliability and simplicity

---

## 🧭 Sensing and Control Strategy
- **Color sensor** determines the robot’s home side at startup and prevents pushing while on the opponent’s side  
- **QTI sensor** continuously monitors the black border and overrides all behaviors to prevent leaving the field  
- **Ultrasonic sensor** detects blocks within a threshold distance and triggers pushing behavior  
- Differential drive control using two continuous rotation servos  

---

## 🧪 Testing and Performance
- Bench-tested individual sensors using serial output for calibration
- Validated drivetrain motion and turning behavior
- Tested block-pushing reliability with different cube orientations
- Competition performance improved significantly after software revisions
- Final placement: **3rd overall**

---

## 📈 Design Process & Iteration
The design evolved through multiple iterations:
- Initial focus on random movement shifted to a controlled perimeter sweep strategy
- Plow geometry refined to reduce block jamming
- Software simplified to favor reliability over complexity
- Ultrasonic sensor behavior corrected to prevent avoidance of blocks
Testing heavily influenced final timing values and state transitions.

---

## 🧠 Reflection
This project strengthened my skills in:
- Embedded programming and debugging
- Sensor integration and calibration
- Mechanical design for real-world constraints
- Trade-off analysis between speed, stability, and reliability  

With more time, improvements would include enhanced path planning and more robust block detection.

---

<img src="IMG_2632.JPG" width="350"> <img src="IMG_2633.JPG" width="350"> <img src="IMG_2634.JPG" width="350"> <img src="IMG_2635.JPG" width="350">
<img src="IMG_2636.JPG" width="350"> <img src="IMG_2641.JPG" width="350">

---

## 🌐 Live Portfolio
🔗 **GitHub Pages Portfolio:**  
https://jose-reyes-me.github.io

---

## 📬 Contact
**Jose Reyes**  
Mechanical Engineering  
California State University, Fullerton  

