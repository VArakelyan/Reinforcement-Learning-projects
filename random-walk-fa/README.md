# Function Approximation in Reinforcement Learning

This project reproduces several key experiments from **Chapter 9** of Sutton and Barto’s *“Reinforcement Learning: An Introduction.”*  
It explores various **function approximation techniques**, including **state aggregation**, **polynomial and Fourier bases**, **tile coding**, and the **effects of bootstrapping** in reinforcement learning.

---

## Overview

Function approximation allows reinforcement learning agents to generalize from limited experience by mapping large or continuous state spaces into a compact set of parameters.  
This notebook collection demonstrates how different function approximation methods impact learning behavior, accuracy, and stability in a controlled 1000-state random walk environment.

---

## Experiments

### 1. State Aggregation on a 1000-State Random Walk
- **Task:**  
  A 1000-state random walk where the agent moves left or right with equal probability.  
  Episodes start in the center and terminate at either end, with rewards of **-1** on the left and **+1** on the right.  
- **Function Approximation:**  
  The 1000 states are grouped into **10 contiguous sets of 100 states** each.  
  Each group shares a single learned weight representing all contained states.  
- **Algorithm:**  
  Gradient-descent Monte Carlo.  
- **Results:**  
  The learned value function forms a **coarse, step-wise approximation** of the true values.  
  Errors are smallest near the middle and largest at the ends due to uneven sample visitation.

---

### 2. Polynomial vs. Fourier Basis
- **Task:**  
  Same 1000-state random walk as in the previous experiment.  
- **Function Approximation:**  
  - **Polynomial Basis:** Orders 5, 10, and 20.  
  - **Fourier Basis:** Cosine terms of orders 5, 10, and 20.  
- **Algorithm:**  
  Gradient-descent Monte Carlo with constant step-size α.  
- **Results:**  
  - **Fourier basis** provides stable and accurate approximations.  
  - **Polynomial basis** becomes unstable at high orders, often diverging.  
  - Demonstrates that Fourier features offer better **numerical stability** and **generalization** in non-linear value landscapes.

---

### 3. Tile Coding on a 1000-State Random Walk
- **Task:**  
  1000-state random walk identical to the previous setups.  
- **Function Approximation:**  
  **Tile coding** with 50 tilings, each tile spanning **200 states**.  
  Each state is represented by the set of active tiles across all tilings.  
- **Algorithm:**  
  Gradient-descent Monte Carlo with constant step-size α.  
- **Results:**  
  Tile coding produces a **fine-grained and smooth approximation** of the true value function.  
  It balances **local sensitivity** (via multiple overlapping tilings) with **robust generalization**, outperforming state aggregation and polynomial bases in stability.

---

### 4. Bootstrapping with Function Approximation
- **Task:**  
  1000-state random walk.  
- **Function Approximation:**  
  State aggregation with **20 groups of 50 states** each.  
- **Algorithms Compared:**  
  - **Gradient Monte Carlo:** Non-bootstrapping; updates occur only after full episodes.  
  - **TD(0):** Bootstrapping; updates occur at each time step using value estimates.  
- **Performance Metric:**  
  Root Mean Squared Error (RMSE) between learned and true value functions.  
- **Results:**  
  - **TD(0)** learns faster initially but exhibits bias due to bootstrapping.  
  - **Monte Carlo** converges more slowly but achieves a more accurate asymptotic estimate.  
  - Demonstrates the **bias-variance trade-off** inherent in bootstrapped updates with function approximation.

---

