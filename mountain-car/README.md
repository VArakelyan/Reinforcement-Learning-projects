### Project 17: Mountain Car with Sarsa(λ) and Tile Coding  

Reproduces **Figure 10.4** from Sutton & Barto’s *“Reinforcement Learning: An Introduction.”*  
Implements **Sarsa(λ)** with **tile coding** to solve the **Mountain Car** problem.

#### Overview  
- **Task:** Car must reach the top of a steep hill by building momentum in a valley.  
- **State:** 2D — position & velocity  
- **Actions:** Reverse (-1), coast (0), forward (+1)  
- **Reward:** -1 per step until goal  

#### Experiment Setup  
- **Algorithm:** Sarsa(λ) with linear function approximation  
- **Representation:** 8 tilings (tile coding)  
- **Parameters:**  
  - α = 0.3 / 8  
  - γ = 1.0  
  - λ = 0.9  
  - ε = 0 (greedy policy)  

#### Results  
- Trained for **500 episodes**, visualizing the **cost-to-go** function at episodes 1, 12, 104, and 500.  
- The agent learns a **valley-shaped value function**, identifying high-momentum states as valuable for reaching the goal.  

#### How to Run  
Run `mountain_car.ipynb` (requires `numpy`, `matplotlib`, `tqdm`).  
Generates `figure_10_4.png` in `generated_images/`.  
