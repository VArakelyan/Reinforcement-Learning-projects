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
- Implemented and compared strategies: ε-greedy algorithm, Upper Confidence Bound (UCB), Gradient bandit algorithms.
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
- Applied Value Iteration to compute the optimal policy.
- Explored how stake sizing impacts the probability of reaching the goal.
- Demonstrated the Bellman Optimality Equation.
- Visualized convergence of value function and policy.

### Project 6: Blackjack — Monte Carlo Methods
- Reproduced the episodic Blackjack example (Chapter 5).
- Implemented three Monte Carlo-based methods: Exploring Starts (MC-ES), On-policy ε-greedy control, Off-policy evaluation via importance sampling.
- Used empirical return averaging to estimate action-value functions.
- Visualized optimal state-value functions and learned policies.
- Demonstrated differences between ordinary and weighted importance sampling.

### Project 7: Random Walk – TD(0) Value Estimation
- Re-created the 5-state random-walk example (Ex. 6.2).
- Used one-step TD(0) with a constant step-size α to learn V(s).
- Logged RMSE versus true values and plotted learning curves.

### Project 8: Windy Gridworld – ε-Greedy Sarsa
- Solved the 7×10 Windy Gridworld control task (Ex. 6.5).
- Implemented on-policy one-step Sarsa with ε-greedy exploration.
- Supported king-moves and stochastic wind; tracked steps-per-episode.

### Project 9: Infinite Variance – Off-Policy Monte-Carlo Evaluation
- Replicated the infinite-variance demo (Ex. 5.5) with a 7-state walk.
- Compared ordinary vs. weighted importance sampling for V(π).
- Showed that ordinary IS can diverge while weighted IS converges smoothly.

### Project 10: Cliff Walking – SARSA, Expected SARSA & Q-Learning
- Implemented the 4×12 Cliff-Walking grid (Ex. 6.6).
- Ran SARSA, Expected SARSA, and Q-Learning algorithms.
- Logged average return and steps per episode.
- Visualized final greedy policies.

### Project 11: n-step TD Methods on the Random Walk
- Implemented n-step Temporal-Difference (TD) methods for state-value prediction.
- Conducted experiments varying step-size (α) and number of steps (n).
- Evaluated performance using RMS error over multiple runs and episodes.
- Replicated results from Figure 7.2 of the textbook.

### Project 12: Comparison of Trajectory Sampling Methods
- Compared uniform and on-policy trajectory sampling methods in randomly generated, undiscounted episodic tasks.
- Implemented task generation with up to 10,000 states, two actions per state, and varying branching factors (b = 1, 3, 10).
- Simulated transitions with probabilistic episode termination and Gaussian-distributed rewards.
- Evaluated policy quality by the true value of the start state under the current greedy policy.
- Demonstrated that on-policy sampling is faster initially, while uniform sampling performs better long-term.

### Project 13: Dyna-Q and Planning Experiments
- Reproduced model-based RL experiments from Chapter 8.
- Implemented Dyna-Q, Dyna-Q+, and Prioritized Sweeping algorithms for maze navigation tasks.
- Compared planning performance across agents with 0, 5, and 50 planning steps.
- Tested adaptability in dynamic environments including blocking and shortcut mazes.
- Showed Dyna-Q+ and Prioritized Sweeping achieve faster convergence and better exploration efficiency.

### Project 14: Expected vs. Sample Updates in Planning
- Investigated computational trade-offs between expected and sample updates in model-based RL.
- Implemented experiments replicating Figure 8.7.
- Compared efficiency across branching factors of 2, 10, 100, and 1000.
- Measured RMS error reduction versus computational cost.
- Demonstrated that sample updates yield faster and more efficient error reduction.

### Project 15: Coarseness of Coarse Coding
- Reproduced experiments from Figure 9.8 using coarse coding and linear function approximation.
- Implemented gradient-descent learning to approximate a 1D square-wave function.
- Tested the effect of feature width (narrow, medium, broad) on early generalization and asymptotic performance.
- Generated plots showing the learned function at multiple stages of training.
- Demonstrated that receptive field width strongly influences early learning but has minimal impact on final solution quality.

---

## Clone

```console
$ git clone https://github.com/VArakelyan/Reinforcement-Learning-projects.git
$ cd Reinforcement-Learning-projects
