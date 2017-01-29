---
layout: page
title: About the Player Project
permalink: /about/
---
Free Software tools for robot and sensor applications

## Purpose
The Player Project creates Free Software that enables research in robot and sensor systems.
In the early 2000s, the Player robot server was probably the most widely used robot control interface in the world.
Its simulation backends, Stage and Gazebo, are also very widely used.

## Software
The Player Project primarialy supports and maintains the following software projects:

### [Player](/player) robot device interface
Player provides a network interface to a variety of robot and sensor hardware.
Player's client/server model allows robot control programs to be written in any programming language and to run on any computer with a network connection to the robot.
Player supports multiple concurrent client connections to devices, creating new possibilities for distributed and collaborative sensing and control.
Player provides a network interface to a variety of robot and sensor hardware.
Player's client/server model allows robot control programs to be written in any programming language and to run on any computer with a network connection to the robot.
Player supports multiple concurrent client connections to devices, creating new possibilities for distributed and collaborative sensing and control.

Player supports a wide variety of mobile robots and accessories.

### [Stage](/stage) multi-robot simulator
Stage simulates a population of mobile robots moving in and sensing a two-dimensional bitmapped environment.
Various sensor models are provided, including sonar, scanning laser rangefinder, pan-tilt-zoom camera with color blob detection and odometry.

Stage devices can be presented as standard Player interfaces, so few or no changes are required to move between simulation and hardware.
Many controllers designed in Stage have been demonstrated to work on real robots.

## Previous Software
Some software from the Player Project has moved on to bigger and better things, and other software is no longer maintained.
The following projects were once maintained by under the Player Project:

### Gazebo 3D multiple robot simulator
Gazebo is a multi-robot simulator for outdoor environments.
Like Stage, it is capable of simulating a population of robots, sensors and objects, but does so in a three-dimensional world.
It generates both realistic sensor feedback and physically plausible interactions between objects (it includes an accurate simulation of rigid-body physics).

Gazebo is currently maintained by the [Open Source Robotics Foundation](http://osrfoundation.org).
Its project page is located at [gazebosim.org](http://gazebosim.org)

### Mezzanine 2D Overhead Tracking
Mezzanine is an overhead 2D visual tracking package intended primarily for use as a mobile robot metrology system.
It uses a camera to track objects marked with color-coded fiducials, and infers the pose (position and orientation) of these objects in world coordinates.
Mezzanine will work with most color cameras (even the really cheap ones), and can correct for the barrel distortion produced by wide-angle-lenses.

Mezzanine is language and architecture neutral: object poses are written into a shared memory-mapped file which other programs can read and make use of as they see fit.
Mezzanine itself is written in pure C and was developed under Linux on x86 hardware.

Mezzanine is no longer maintained.
