# Turtlebot3 Maze Solver

## Overview

This project simulates a Turtlebot3 robot navigating a maze using ROS2. The robot utilizes an RGB camera for Aruco marker detection and a logical camera for identifying parts in the environment.

![demo](https://github.com/FazilMammadli/Maze_Turtlebot3/blob/master/waffle_demo.gif)

## Getting Started

To start the simulation, run the following command:

This will initialize the Gazebo environment with Turtlebot3 and its sensors.

## Node Descriptions

### MoveRobot Node
Moves the robot forward and stops when it is ≤ 0.4 meters from an Aruco marker, subscribing to `odom` and controlling movement via `cmd_vel`.

### ArucoMarkerHandler Node
Transforms detected Aruco markers into the `odom` frame, calculates the distance, and checks marker parameters for instructions.

### LogicalCameraHandler Node
Subscribes to `mage/advanced_logical_camera/image` and detects batteries, printing their positions in the `odom` frame.

## Instructions
- Start the simulation using the launch command.
- Run the MoveRobot node to move toward Aruco markers.
- ArucoMarkerHandler processes markers and controls movement.
- LogicalCameraHandler prints battery positions upon detecting the "end" marker.



