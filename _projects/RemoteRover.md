---
layout: project
title: Robot Web Tools for Rover Control
date: March 21, 2015
image: http://i882.photobucket.com/albums/ac22/sadmani/rover_demo_day_zpsf9gqqneq.jpg
---

## Overview
The goal of this project is to control a microcontroller-based rover through an obstacle course with ROS by user input (Leap Motion, Joystick, keyboard, etc.) remotely using a web interface.

In particular, this involved using rosserial for communication of the computer with the microcontroller. Next, I had to gain a base level knowledge of html/css in order to build a web interface to control the robot.

###Major steps involved:

1. Setting up microcontroller and ROS communication through rosserial
* Write an Arduino sketch that is subscribed to a topic that will change the state of an LED when a particular letter is published to it
2. Creating a rover teleop package
* Begin with writing a keyboard teleop package
* Then, modify the package so it can be controlled with a joystick or a web interface
3. Get feed from webcam on the rover
* Use OpenCV to stream video from webcam to a ROS topic
4. Interfacing with robot web tools
* Start with getting the video feed to show up on the website
* Add arrow buttons to control movement of the rover, and the rover's camera servos
* Lastly, add controls for headlights, as well as error messages for approaching an obstacle using data from the ultrasonic sensor