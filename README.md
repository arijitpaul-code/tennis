# tennis

Project Details

The project is to train two agents control rackets to bounce a ball over a net. If an agent hits the ball over the net, it receives a reward of +0.1. If an agent lets a ball hit the ground or hits the ball out of bounds, it receives a reward of -0.01. Thus, the goal of each agent is to keep the ball in play, in Unity Reacher environment. The observation space consists of 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives its own, local observation. Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping. Every entry in the action vector should be a number between -1 and 1.

The task is episodic, and in order to solve the environment, the agents must get an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents). Specifically,

- After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 2 (potentially different) scores. We then take the maximum of these 2 scores.
- This yields a single score for each episode.

The environment is considered solved, when the average (over 100 episodes) of those scores is at least +0.5.

Getting Started

The dependencies for the progream are in requirements.txt file, following the instructions in https://github.com/udacity/Value-based-methods#dependencies, with the tennis unity environment sourced directly from (for Linux) https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux.zip and extracted and placed in the p3_collab-compet/ folder. After that cuda support was installed using conda install cudatoolkit.

Instructions

The entire code is in Tennis.ipynb. To execute, run upto cell "In [4]" (under 2. Examine the State and Action Spaces) sequentially, to load and examine the environment. You can explore the environment to see random actions being taken by executing the next cell. Then execute cells "In [19]" for setting model parameters, class definition (Agent, Noise, Replay Buffer, Multi_Agent, Actor, Critic NN model classes), build the ddpg agent, train the model and finally plot the results. At the end, if the model is solved the best weights are saved in checkpoint_actor_0.pth,  checkpoint_critic_0.pth, checkpoint_actor_1.pth,  checkpoint_critic_1.pth files, which can be loaded later for execution without additional training.

Lastly, run the env.close() cell, when finished.
