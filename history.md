---
layout: page
title: Player Project History
permalink: /history/
---
## Origin
The origin of the Player Project, as told by Richard Vaughan.

Brian Gerkey and Richard Vaughan arrive independently at USC in fall 1998. At this time the Interaction Lab works almost entirely on multi-robot systems. Richard writes Arena, a multiple robot simulator for his own use. Initially, robot controllers are compiled directly into the Arena code. The lab's Pioneer robots all run Ayllu by Barry Werger. Ayllu is a 'port-arbitrated' (ie. subsumption like, with some extensions) programming framework based on C. It works well, but forces a particular control model. Richard and Brian both give talks to the lab about using UNIX-like abstractions and machinery to improve the woeful state of robot software infrastructure. Supervisor Maja Mataric frowns so we do Other Stuff, but resolve to build the tools we need as we go along.

Kasper Stoy joins in 1999 and works with Richard designing robot controllers in Arena. By this time, Richard has written a socket interface to Arena, giving the familiar client-controller/server-robot(s) model. Kasper and Richard produce big chunks of code that they want to try on real robots but don't want to port to Ayllu, so they develop ArenaServer. ArenaServer runs on the robot and presents the same socket interface as Arena. Written in a hurry, it wraps chunks of Ayllu/ActivMedia code to interface with the Pioneer and is rather ugly. It works well, though, and the robot control code ran unchanged in Arena and on the real robots. ArenaServer also includes Richard's original USC Sick LMS driver.

In some coffee-fueled sessions on the Interaction Lab steps, Brian, Richard and Kasper spec out the generic robot interface of their dreams. It should be as unprescriptive as possible, present a socket interface and hide all the hardware junk from you. It should be Free so people could use it and add drivers, and it should work nicely with a simulator. Brian and Kasper write a new server for the Pioneer with their own original PSOS driver and the LMS driver. Brian names it Golem, "One hell of a robot server" and chooses port 6665 as the default. Richard writes a Golem/Arena interface and ArenaServer is retired as obsolete. Golem/Arena has the very basic functionality of Player/Stage, but is still quite tightly tied to the Pioneer.

In 2000 Andrew Howard arrives at USC. About now Brian draws the system diagram that is still in the Player manual. It turns out that 75% of all robot software is called Golem and another 20% is called Arena. For the sake of a good quote ("All the world's a stage;/ and all the men and women merely players", from As You Like It by William Shakespeare) we renamed Golem and Arena to Player and Stage. Brian and Richard write "Most Valuable Player" in 18 hours. Kasper returns to Denmark and stops working on Player. Andrew becomes a core developer of both Player and Stage. Brian, Andrew and Richard design the interface/driver abstraction framework that underlies Player today. By now the majority of Interaction Lab and RESL robots run Player, and the students are using Stage regularly. The project is announced on the lab web site. People outside the lab start submitting bug reports.

Increasingly, evening beer augments daytime coffee as the team and the software develop nicely. People start to use the software quite a lot. Brian is pointed out at a conference as "the Player guy" by someone he'd never met. With great power comes great responsibility.



## Landmarks
* 2001: First contributions from third party developers (UMass guys?)
* 2001: Player/Stage source tree moves to Sourceforge, making it independent of USC
* 2002: Brian invents the passthrough driver
* 2002: First direct funding for Player/Stage
* 2002: Andrew and Nate Koenig start work on Gazebo
* 2002: RADISH established by Andrew and Nick Roy of MIT
* 2003: "On device abstractions" published - first clear statement of the seperation of Player protocol, interfaces, and implementation
* 2003: RETF discussion focusses on Player as a "defacto standard"
