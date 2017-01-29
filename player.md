---
layout: page
title: Player
permalink: /player/
---
Cross-platform robot device interface and server.

## About Player
Player is a network server for robot control.
Running on your robot, Player provides a clean and simple interface to the robot's sensors and actuators over the IP network.
Your client program talks to Player over a TCP socket, reading data from sensors, writing commmands to actuators, and configuring devices on the fly.

Player supports a variety of robot hardware.
The original Player platform is the ActivMedia Pioneer 2 family, but several other robots and many common sensors are supported.
Player's modular architecture makes it easy to add support for new hardware, and an active user/developer community contributes new drivers.

Player runs on Linux (PC and embedded), Solaris, BSD, and Windows.

## Player Features
Player is designed to be language and platform independent.
Your client program can run on any machine that has a network connection to your robot, and it can be written in any language that supports TCP sockets.
We currently have client-side utilities available in C, C++, Python and Ruby.
Further, Player makes no assumptions about how you might want to structure your robot control programs.
In this way, it is much more "minimal" than other robot interfaces.
If you want your client to be a highly concurrent multi-threaded program, write it like that.
If you like a simple read-think-act loop, do that.
If you like to control your robot interactively, try our Python client (or write your own client utilities in your favorite interactive language).

Player allows multiple devices to present the same interface.
For example the Pioneer 2 and RWI drivers both use Player's 'position2d' interface to allow control of the robot's movement.
Thus the same control code could drive both kinds of robot.
This feature is very useful when combined with the Stage simulator; control programs written for Stage's simulated robots will often work unchanged on real hardware.

Player is also designed to support virtually any number of clients.
Have you ever wanted your robots to "see" through each others' eyes?
Now they can.
Any client can connect to and read sensor data from (and even write motor commands to) any instance of Player on any robot.
Aside from distributed sensing for control, you can also use Player for monitoring of experiments.
For example, while your C++ client controls a robot, you can run a graphical visualization tool elsewhere that shows you current sensor data and a logger program to save data for later analysis.
On-the-fly device requests allow your clients to gain access to different sensors and actuators as needed for the task at hand.

The behavior of the server itself can also be configured on the fly.
See the [user manual](/manuals) or details on changing sensor data rate and other features.

Last but not least, Player is free software, released under the GNU Public License.
If you don't like some part of how it works, change it.
And please [send us your patch!](https://github.com/playerproject/player/pulls)
