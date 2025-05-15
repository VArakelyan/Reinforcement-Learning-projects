### **Project 10: Cliff Walking – SARSA, Expected SARSA & Q-Learning**

- **Objective:** Reproduce the Cliff Walking control task and compare three TD-control methods:
  - **SARSA** (on-policy)
  - **Expected SARSA**
  - **Q-Learning** (off-policy)

- **Environment:** 4 × 12 grid  
  Start = (3, 0), Goal = (3, 11)  
  Cells (3, 1) – (3, 10) form the **cliff**. Stepping there returns the agent to Start with **reward –100**.  
  Any other non-terminal move gives **reward –1**. (γ = 1)

- **Methodology**
  1. Initialise `Q(s,a) ≈ 0`.
  2. Run episodes under an ε-greedy policy (fixed ε).
  3. After each transition update **one** of:
     - **SARSA**  
       ```text
       Q[s,a] ← Q[s,a] + α * ( r + γ * Q[s',a'] - Q[s,a] )
       ```
     - **Expected SARSA**  
       ```text
       Q[s,a] ← Q[s,a] + α * ( r + γ * E_{a'}[Q[s',a']] - Q[s,a] )
       ```
     - **Q-Learning**  
       ```text
       Q[s,a] ← Q[s,a] + α * ( r + γ * max_{a'} Q[s',a'] - Q[s,a] )
       ```



