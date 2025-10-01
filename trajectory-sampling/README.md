# Comparison of Trajectory Sampling Methods

The experiment compares two trajectory sampling methods, **uniform** and **on-policy**, for planning in randomly generated, undiscounted episodic tasks.

# Experimental Setup

## Task Generation
- Tasks involve either **1,000** or **10,000 states**.
- From each state, two actions are possible.
- Each action transitions to one of **b possible next states** with equal probability. The branching factor **b** was tested for values of 1, 3, and 10.
- On every transition, there is a **0.1 probability** of the episode ending.
- Expected rewards for each transition are selected from a **Gaussian distribution** with mean 0 and standard deviation 1.

## Sampling Methods
- **Uniform**: Cycles through and updates every state-action pair.
- **On-policy**: Simulates episodes from a single start state and updates the state-action pairs that occurred while following the current ε=0.1-greedy policy.

## Performance Metric
- The quality of the policy is measured by the **true value of the start state under the current greedy policy**.
- This value is plotted against the number of expected updates completed.

# Results

- Results are averaged over **200 sample tasks**.
- **General Performance**: On-policy sampling resulted in faster planning initially but was slower in the long run compared to uniform sampling.
- **Effect of Branching Factor**: The initial advantage of on-policy sampling was stronger and lasted longer for smaller branching factors.
- **Effect of State Space Size**: The advantage of on-policy sampling becomes larger and more long-lasting as the number of states increases. This is demonstrated in the experiment with **10,000 states** and a **branching factor of 1**.
