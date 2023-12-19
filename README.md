# Reinforcement_SARSA
Implementing SARSA algorithm to use reinforcement learning to find best route through a maze


## General Information
Here we implement the SARSA algorithm to find an optimum path through a square maze. The maze is constructed with several pitfalls (places where the agent cannot go), and one entrance and one exit.
- When the agent hits a pitfall she is punished with score $-50$.
- When the agent finds the exit, she is rewarded with score $+10^5$.
- We use an $\epsilon-$ greedy policy

At each step of the algorihtm, the action-value function is updated according to

$$q(s,a) \to q(s,a) -\alpha( r(s')+ \gamma q(s',a') - q(s,a) )$$

Here $(s,a)$ represent the current state $(s)$ and action $(a)$ choices. $s'$ represents the next state given action $a$, and $a'$ is the action the greedy-policy would choose at this instance of the algo, given state $s'$.
- Note, if a pitfall is hit, the action-value function is updated but the agent stays put.
- $\alpha$ is the learning rate and $\gamma$ is the discount factor - this incentivises high-reward actions in the near future.


The algorithm terminates if the agent finds the exit or if the agent takes 1000 steps.
The action-value function updates at each step, eventually converging on a matrix which shows at every state $s$, what the `best' action $a$ is to take in order to reach the exit.
We visualize this matrix by converting these instructions to ``up'',``down'', ``left'' and ``right'': highlighting the algorithm's success.

