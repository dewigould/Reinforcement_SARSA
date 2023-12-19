# Reinforcement_SARSA
Implementing SARSA algorithm to use reinforcement learning to find best route through a maze


## General Information
Here we implement the SARSA algorithm to find an optimum path through a square maze. The maze is constructed with several pitfalls (places where the agent cannot go), and one entrance and one exit.
- When the agent hits a pitfall she is punished with score $-50$.
- When the agent finds the exit, she is rewarded with score $+10^5$.
- We use an $\epsilon$ greedy policy

At each step of the algorihtm, the action-value function is updated according to
\begin{equation}
q(s,a) \to q(s,a) -\alpha( r(s')+ \gamma q(s',a') - q(s,a) )
\end{equation}


