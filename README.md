This is the repo for the RA-L submission, HEA-Planner: Human-Guided Motion Planner with Environmental Adaptation for Assistive Aerial Teleoperation.

# Training details

The policy training and simulation experiments are conducted on the RTX 3070 desktop, while computations for the physical flights are performed on our quadcopter’s onboard computer (NVIDIA Jetson Orin NX). 

The policy is learned with the soft actor-critic algorithm. Both its action and critic networks are implemented with 3 fusion layers having 128, 64 and 32 units, respectively. 

![加载动画](https://github.com/SAA-Robot-Lab/HEA-Planner/blob/main/policy%20training.gif "加载中...")

# Acknowledgements
This repo was developed based on Fast-Planner and ZJU-FAST-Lab, many thanks to them.
