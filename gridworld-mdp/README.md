Markov Decision Process (MDP) in Grid-World

This project implements MDP solution methods—policy evaluation and value iteration—for a 5×5 grid-world environment, based on Reinforcement Learning: An Introduction by Sutton & Barto. It demonstrates how Bellman equations converge to optimal value functions and policies in a finite MDP with discrete states and actions.

Key Components

State Space: 5×5 grid (25 states)
Action Space: {↑, ↓, ←, →}
Transition Model: Deterministic (edge collisions handled)
Reward Function:

State A = +10, State B = +5
Edges = -1, Other states = 0
Discount Factor (γ): 0.9
Algorithms

Policy Evaluation: Solves the Bellman Expectation Equation for a fixed policy.
Value Iteration: Solves the Bellman Optimality Equation to find the optimal policy.
Results

Policy Evaluation: Shows value function convergence for a random policy.
Value Iteration: Finds the optimal policy, with multiple optimal actions in some states.

How to Run

Install Dependencies: Ensure all required libraries are installed.
Run the Code: Open grid_world.py in PyCharm and run the script.
Generated Plots: Plots are saved in the generated_images/ folder.