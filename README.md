# Mudang Autonomous Driving Project

Welcome to the Mudang Autonomous Driving Project! This project aims to develop an autonomous shuttle service to enhance the current Mudang shuttle operations at Gachon University, providing a more efficient, cost-effective, and continuous transportation solution for students.

## Table of Contents
- [Project Overview](#project-overview)
- [Background](#background)
- [Installation Environment](#installation-environment)
  - [Hardware Requirements](#hardware-requirements)
  - [Software Requirements](#software-requirements)
  - [Development Tools](#development-tools)
- [Implementation](#implementation)
  - [System Architecture](#system-architecture)
  - [Workflow](#workflow)
- [Future Works](#future-works)
- [GitHub Repository](#github-repository)

## Project Overview

**Mudang Autonomous Driving** is an innovative project aimed at developing an autonomous shuttle service to address the operational limitations of the current Mudang shuttle at Gachon University. The project was initiated to provide a more efficient, cost-effective, and continuous transportation solution for students, particularly during times when the conventional shuttle service is unavailable, such as early mornings, late evenings, and vacation periods.


### Team Members

- **Choi Sanghyun** (201935141)
- **Yoon Sehyeon** (202135553)
  - **Jeon Jihyun** (202035385)

## Background

Mudang, the current shuttle service, operates with fixed dispatch times and does not run during early mornings, late evenings, or vacation periods due to the high costs associated with hiring drivers. This often leads to inconvenience for students, particularly those whose classes run beyond regular hours or during peak times when the shuttle is in high demand.

The goal of the Mudang Autonomous Driving project is to automate the shuttle service, eliminating the need for human drivers and providing a more flexible and reliable transportation solution.
![image](https://github.com/Mudang-Autonomous-Driving/AutonomousDriving/assets/99864704/b206f9b1-d769-40c0-ad60-cecad9ffeab7)


## Installation Environment

### Hardware Requirements

- **Vehicle**: An electric shuttle or similar vehicle capable of integration with autonomous driving technologies.
- **Sensors**:
  - **GPS**: For global positioning.
  - **IMU (Inertial Measurement Unit)**: For measuring acceleration and angular velocity.
  - **LiDAR**: For object detection and environment mapping.
  - **Wheel Encoders**: For tracking the vehicle's movement.

### Software Requirements

- **Operating System**: Ubuntu 20.04 or later.
- **Programming Languages**: Python, C++.
- **Libraries and Frameworks**:
  - **ROS (Robot Operating System)**: Middleware for robotics applications.
  - **LeGO-LOAM**: Lightweight and Ground-Optimized Lidar Odometry and Mapping.
  - **Extended Kalman Filter**: For sensor fusion and state estimation.In robot_localization package
  - **Controller Area Network (CAN)**: For vehicle communication and control.

### Development Tools

- **Git**: Version control system.
- **Rviz**: ROS visualization tool.

## Implementation

### System Architecture
![image](https://github.com/Mudang-Autonomous-Driving/AutonomousDriving/assets/99864704/3ba8aaae-20f3-446b-a836-d1bf28f56494)


The Mudang Autonomous Driving system is composed of several key components:

1. **Localization**:
   - **GPS and IMU**: Provide initial positioning and orientation data.
   - **LiDAR**: Used for precise localization, especially in GPS-denied zones.
   - **Sensor Fusion**: Combines data from GPS, IMU, and LiDAR using the Extended Kalman Filter to improve accuracy.

2. **Mapping and Navigation**:
   - **SLAM (Simultaneous Localization and Mapping)**: Creates a detailed 3D map of the environment using the LeGO-LOAM algorithm.
   - **Path Planning**: Determines the optimal route for the vehicle to follow.
   - **Obstacle Detection and Avoidance**: Uses LiDAR data to detect and navigate around obstacles.

3. **Control Systems**:
   - **Lateral Control**: Uses the Stanley lateral controller for path following.
   - **Longitudinal Control**: Uses PID controllers to manage speed and braking.
   - **CAN Protocol**: For sending control commands to the vehicle and receiving feedback.

### Workflow

1. **Sensor Data Acquisition**: Collect data from GPS, IMU, and LiDAR sensors.
2. **Localization**: Use sensor fusion to determine the vehicle's precise location.
3. **Mapping**: Create and update the environment map using SLAM.
4. **Path Planning**: Generate the optimal path based on the map and destination.
5. **Vehicle Control**: Send control commands via the CAN network to steer and adjust speed.

## Demo Video
[![Video Label](http://img.youtube.com/vi/Qv_Vt0vdYl0?si=ZxbeK15yVu8BA-Ba/0.jpg)](https://youtu.be/Qv_Vt0vdYl0?si=ZxbeK15yVu8BA-Ba)
NDT localization



## Future Works

Although significant progress has been made, several tasks remain to be completed:

- **Algorithm Refinement**: Improve the accuracy and reliability of the localization and mapping algorithms.
- **Real-world Testing**: Conduct extensive testing on a real vehicle within the campus to ensure safety and performance.
- **User Interface**: Develop a user-friendly interface for scheduling and monitoring the autonomous shuttle service.

