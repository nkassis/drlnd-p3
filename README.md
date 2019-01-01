# Udacity Deep Reinforcement Learning Nanodegree Project 2: Contiunous Control

## Synopsis

This is my solution to the second project of the Udacity Deep Reinforcement Learning Nanodegree. In this project we were asked to build an agent that could control a double-jointed arm towards specific locations.

#Environment

We were prodived an environment built with Unity ML-Agent toolkit. 

Here is the project description of the environment:

```
In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.
```

## Requirements

* python 3
* pytorch (Instructions: https://pytorch.org/)
* unityagent (Instructions: https://github.com/Unity-Technologies/ml-agents)
* Jupyter
* Numpy
* Matplotlib
* Reacher Unity Environment ([Linux](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux.zip)),([OSX](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher.app.zip)),
([Win64](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86_64.zip)),([Win32](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86.zip))

## Environment 



## How to run

1. Download the environment and unzip it into the directory of the project. Rename the folder to reacher and ensure that it contains Reacher.exe 
2. Use jupyter to run the Report.ipynb notebook: `jupyter notebook report.ipynb`
3. To train the agent run the cells in order. They will initialize the environment and train until it reaches the goal condition of +30
4. A graph of the scores during training will be displayed after training. 

## Code

The code is split between three files and Report.ipynb

### agent.py

Contains the definition of the DDPG actor. It sets up the 4 network the Actor's target and local network and the critics target and local network. 

### model.py

Defines the two model achitecture (further details in Report.ipynb on them)

### replay_buffer.py

Implements a experience store for experience replay. 