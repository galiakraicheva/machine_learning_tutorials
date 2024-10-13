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

The value function for a given policy $\( \pi \)$ is defined as:

![Value Function Formula](https://github.com/galiakraicheva/machine_learning_tutorials/blob/main/Value%20Function%20RL%20(credit%20IUAS).png)

Even without carefully looking at the formula, it is obvious that is sums up something. In this case, the expected future rewards for the states onwards. However, rewards in distant future can be less valued or less certain than the present rewards so we introduce the **discount rate**: $\gamma$. The discount rate is a number between 0 and 1 and tells the agent how much it should value future rewards. 
-A higher discount rate tells the agent to be more patient now and to value future rewards more. 
-A lower discount rate tells the agent to favour immediate rewards. 

At each step, the discount rates slighly decrease given the Marginal benefit economic theories. The discount rate is importent because it lets agents make smarter strategies. For example, a chess playing agent can sacrifice a piece to win a better position or to win the game. 

Explaining the formula further: 
- T: the terminal state, the one that ends the episode
- k: the number of steps from the current moment. The second formula is the generalisation for an infinate game scenario with k from 0 to $\infty$.
- $\gamma^k$: as we speak about more distant state, the expected reward become less because it is raised to a bigger power. It is like that because of the more uncertain future state.

## Types of Reinforcement Learning
There are two fundamental types of reinforcement learning: model-frre and model-based and they both deal with how the agent learns to maximase the rewards in the environment but they differ in how they handle the environment dynm=amics, meaning how the world works for them. 

### Model-Based Reinforcement Learning
In model-based reinforcement learning, the agent tries to plan ahead based on the knowledge it has of the environment. It tries to build a model of the environment and tries to predicts what happens as a result of its actions. It learns how the environment works, its dynamics and rules. It uses this knowledge to plan its actions and simulate future steps before it makes a decision. 

Examples of model-based reinforcement learning: 
- playing chess: the agent tries to understand the rules of the game and at each step, the agent simulates the possible scenarios a couple of moves ahead. It makes the decision based on the result of these simulations. 
- robot movement: if a robot operates in a closed space, it maps the area and then simulates different scenarios from the location it is to the location it should go to avoid obstacles and find the shortest way. It chooses the best result out of these simulations.
- medical assistance agent: a possible scenario for an agent that learns as much as possible for the patient's health and tries to simulate the possible scenarios of how different treatments will affect the patient and chooses the one that maximises patient's health oveer time.

### Model-free Reinforcment Learning
In model-free reinforcemnt learning, the agent learns the best strategies without building a map of the environment or understanding its rules. Instead, it tries different strategies and sees the results from them. It is usually applicable for more complex environments like video-games or self-driving cars. 

Examples of model-free reinforcement learning: 
- video games: the agent doesn't need to make a whole map of the world since there are many unpredictable elements in it, like other players and hidden obstacles. Instead, it plays different strategies and sees which are the best, given the rewards or penalties it gets.
- self-driving cars (on a basic level): they don't need to map the whole world with all the roads that they may be exposed to since the most important things to avoid are not static (like pedestrians). Instead, it should learn in what cases it shoudl speed up or push the break based on the rewards it gets as a feedback. 

##Common Algorithms in Reinforcement Learning

### Algorithms for Model-Free Learning: 
#### Q-Learning

