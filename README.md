# Udacity Self-Driving Car Capstone Project <img src="imgs/1.png" alt="drawing" width="50"/> <img src="imgs/2.png" alt="drawing" width="50"/> <img src="imgs/3.png" alt="drawing" width="50"/>   

## About
This is the capstone project for the **Udacity Self-Driving Cars Nanodegree**.
The objective of this project is to enable Carla(Udacity's self driving car) to follow a set of waypoints while following the rules of traffic.
Modules of Perception, Planning and Control have been implemented with different techniques learnt along the course. We will be using ROS as the framework to communicate between each module at a frequency of 50 MHz.

## System Architecture Diagram
The **main idea** is that the **car will follow** smoothly(controlled with a PID and a low pass filter) **every waypoint** of the map **using the drive-by-wire node**(DBW), which will determine the vehicle acceleration, brake and steering. When a **red traffic light is detected** in front of the vehicle, the perception module will update the waypoints so that the control module can apply the suitable deceleration to make **the vehicle come to a stop**.

![ros-graph](https://user-images.githubusercontent.com/30600046/43013602-5a750a82-8c41-11e8-9e64-6c00290b5405.png)

## Contributors

Name | Contact | GitHub
-----|---------|-------
Oscar Rovira (lead) | oscar.roviramontenegro@gmail.com | @hirovi
Atul Pandey | atul799@gmail.com | @atul799
JiaWei | JiaWei.You1016@gmail.com | @yjw16
Cesar Bonadio | cesar.bonadio@gmail.com | @bonadio
Christy Cui | christycui14@gmail.com | @christycui


## Build & Run Instructions

1. Clone repository.
```
git clone https://github.com/atul799/SDC_Capstone_Project.git
```
2. Install python dependencies.
```
cd SDC_Capstone_Project
pip install -r requirements.txt
```
3. Make and run styx. (No need for roscore)
```
cd ros
catkin_make
source devel/setup.sh
roslaunch launch/styx.launch
```
