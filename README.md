# Autonomous Driving Model in Carla Simulation
In this project, an autonomous vehicle was developed in the CARLA simulation environment. The primary objective of the project is to enable autonomous vehicles to navigate traffic safely and efficiently by recognizing traffic signs and lights, using distance measurement algorithms, and applying reinforcement learning techniques.
## Autonomous Driving System Architecture
![Description of the image](BreadcrumbsAutonomous-Driving-Model/picture.png)

The core architecture of our autonomous driving system is shown in The system consists of key components such as environment perception, state estimation, decision making, and action control.

For environment perception, we employ the YOLO (You Only Look Once) object detection algorithm and a traffic sign recognition module. The sensed data (steering, speed, braking, position) is compressed using a Variational Autoencoder (VAE) to create a meaningful state representation. At time t, the system perceives the current state (vehicle speed, position, road conditions, and surrounding objects) and uses this information to determine the next action.

Proximal Policy Optimization (PPO) is used to select the optimal action based on this state representation. At time t+1, the selected action (e.g., acceleration, braking, turning) is executed, and the system transitions to a new state. Before the actions are sent to the vehicle control system, they pass through a smoothing filter.

The system is trained and tested in the CARLA simulation environment using data from sensors and cameras. A test video demonstrating the system's performance is available [here](https://www.youtube.com/watch?v=Vv5ntKC1Y2k)

