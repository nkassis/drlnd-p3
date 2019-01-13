# Udacity Deep Reinforcement Learning Nanodegree Project 2: Contiunous Control

## Synopsis

This is my solution to the third project of the Udacity Deep Reinforcement Learning Nanodegree. In this project we were asked to build agents that could play a game of tennis. 

#Environment

We were prodived an environment built with Unity ML-Agent toolkit. 

Here is the project description of the environment:

```
In this environment, two agents control rackets to bounce a ball over a net. If an agent hits the ball over the net, it receives a reward of +0.1. If an agent lets a ball hit the ground or hits the ball out of bounds, it receives a reward of -0.01. Thus, the goal of each agent is to keep the ball in play.

The observation space consists of 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives its own, local observation. Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping.

The task is episodic, and in order to solve the environment, your agents must get an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents). Specifically,

After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 2 (potentially different) scores. We then take the maximum of these 2 scores.
This yields a single score for each episode.
The environment is considered solved, when the average (over 100 episodes) of those scores is at least +0.5.
```

## Requirements

* python 3
* pytorch (Instructions: https://pytorch.org/)
* unityagent (Instructions: https://github.com/Unity-Technologies/ml-agents)
* Jupyter
* Numpy
* Matplotlib
* Tennis Unity Environment ([Linux](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux.zip)),([OSX](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis.app.zip)),
([Win64](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86.zip)),([Win32](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86_64.zip))

## Environment 



## How to run

1. Download the environment and unzip it into the directory of the project. Rename the folder to Tennis and ensure that it contains Tennis.exe 
2. Use jupyter to run the Report.ipynb notebook: `jupyter notebook report.ipynb`
3. To train the agent run the cells in order. They will initialize the environment and train until it reaches the goal condition of +0.5 average over 100 episode
4. A graph of the scores during training will be displayed after training. 

## Code

The code is split between three files and Report.ipynb

### agent.py

Contains the definition of the DDPG actor. It sets up the 4 network the Actor's target and local network and the critics target and local network. 

### model.py

Defines the two model achitecture (further details in Report.ipynb on them)

### replay_buffer.py

Implements a experience store for experience replay. 