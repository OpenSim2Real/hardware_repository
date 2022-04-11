.. _monopod_design:

Monopod Design
==============

Introduction
------------

This page describes the overarching design of the Monopod hardware platform. 

Design Requirements
-------------------

The following requirements drive the design of the Monopod hardware platform:

- The system must pose a non-trivial control problem, to be of interest to control system researchers. However, the 
  hardware must allow the control problem to be reductible to a simpler form for testing and software validation 
  purposes.

- All components of the system, both software and hardware, must be released under permissive licenses such that this 
  hardware platform can also be released under a permissive license for others to build on top of.

- This system must be inexpensive and within the budgetary constraints of a small lab or to a hobbyist.

- The system must also be easily assembled and reproduced with mostly off-shelf, 3D printed, waterjet or laser-cut 
  parts. This ensures that all parts of this hardware platform can be either manufactured in situ, or contracted 
  out to an external service without much expense.

- The system must be widely used in robotics and controls research, so that there will be many research papers 
  describing the dynamics of the system.


Other Designs Considered: Inverted Pendulum
-------------------------------------------

We considered basing our system out of an inverted pendulum configuration. An inverted pendulum essentially tries to
maintain a mass at a high position without it falling, by actuating several joints. An inverted pendulum has some 
precedent in research: 

- 

An example of a simple inverted pendulum configuration is shown below:

TODO

A 2 jointed inverted pendulum is shown below:

TODO

However, an inverted pendulum configuration is not very extensible. It is quite difficult to attach an additional 
degree of freedom to a two-wheeled inverted pendulum, as a second "pendulum" attached to the first pendulum will 
interfere physically with the first pendulum. There is also significant doubt as to how fast the base of the first 
pendulum must move to swing the second pendulum to an upright position, potentially making this problem unsolvable.

Other Designs Considered: 3D Hopper
-----------------------------------

A 3D Hopper is best characterized by the MIT Hopper, which has 2 actuators to tilt a pogo-stick, and a single actuator 
to compress the pogo-stick. 


Other Designs Considered: 2D Hopper
-----------------------------------

A 2D Hopper is a robotic leg which can hop in 



The Open Dynamic Robot Initiative
---------------------------------



Design Finalization
-------------------

