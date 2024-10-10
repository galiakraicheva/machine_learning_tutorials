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
  
This chapter is about reinforcement learning. It mimics the way humans and animals learn. For example, a child learns not to touch hot plate after he/she touches the hot plate a several times and learns that this hurts. A dog learns to give a paw after it is given biscuits everytime it gives a paw. 

## Reinforcement Learning Basic Terms
- Agent: the algorithm that performs actions in the environment
- Actions (A): the set of all possible action in the environment. Out of this set,the agent chooses one possible action a on each step.
- Environment (E): the external environment the agents operates in. It reacts to the agent by giving rewards on every movement
- States (S): The set of all possible states in the environment. A single state s is a representation of the agent's current situation. The state s contains all the necessary information for the agent to make a decision.
- Reward (R): An immediate feedback signal from the environment.
- Policy ($\pi$): the strategy that the agent follows to determine which action to take. It can be **deterministic:** everytime the agent is in the current state, it chooses the same strategy or **stochastic:** the agent chooses among the actions with certain probabilities
- Value Function (F): a function that estimates the long-term rewards that can be accumulated with any given state. It allows the agent to plan for the future.

The goal of the agent is to maximise the reward it receives during the learning process. In that sense, the algorithm should choose a strategy that it knows if beneficial. However, it should also decide if it wants to explore new strategies or rely on strategies it knows to be beneficial. These are called: 
- Exploration: Trying out new strategies to discover more about the environment and potentially find more beneficial  strategies than the current ones. 
- Exploitation: using the knowledge the agent already has to maximise the reward

Finding the balance between exploration and exploitation is one of the challenges in reinforcement learning and is often solved by $ε$-greedy strategy, where the agent most often chooses the knowln strategy but occasionally it prefers to explore. 

## The Reinforcement Learning Process: Markov Decision Process (Markov's Chain)
**Markov Decision Process:**
- a way to formalise the sequential decision making
- used when outcomes are partly random and partly under the control of the decision maker
- the most common way to model the reinforcement learning process

#### Why is this method so preferred?
A state is said to have the Markov property if it holds all the relevant information about past actions. Therefore, all the necessary information about making a decision is held in the present state. The process is memoriless. in reinforcement learning, all decisions are also a function of the present state.

Further explanation: it might seem that the actual idea of learning contradicts the memoriless decision making. If an agent learns the best strategy how does it make memoriless decisions? The idea is that the knowledge is encoded in the expected rewards and the transitional probabilities of the state. For example, an agent learning to play chess can know the best strategy for the currrent state but doesn't need to remember how it got there and all the games it played that led to the same situation in which it had to decide. 

**Key terms in Markov Decision Process:**
- States (S): same as in RL
- Actions (A): same as in RL
- Transition Probabilities (P): the probabilities of transitioning from one state to another, given the action
- Reward (R): the reward function that provides feedback at any transition to a new state.

**Value Function:** 
-it estimates how much total reward can the agent expect to receive, starting from a given state, over the long run 
-this means it is contained and the information it holds is contained in the present state (no contradiction with Markov property
-**value of a state**: how beneficial it is for the agent to be in that state, considering immediate rewards and future rewards it can gain, if it takes the right actions from here on. For example: in a chess game, being in a strong position in the center may not lead to winning immediately but may be more beneficial for future winning because it often leads to better moves and rewards in future. 

The value function for a given policy \( \pi \) is defined as:

![Value Function Formula](path_to_image/value_function.png)
