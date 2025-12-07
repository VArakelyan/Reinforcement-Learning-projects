## Mountain Car with Sarsa(λ) and Tile Coding

This project reproduces the Mountain Car control experiment from Sutton & Barto’s *Reinforcement Learning: An Introduction* (Figure 10.4). It uses **Sarsa(λ)** with **tile coding** to solve the continuous control problem.

###  Problem Overview
- The agent must drive an underpowered car up a steep hill.
- It learns to **rock back and forth** to gain enough momentum.
- **State:** Continuous position + velocity  
- **Actions:** Reverse, no throttle, forward  
- **Reward:** -1 per step until reaching the goal  

###  Method
- **Algorithm:** Sarsa(λ) with replacing traces  
- **Function Approximation:** Tile Coding (8 tilings)  
- **Hyperparameters:**  
  - α = 0.3 / 8  
  - λ = 0.9  
  - γ = 1.0  
  - Exploration ϵ = 0 (greedy)  




