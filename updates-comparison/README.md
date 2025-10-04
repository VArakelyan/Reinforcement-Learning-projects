# Expected vs. Sample Updates in Planning

This notebook explores the trade-off between two types of updates used in model-based reinforcement learning: **expected updates** and **sample updates**.

**Expected Updates** consider all possible successor states for a given state-action pair, weighting their values by their probabilities. The computational cost is proportional to the branching factor, **b** (the number of possible next states).

**Sample Updates** use the model to simulate just one transition, making them computationally cheaper than expected updates by a factor of **b**.

The experiment addresses the question of how to best allocate a given amount of computation: to a few expected updates or to many sample updates.

# Experimental Setup & Results

The notebook reproduces the analysis shown in *Figure 8.7* of Sutton and Barto's textbook.

- **Scenario**: The analysis focuses on a single state-action pair with an initial value estimate error of 1.  
- **Branching Factors (b)**: The experiment is run for branching factors of 2, 10, 100, and 1000.  
- **Metric**: The Root Mean Squared (RMS) error in the value estimate is plotted against the amount of computation. The cost of one expected update is considered equivalent to the cost of **b** sample updates.

**Key Finding**:  
Sample updates are significantly more computationally efficient, especially for large branching factors. The error in the value estimate falls dramatically with just a few sample updates, achieving a large portion of the potential reduction long before a single, full expected update could be completed.

This suggests that in large-scale problems, it is more beneficial to perform many inexpensive sample updates across a wide range of state-action pairs rather than a few expensive expected updates on a smaller set of pairs.
