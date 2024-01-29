---
title: "Optimal Path Routing using Reinforcement Learning"
excerpt: "The project is aimed  to develop an environment with Open-AI Gym and create an AI (Artificial Intelligence) system to help control the flow of network traffic dynamically. "
collection: portfolio
---

Introduction
-------
Routers use routing algorithms like Dijkstra, Bellman-Ford, and Ford-Fulkerson to find the best route from a source node to a destination node through multiple switches and routers. These algorithms have drawbacks, such as being complex, taking a long time to process, and not being dynamic enough to consider parameters like traffic congestion and queue size. In internet congestion control, the goal is to modulate traffic sources' data-transmission rates to efficiently use network capacity. Reinforcement learning (RL) can be used to train deep network policies that capture intricate patterns in data traffic and network conditions, improving performance.

Environment:
-------
An environment is required for developing and testing learning agents. We have created an Environment using openAI gym.

States :States is comprised of a state vector which has 3 elements describing the following:

* Latency Gradient: the derivative of latency with respect to time
* Latency Ratio :the ratio of the current MI’s mean latency to minimum observed mean latency
*Sending Ratio:the ratio of packets sent to packets acknowledged by the receiver

State at Time T , \{s_t} = \(v_{t-k+d},...,v_{t-d}\)

Here, St is the state vector with components being a list of a list.Each element of the state vector is a list having the 3 metrics described above. k is the window time from which each list has to be used in St

Actions: Actions are changes to sending rate(at) 

Rewards: The Reward Function is 10\*throughput - 1000\*latency - 2000*loss

The agent is the transmitter of traffic in our concept, and its activities lead to changes in sending rates. We use the concept of monitor intervals (MIs) to define this.Time is split into segments that are successive. The sender can alter its transmission rate xt at the start of each MI t, which remains constant during the MI.

Algorithm:
------
* Proximal Policy Optimization (PPO):
  * Reinforcement learning algorithm that optimizes a neural network policy to maximize expected rewards
  * Uses surrogate objective function to prevent large policy updates that could cause instability or performance degradation
  * Example application: training an agent to play a game like Atari's Breakout
* Hindsight Experience Replay (HER):
  * Technique used to improve efficiency of learning from failed experiences in reinforcement learning
  * Relabels unsuccessful experiences as successful by changing agent's goal to achieved state instead of original desired state
  * Example application: training an agent to solve a robotic manipulation task like stacking blocks

