# Highway Path Planning Project - Reflection

## Udacity Self Driving Car Nanodegree

## Goals

#### In main goal of this project is to safely navigate around a virtual highway and handling the

#### below mentioned points.

- Stay within your lane unless
- Follow the Traffic Signal rules
- Don’t overstep the stop line in front of all signals
- **Acceleration** should be less
- Jerk should be less

## Architecture:

#### There are 4 major operations that controls the motion of car in an environment

### 1. Sensors:

#### Gets input from Camera images to detect and classify signals.

### 2. Perception

#### Detects signals using Single Shot Detector (SSD) pretrained model and classifies

#### between various types of signals.

### 3. Planning

```
Plans and generate Way points in which the vehicle is supposed to travel. The planning is
based on the input from the traffic light detection and classification and also from the
obstacle detection.
```
### 4. Control

```
Controlling the Steering, Brake and throttle is done in Drive by wire model. A PID controller
is implanted in order to reduce oscillations in car’s trajectory and to reduce steady state
error.
```
## Communication :

Communication between all the above-mentioned components is done using ROS Publish and
Subscribe mechanisms as given in the below diagram.


## Future Woks:

- Behavioural Cloning based path planning and traffic light detection same as project 4 can be
    implemented. This reduces the latency in predicting and classifying the traffic signals
- Reinforcement learning based path planning algorithm can be incorporated.


