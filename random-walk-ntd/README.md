# n-step TD Methods on the Random Walk

This repository contains a Python implementation to reproduce the results from Figure 7.2 of Sutton and Barto's *Reinforcement Learning: An Introduction*. The experiment evaluates and demonstrates the performance of n-step Temporal-Difference (TD) methods on a 19-state random walk problem.

# The Random Walk Problem

The environment is a 19-state random walk task as described in the book. Key characteristics include:

- **States**: 19 states, plus two terminal states at each end.
- **Actions**: At each state, the agent can move one step to the left or right with equal probability.
- **Rewards**: A reward of -1 is given for transitioning to the leftmost terminal state, and a reward of +1 is given for transitioning to the rightmost terminal state. All other transitions yield a reward of 0.
- **Initialization**: The estimated values for all states are initialized to 0.

The goal of the TD method is to learn the true state values for this Markov Reward Process.

# Experiment Details

The notebook runs an empirical test to compare the performance of n-step TD for various values of n (the number of steps) and α (the step-size parameter).

**Algorithm**: n-step Temporal-Difference (TD)

**Parameters Swept**:
- n (steps): Powers of 2 from 1 to 512 ([1, 2, 4, 8, 16, 32, 64, 128, 256, 512])
- α (step-size): Values from 0.0 to 1.0, with an increment of 0.1.

**Structure**:
- Runs: 100 independent runs are performed.
- Episodes: Each run consists of 10 episodes.
- Performance Metric: The performance is measured by the Root Mean Squared (RMS) error between the learned state-value estimates and the true state values, averaged over the 19 states and the 10 episodes for each run. The final reported error is the average over all 100 runs.
