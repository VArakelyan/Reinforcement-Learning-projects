### 🎰 **Project 5: Gambler’s Problem – Value Iteration Approach**

- Simulated the **Gambler’s Problem** as a finite MDP, where states represent capital values from 0 to 100.
- Implemented the **Value Iteration** algorithm to iteratively compute the optimal state-value function.
- Defined actions as all possible stakes bounded by the current capital and distance to the goal.
- Used a biased coin flip (p = 0.4 for heads) to define stochastic transitions.
- Designed the reward structure to give **+1 only when reaching the goal (capital = 100)**; all other transitions yield 0.
- Extracted the optimal policy by choosing the stake at each state that maximizes expected value.
- Visualized:
  - 📈 Value function updates across sweeps
  - 🧠 Final optimal policy (stakes per capital)

📘 *Based on Sutton & Barto, Reinforcement Learning: An Introduction – Figure 4.3*
