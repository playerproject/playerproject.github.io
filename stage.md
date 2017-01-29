---
layout: page
title: Stage
permalink: /stage/
---
2.5D multiple robot simulator.

## Get Stage
[[Releases]](https://github.com/rtv/stage/releases)  [[Source]](https://github.com/rtv/stage) [[Issue Tracker]](https://github.com/rtv/stage/issues) [[Wiki]](https://github.com/rtv/stage/wiki)

## About Stage
<img style="float: right;" src="/assets/img/pioneer.png">
Stage simulates a population of mobile robots, sensors and objects in a two-dimensional bitmapped environment.
Stage is designed to support research into multi-agent autonomous systems, so it provides fairly simple, computationally cheap models of lots of devices rather than attempting to emulate any device with great fidelity.
We have found this to be a useful approach.

## Stage Features

### Stage Simulator
The standalone program *stage* is a fast and scalable robot simulator.
Your robot controllers are compiled and loaded at run-time, and can be attached to any model.
Controllers have complete access to the Stage API.

### Player/Stage (Player with libstageplugin)
Stage is often used a a Player plugin module, providing populations of virtual devices for Player.
Users write robot controllers and sensor algorithms as 'clients' to the Player 'server'.
Typically, clients cannot tell the difference between the real robot devices and their simulated Stage equivalents (unless they try very hard).
We have found that Player clients developed using Stage will work with little or no modification with the real robots and vice versa.
Thus Stage allows rapid prototyping of controllers destined for real robots.
Stage also allows experiments with realistic robot devices you don't happen to have.
Various sensors and actuator models are provided, including range-finders (sonar, SICK and Hokuyo laser scanners, IR), vision (color blob detection), 3D depth-map camera, odometry (with drift error model), and a differential steer robot base.

### libstage
Stage can also be used as a C++ library to provide a robot simulation inside your own programs.
This is useful if Player is not suitable for your needs, or if you want custom simulation models based on a well-known simulation engine.


<img style="float: right;" src="/assets/img/hospital.png">
<img style="float: right;" src="/assets/img/fasr.png">
