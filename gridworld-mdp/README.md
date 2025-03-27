Markov Decision Process (MDP) in Grid-World
This project applies MDP solution techniques—policy evaluation and value iteration—within a 5×5 grid-world environment, as described in Reinforcement Learning: An Introduction by Sutton & Barto. It shows how Bellman equations can converge to optimal value functions and policies in a finite MDP with discrete states and actions.

Key MDP Components

Component	Implementation Details
State Space (S)	5×5 grid (25 discrete states)
Action Space (A)	{↑, ↓, ←, →}
Transition Model	Deterministic (with exceptions at edge collisions)
Reward Function	Special states (A=+10, B=+5), edges = -1, others = 0
Discount (γ)	0.9
Algorithms Implemented

Policy Evaluation
Solves the Bellman Expectation Equation for a fixed policy 
π
π:

Input: Uniform random policy 
π
(
a
∣
s
)
=
0.25
π(a∣s)=0.25 for all actions
Output: Converged value function (see Figure 3.2)
Value Iteration
Solves the Bellman Optimality Equation by iteratively updating the value function 
v
(
s
)
v(s) and improving the policy. The update rule used at each iteration is:

Output: Optimal value function and policy (see Figure 3.5)

Once 
v
(
s
)
v(s) converges, the optimal policy is derived.
Results & MDP Insights

Policy Evaluation (Random Policy):
Observations:
States near the edges have negative values due to the high penalty probability.
State A’s value (8.79) is less than +10 due to potential transitions leading to edge states.
Demonstrates the outcome of policy evaluation for a given 
π
π.
Value Iteration (Optimal Policy):
Observations:
Arrows indicate multiple optimal actions in some states.
State B’s value exceeds +5 due to a strategic path through state B’.
Shows policy improvement through value iteration.
Theoretical Implications

MDP Fundamentals:
States, actions, rewards, and the discount factor 
γ
γ fully define the problem.
The discount factor 
γ
=
0.9
γ=0.9 balances long-term versus immediate rewards.
Bellman Equations:
Policy evaluation is the iterative solution of linear equations.
Value iteration is dynamic programming with a max operator.
Optimality:
An optimal policy exists for finite MDPs (as per Bellman’s principle of optimality).
How to Run

Install Dependencies:
Install the necessary libraries for the project.
Run the Jupyter Notebook:
jupyter notebook grid_world.ipynb
Generated Plots:
All generated plots will be saved in the ../generated_images/ directory.