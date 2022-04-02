Monopod Firmware Setup & Flash
==============================

Introduction
------------

This page explains how to flash the prerequisite firmware onto the TI Launchpad boards.

There are 2 different firmware packages which need to be flashed onto 2 TI Launchpad boards. The first firmware
controls the motors and reads the encoders on the Robotic Leg. The second firmware reads the encoders on the Central
Pivot. Communication to and from both TI Launchpads to a computer is done via CAN protocol.

The following instructions require the use of a Windows 10 operating system. The instructions are structured as 
follows:
* Instructions for Robotic Leg Firmware
* Instructions Central Pivot Firmware

Instructions for Robotic Leg Firmware
----------------------------------------

TI Code Composer Studio(CCS) is an IDE for developing Texas Instruments microcontrollers. Motorware is an SDK
for developing motor control functionality on Texas Instruments microcontrollers.

Follow these instructions to set up both TI CCS and TI Motorware: 
* `ODRI Firmware for CAN: How to Build and Flash the Firmware <https://open-dynamic-robot-initiative.github.io/mw_dual_motor_torque_ctrl/build_instructions.html>`

ahh what to do here....

Follow the instructions above. 

Instructions for Central Pivot Firmware
---------------------------------------

Clone the following repository: `Encoder Measurement Firmware <https://github.com/OpenSim2Real/encoder_measurement>`

