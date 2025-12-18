📦 Messy Room Autonomous Robot

EGME 456 – Introduction to Mechatronics | Fall 2025

Author: Jose Reyes
Program: B.S. Mechanical Engineering, Cal State Fullerton

🔹 Project Introduction

This project was completed as part of EGME 456: Introduction to Mechatronics and involved the design, construction, and programming of an autonomous mobile robot for the Messy Room Competition.

The objective of the competition was to autonomously reduce the number of foam cubes on the robot’s side of a shared playing field within a one-minute match. Each robot operated without human input and relied entirely on onboard sensing and control.

Our robot was designed to identify its starting field color, navigate within its half of the arena, detect and push blocks, and avoid crossing the black boundary.

🔹 System Overview

The robot is a fully integrated mechatronic system consisting of:

Mechanical Subsystem:

Two-wheel differential drive using continuous-rotation servos

Passive front support (skid/caster)

Compact chassis designed to remain within size constraints

Electrical Subsystem:

Arduino Uno microcontroller

Ultrasonic distance sensor for block detection

QTI reflectance sensor for black border detection

TCS3200 color sensor for field side identification

Battery-powered onboard electronics

Software Subsystem:

Autonomous state-based control

Sensor fusion for navigation and decision-making

Timing-based motion control

These subsystems work together to allow autonomous operation for the full competition duration.

🔹 Design & Development Process

My individual contributions focused primarily on software architecture and sensor integration.

Key development steps included:

Writing and debugging low-level motor control for continuous-rotation servos

Implementing ultrasonic distance sensing for small (1 in × 1 in) foam cubes

Integrating the TCS3200 color sensor to determine the robot’s home side

Iteratively refining control logic to eliminate unstable behaviors such as uncontrolled spinning

Several iterations were required to balance forward motion, scanning behavior, and boundary avoidance without violating competition rules.

🔹 Sensing and Control Strategy

The robot’s autonomous behavior is organized around a simple state machine:

1. Startup / Initialization

A 2-second delay allows sensor stabilization

The color sensor detects whether the robot starts on the red or blue half

The detected color is stored as our side, with the opposite color designated as the opponent’s side

2. Sweep and Push

The robot drives forward across its half of the field

The ultrasonic sensor detects nearby blocks

When a block is detected, the robot pushes it forward

3. Boundary Avoidance

If the QTI sensor detects the black border:

The robot immediately stops

Reverses for 2 seconds

Turns around

Resumes sweeping within its side

This strategy prioritizes simplicity, robustness, and repeatability over complex planning.

🔹 Testing and Performance

Testing was conducted both on benchtop setups and on a mock competition field.

Key results:

Reliable detection of the black boundary using the QTI sensor

Consistent forward motion without uncontrolled spinning

Successful detection and displacement of foam cubes

Stable autonomous operation for the full match duration

While cube-clearing efficiency varied depending on initial cube distribution, the robot met all competition requirements and passed technical inspection.

🔹 Reflection

This project reinforced the importance of:

Incremental testing and debugging

Simple, well-structured control logic

Understanding real-world sensor limitations

Given additional time, improvements could include:

More efficient sweeping patterns

Improved cube engagement geometry

Sensor filtering for increased reliability

Overall, the project strengthened my skills in embedded systems, robotics integration, and practical autonomous control.

🔹 Media and Documentation

📷 Photos and videos: (add links here)

💻 Source code: (this repository)

📐 CAD models: (add link if applicable)

🔗 Repository Contents
/src        → Arduino source code
/docs       → Project documentation
/media      → Images and videos
README.md   → Project overview (this file)

📌 Course Information

Course: EGME 456 – Introduction to Mechatronics
Institution: California State University, Fullerton
Semester: Fall 2025
