## Random Walk with Function Approximation

This project implements several function-approximation methods for the **1000-state Random Walk** from Sutton & Barto’s *“Reinforcement Learning: An Introduction”* (Chapter 9).  
It compares how different representations generalize, converge, and approximate the true value function.

### The Task
A 1000-state random walk:
- The agent moves **left or right** with equal probability.
- Episodes start in the **center** and end at the boundaries.
- Terminal rewards: **−1** on the left end, **+1** on the right.
- Goal: Learn the state-value function under the random policy.

### Experiments Included
#### 1. State Aggregation
- 1000 states grouped into **10 equal segments**.  
- Updated using **gradient Monte Carlo**.  
- Produces a coarse step-wise approximation that improves with more samples.

#### 2. Polynomial vs. Fourier Bases
- Polynomial bases (orders **5, 10, 20**)  
- Fourier cosine bases (orders **5, 10, 20**)  
- Fourier features remain stable and accurate; high-order polynomials diverge.  
- Highlights the importance of smooth, bounded basis functions.

#### 3. Tile Coding
- **50 tilings**, each tile covering **200 states**.  
- More expressive than aggregation without instability.  
- Produces a fine, piecewise approximation that tracks the true function well.

#### 4. Bootstrapping Comparison
- State aggregation with **20 groups**.  
- Algorithms: **Monte Carlo** vs. **TD(0)**  
- MC → lower bias but slower  
- TD(0) → faster learning but biased  
- Demonstrates the classic bias–variance trade-off.

### How to Run
Run the notebook:

```bash
jupyter notebook random_walk.ipynb
