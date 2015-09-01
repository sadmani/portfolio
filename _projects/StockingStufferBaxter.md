---
layout: project
title: Stocking Stuffer Baxter
date: December 10, 2014
image: http://i882.photobucket.com/albums/ac22/sadmani/baxter2image1_zpsureqj4sj.png
---

## Overview
The goal of this project was to use the Baxter robot (research model) by [Rethink Robotics](http://www.rethinkrobotics.com/) to fill stockings for the MSR 2015 cohort- just in time for the Holidays! This project involved using ROS and Python to use the inverse kinematics server by Rethink, as well as perform tag tracking and object recognition tasks.

To fit this project into our two week final project timeframe, our team of four started small by placing four different colored blocks on a table in front of baxter, with stockings labelled with tags hanging to the left of Baxter; we had ideas for extensions to add to this base level as we accomplished tasks. The full overview of the project can be seen on Github using this [link](https://github.com/ChuChuIgbokwe/ME495-Final-Project-Baxter-Stocking-Stuffer).

###Major steps involved:

1. Scanning and identification of next stocking in line:
..*Point the camera in Baxter's left hand at the board on which the stockings hang and search the area
..*Using a tag tracking ROS package, identify each stocking and find the first one classified as empty, storing the location of stocking and identifying the present associated with it

2. Scanning for present on the table
..*Using OpenCV with ROS, scan the table using the hand camera and locate the correct present color associated with the target present identified in Step 1

3. Grasp the present and go back to the location stored previously- release the present into it

4. Update the filled stockings list

5. Repeat steps 1-5 for the number of stockings hung
