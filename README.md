This is the repo for the RA-L submission, HEA-Planner: Human-Guided Motion Planner with Environmental Adaptation for Assistive Aerial Teleoperation.

As I am currently writing my graduation thesis, I do not have enough time to organize the data. If you have any questions, please do not hesitate to leave a message.

# Training details

The policy training and simulation experiments are conducted on the RTX 3070 desktop, while computations for the physical flights are performed on our quadcopter’s onboard computer (NVIDIA Jetson Orin NX). 

The policy is learned with the soft actor-critic algorithm. Both its action and critic networks are implemented with 3 fusion layers having 128, 64 and 32 units, respectively. 

![Training environment](https://github.com/SAA-Robot-Lab/HEA-Planner/blob/main/policy%20training.gif "Training environment")

# Parameters & Convergence

Some images about parameter selection. 

<img src="https://github.com/SAA-Robot-Lab/HEA-Planner/blob/main/pictures/para.png" width="700px">


A comparison of the convergence speed of policy networks. Our work can achieve convergence with less human feedback.

<img src="https://github.com/SAA-Robot-Lab/HEA-Planner/blob/main/pictures/convergence.png" width="300px">

The simulation environment is mainly composed of random obstacles in a 30m × 30m × 5m volume. A episode is defined as the quadrotor flying around the environment once, which takes approximately 2 to 3 minutes. In particular, we record the reward curves of each method to evaluate the efficiency of the policy in learning human preferences.  As shown in 'convergence.png', other methods struggle to quickly guide the policy to learn human preferences, which limits the practicality of human-in-the-loop reinforcement learning. In contrast, our proposed method enables the policy to converge within approximately 20 episodes, with each episode involving around 10 simulated inputs. 

# Acknowledgements
This repo was developed based on Fast-Planner and ZJU-FAST-Lab, many thanks to them.
