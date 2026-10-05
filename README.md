# Basic-URDF-Robot-
My Robot: Differential Drive Robot in URDF (Visualized in RViz)

A mini project that models a simple differential-drive mobile robot using URDF (Unified Robot Description Format) and visualizes it in RViz.

Overview

This project defines a small wheeled robot with a rectangular body, a LIDAR on top, two driven wheels, and a passive castor wheel. It is a beginner-friendly introduction to:

Writing a URDF file (links, joints, materials)
Understanding parent-child frame relationships (TF tree)
Visualizing and testing a robot model in RViz
Robot Description
Links
Link	Shape	Size	Color

Design Notes
base_footprint is an empty link that sits on the ground. 
base_joint lifts base_link by 0.1 m so that the 0.1 m radius wheels touch the ground.
Wheels are continuous joints rotating about the Y axis, so they can spin freely.
The visual rpy="1.57 0 0" rotates the cylinders so their flat faces point sideways (otherwise they would lie like a standing disc facing the wrong way).
Castor wheel is a fixed sphere at the front that provides a third support point (it does not rotate or steer in this model).
LIDAR is mounted on top of the body at z = 0.225 m (top of the box at 0.2 m plus half the LIDAR height).
Materials (grey, green, white) are defined once at the top and reused by name.

Packages:
robot_state_publisher
joint_state_publisher_gui
rviz2
urdf_tutorial (optional, for a one-command launch)


Expected Result
Green rectangular chassis
White cylindrical LIDAR on top
Two grey side wheels (rotating about the Y axis)
One grey castor wheel at the front, touching the ground

