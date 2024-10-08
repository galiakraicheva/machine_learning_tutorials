## Basic Machine Learning Techniques

There are three techniques in Machine learning to train a model: 
1. Supervised Learning:
   - you need a large labeled dataset
   - typical tasks: regression and classification
   - uses: spam detection, credit risk estimation, etc.  
2. Unsupervised Learning:
   - unlabeled data, algorithm must find underlying patterns
   - typical tasks: cluster analysis, dimensionality reduction, anomaly detection
   - uses: to oraganise massive amounts of information like profiling website users, identify relevant peer groups, etc. 
3. Reinforcement Learning:
   - algorithms improve themselves by interacting with the environmen, no predefined data required. The agent learns on an unknown set of data by the rewards it gets from the environment
  
This chapter is about reinforcement learning. 

## Reinforcement Learning Basic Terms
- Agent: the algorithm that performs actions in the environment
- Actions (A): the set of all possible action in the environment. Out of this set,the agent chooses one possible action a on each step.
- Environment (E): the external environment the agents operates in. It reacts to the agent by giving rewards on every movement
- States (S): The set of all possible states in the environment. A single state s is a representation of the agent's current situation. The state s contains all the necessary information for the agent to make a decision.
- Reward (R): An immediate feedback signal from the environment.
- Policy ($\pi$): the strategy that the agent follows to determine which action to take. It can be **deterministic:** everytime the agent is in the current state, it chooses the same strategy or **stochastic:** the agent chooses among the actions with certain probabilities
- Value Function (F): a function that estimates the long-term rewards that can be accumulated with any given state. It allows the agent to plan for the future.
