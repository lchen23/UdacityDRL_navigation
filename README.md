# Navigation in a banana field

## Environment
Unity Machine Learning Agents ([ML-Agents](https://github.com/Unity-Technologies/ml-agents)) is an open-source Unity plugin that enables games and simulations to serve as environments for training intelligent agents. 

This repo presents code and step by step guide on how to train an intelligent agent to solve the [Banana-collector environment](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#banana-collector).

In this Banana-collector environment, a reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana. Thus, the goal of the agent is to collect as many yellow bananas as possible while avoiding blue bananas.

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around the agent's forward direction. Given this information, the agent has to learn how to best select actions. Four discrete actions are available, corresponding to:

    0 - move forward.
    1 - move backward.
    2 - turn left.
    3 - turn right.


## Goal
The goal is to train agents to get an average score of at least +30 (over 100 consecutive episodes, and over all agents). Specifically,
* After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 20 (potentially different) scores. We then take the average of these 20 scores.  

* This yields an average score for each episode (where the average is over all 20 agents).

As an example, consider the plot below, where we have plotted the average score (over all 20 agents) obtained with each episode.  

![mean score plot](score.png)  
The environment is considered solved, when the average (over 100 episodes) of those average scores is at least +30.

## Result
A movie clip demonstrating successfully trained agents (achieving an average score of +35) is shown below. The robotic arms can follow the moving targets (rotating green ball) most of the time.  

![trained agents](reacher.gif)  

## Dependencies
* Numpy
* Matplotlib
* PyTorch (0.4.0 or above)
* ML-Agents toolkit (`pip install unityagents`) 

## Usage
* The Windows (64-bit) version of the environment is provided in this repo in the folder "Reacher_Windows_x86_64".
* Mac OSX version can be downloaded [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip)
* Linux version can be downloaded [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip)

Follow the step by step instructions in **Report.ipynb** to start running the environment and training the agents.

