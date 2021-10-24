# **PID Control Project** 

Control a vehicle around a circular track using PID controller

## Writeup

#### The effect of P, I, and D components

##### P component

As P or proportional controller is proportionally controlling the error, increasing its coefficient will decrease the steady state error, and rise time, but it would also increase the overshoot.

##### I component

By controlling the accumulative error, this controller is suitable for systems with biases and noises. It decreases the steady state error, and settling time, but increases overshoot.

##### D component

This controller takes the derivatives of error as input, so it is effective to reduce overshoot. It also decreases the settling time, but increases the rise time.

#### Parameter tuning

I set the hyperparameters of controllers manually based on the effect of each one on the output. The final values are set as follows:

_________________________________________________________________
Parameter       | Steering controller      | throttle controller   
=================================================================
Kp			    | 0.14			           | 0.5       
_________________________________________________________________
Ki              | 0.0      				   | 0.0       
_________________________________________________________________
Kd              | 1.1       			   | 0.5         
_________________________________________________________________ 

#### Goal

The vehicle in this project successfully drives a lap around the track with the velocity of around 50 mph. This goal is achieved by defining two separate PID controllers for steering and throttle values. The throttle controller does a good job in reaching and keeping the desired speed. The steering controller on the hand, is not as good as it should be. There are disturbances in the output which lead to an undesirable steering angles specially when the car needs to change its direction. It seems a more powerful controller with nonlinear characteristics or an adaptive PID controller would be more beneficial for controlling the steering angle.
