---
title: "Robotic Surgical Skull Cutting!"
description: "Term project during internship at The PCIGITI Lab at SickKids"
date: 2025-07-31
tags: ["surgical robotics", "controls", "pHRI"]
image: "/projects/rabt.png"
github: "https://youtu.be/8pv8ENcGmts" #can put a link to the paper once submitted
demo: "https://youtu.be/8pv8ENcGmts"
---
## Note
Due to confidentiality agreement, my work cannot be expressed in detail until our paper has been accepted to the conference ~ Jan 2026. Hence the github link goes to the demo video

## Overview
The goal of this project was to provide a reliable robotic solution to collaborative Craniosynostosis operations in fetal patients. Prior work can be found in the [paper linked](https://journals.lww.com/prsgo/fulltext/2025/05001/56__development_and_characterization_of_a_cranial.54.aspx)


The system is comprised of the custom tendon driven continuum/snake mechanism, connected to a Franka Research 3 serial robotic arm. Using the respective sensors and motors for the combined robotic system paired with a ROS middleware, it was possible to create a fully functioning User Interface for and low-level controls suite for both teleoperation thourgh mouse and keyboard, as well as collaborative movement through a force-guided controller.

## Technical Details
- System Modelling: To develop a useful and realistic force guided controller a 2nd order model was used to create virtual mass and damping to adjust the feel and sensitivity of the robot's motion to the user force input.

- Sensor Interfacing: Using different sensors in the control loop for accurate results involved post-processing such as filtering and smoothing, as well as applying wrench transformations to backwards solve input force based on the measurement sensor positioning.

- Motor Drivers/Robot Interfaces: To properly send commands from the User Interface for either Teleoperation or Shared control, proper interfaces and layers were designed so make the user interface agnostic to operation mode (Sim/Real/Dig. Twin) while maintaining a real-time system with no delays and minimal overhead on process threads for different functions


## Results
The results of the findings showed promising and accurate results with a generally low and acceptable error, with repeatable and predictable solutions. Further testing and results regarding the system will be found in the paper submission - once public.

## Skills/Technologies Used
- Python
- C++
- ROS
- libfranka
- Jax
- Scipy
- Numpy