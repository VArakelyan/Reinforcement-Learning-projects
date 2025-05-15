### **Project 10: Cliff Walking – SARSA, Expected SARSA & Q-Learning**

- **Objective:** Reproduce the Cliff Walking control task (Sutton & Barto, RL 2nd ed., Example 6.6) and compare three TD-control methods:
  - **SARSA** (on-policy)
  - **Expected SARSA**
  - **Q-Learning** (off-policy)

- **Environment:** 4 × 12 grid.  
  Start = (3, 0), Goal = (3, 11).  
  Cells (3, 1) – (3, 10) form the **cliff**: stepping there returns the agent to the start with **−100 reward**.  
  Every non-terminal move costs **−1 reward** (γ = 1).

- **Methodology:**
  - Initialise \(Q(s,a)\approx 0\).
  - Run episodes under an ε-greedy policy (ε fixed).
  - **Updates**
    - SARSA: \(Q(s,a)\leftarrow Q(s,a)+\alpha\,[r+\gamma Q(s',a')-Q(s,a)]\)
    - Expected SARSA: \(Q(s,a)\leftarrow Q(s,a)+\alpha\,[r+\gamma\,\mathbb E_{a'}Q(s',a')-Q(s,a)]\)
    - Q-Learning: \(Q(s,a)\leftarrow Q(s,a)+\alpha\,[r+\gamma \max_{a'}Q(s',a')-Q(s,a)]\)
  - Track **return per episode** and **steps per episode** to build learning curves.


