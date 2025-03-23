---
title: "BarBot: Autonomous Drink Carrier"
description: "1st Year Design Project"
date: 2022-11-20
tags: ["engineering", "robotics", "automation"]
image: "/projects/barbot.png"
github: "https://github.com/csabahi/BarBot"
demo: "https://www.youtube.com/watch?v=TPw-_4b_qSk"
---

## Overview
The aim of this project was to develop an autonomous system using only the materials provided. 
Which was a Lego EV3 Mindset Kit, and mechanical lego pieces, with permittance to use custom 3D printed piece.
My group and I opted to design and develop a custom drink delivery robot, which can drive to tables, use pre-recorded voice commands,
and a custom drink tray to deliver refreshments to the table. Addressing the labour shortage across the 
service industry and integrating autonomous robotics to reduce dedundant and mundane tasks.

## Technical Details
The bot is provided a pair of drinks as well as an input as to which table to wait. Based on it's internal map of the restaurant, it travels the optimal route to the table, continuously checking for obstacles.

If an obstacle is detected, BarBot first determines whether the obstacle is stationary (ex. a dropped fork on the ground), or moving (a customer passing in front of the robot), and carries out it's next movement based on it's classification.
- If moving, wait and politely ask customer to move (using pre-recorded voice messages)
- If stationary, scan both right and left direction, and move around the object accordingly.

Once the robot arrives, it raises it's custom designed scissor lift, and asks for payment from the customers before returning back to the bar for it's next service route.

The software uses object oriented programming to classify different objects in its operation such as table numbers for route calculation, as well as sensor interfacing to detect drift cause by poor quality motors and constantly accounts for the drift to maintain a steady course.
## Features
- Height Adjustable Tray
- Custom 3D modeled and printed cup stabilizing tray
- Mathematical based acceleration and de-acceleration profiles
- 180 degree field of vision objject detection
- Object detection, classification, and avoidance routine

## Skills/Technologies Used
- C/RobotC
- Sensors (Gyro and Ultrasonic)
- Position Tracking
- Drift Correctment