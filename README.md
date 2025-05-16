# Reinforcement Learning Projects

This repository contains a collection of Reinforcement Learning (RL) projects developed as part of the Reinforcement Learning course at the National Polytechnic University of Armenia (NPUA).  
Each project explores different RL algorithms and concepts, balancing theoretical insights with practical implementation.

Inspired by Sutton and Barto’s *Reinforcement Learning: An Introduction*.

---

## Projects Overview

### Project 1: Tic-Tac-Toe with Reinforcement Learning
- Developed a Tic-Tac-Toe game environment.
- Implemented a Reinforcement Learning agent capable of learning optimal strategies.
- Enabled users to play against the trained AI to observe its learning progress.

### Project 2: Multi-Armed Bandit Problem
- Investigated the exploration-exploitation trade-off in the multi-armed bandit setting.
- Implemented and compared strategies:
  - ε-greedy algorithm  
  - Upper Confidence Bound (UCB)  
  - Gradient bandit algorithms
- Analyzed the impact of optimistic vs. realistic initial values.

### Project 3: Markov Decision Process (MDP) in Grid-World
- Implemented policy evaluation and value iteration for a 5×5 grid-world.
- Visualized value function convergence under random and optimal policies.
- Demonstrated Bellman equations in finite MDPs.

### Project 4: Dynamic Programming (DP) in Grid-World
- Performed policy evaluation and improvement in a 4×4 grid-world with terminal states.
- Compared in-place vs. out-of-place dynamic programming updates.
- Analyzed theoretical guarantees of policy improvement.

### Project 5: Gambler’s Problem – Value Iteration Approach
- Simulated the Gambler’s Problem as a finite Markov Decision Process (MDP).
- Applied the Value Iteration algorithm to compute the optimal policy.
- Explored how stake sizing impacts the probability of reaching the goal.
- Demonstrated use of the Bellman Optimality Equation.
- Visualized convergence of value function and policy.

### Project 6: Blackjack — Monte Carlo Methods
- Reproduced the episodic Blackjack example from Sutton & Barto (Chapter 5).
- Implemented three Monte Carlo-based methods:
  - Exploring Starts (MC-ES)  
  - On-policy control with ε-greedy exploration  
  - Off-policy prediction via importance sampling
- Used empirical return averaging to estimate action-value functions.
- Visualized optimal state-value functions and learned policies.
- Demonstrated the practical differences between ordinary and weighted importance sampling in off-policy evaluation.

### Project 7: Random Walk – TD(0) Value Estimation
- Re-created the 5-state random-walk example (Sutton & Barto, Ex. 6.2).
- Used one-step TD(0) with a constant step-size α to learn V(s).
- Logged RMSE versus the true values; plotted learning curves.

### Project 8: Windy Gridworld – ε-Greedy Sarsa
- Solved the 7 × 10 Windy Gridworld control task (Ex. 6.5).
- Implemented on-policy one-step Sarsa with ε-greedy exploration.
- Supports king-moves and stochastic wind; tracks steps-per-episode.

### Project 9: Infinite Variance – Off-Policy Monte-Carlo Evaluation
- Replicated the infinite-variance demo (Ex. 5.5) with a 7-state walk.
- Compared ordinary importance sampling vs. weighted IS for V(π).
- Showed how ordinary IS blows up while weighted IS converges smoothly.

### Project 10: Cliff Walking – SARSA, Expected SARSA & Q-Learning
- Implemented the 4 × 12 Cliff-Walking grid (Ex. 6.6).
- Ran three TD-control algorithms (SARSA, Expected SARSA, Q-Learning).
- Logged average return & steps per episode; visualised final greedy policies.

---
## Clone 

```console
$ git clone https://github.com/VArakelyan/Reinforcement-Learning-projects.git
$ cd Reinforcement-Learning-projects

