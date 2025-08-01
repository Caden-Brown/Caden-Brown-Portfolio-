# uav-autonomy-project
This repository contains some of the code for an autonomous UAV system developed using ROS 2 as the core framework. The system utilizes MAVLink for flight controller communication via MAVROS, enabling native integration with ROS 2 nodes.

Key components include real time object detection and classification using a custom trained YOLOv8 model, along with sensor data processing from onboard IMU, GPS, gyros, and infrared/visual sources. These inputs are fed into a Bayesian fusion node, which combines the sensor outputs into a unified situational understanding. Fusion parameters are configurable and can be adapted based on mission requirements.

The fused data is then passed to an autonomous decision making node that evaluates the current scenario and selects appropriate actions, such as adjusting flight paths, prioritizing threats, or tracking targets. This system is designed for modularity, allowing future expansion into swarm coordination, or reinforcement learning.

This repo houses the nodes that are used in the companion onboard computer, which communicates with the flight controller via MAVROS. Each node serves a distinct function within the autonomy pipeline, including perception, sensor fusion, decision-making, and actuator command routing. 

Still under active development, as such more files will be added to the repo with updates being made to this readme explaining thier purpose and steps for integration and comunication.

