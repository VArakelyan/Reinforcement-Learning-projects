## Off-Policy Convergence: Baird’s Counterexample
This project reproduces several experiments from **Chapter 11** of Sutton & Barto’s *Reinforcement Learning: An Introduction*, showcasing the instability of off-policy TD learning with linear function approximation—the classical **Deadly Triad** example.

### Overview
Baird’s counterexample is a 7-state MDP specifically designed to show that:
- Off-policy learning  
- Bootstrapping  
- Function approximation  
together can cause **divergence**, even in a simple linear setup.

This project includes three notebooks demonstrating:
1. **Standard TD diverges**  
2. **Gradient-TD methods stabilize learning**
3. **Emphatic-TD stabilizes through state weighting**

---

## 1. `bairds_counterexample.ipynb` — Standard Off-policy TD
- **Algorithm:** Semi-gradient TD  
- **Goal:** Replicate the classical divergence result  
- **Result:** Weight components grow without bound, matching **Figure 11.2**.  
  Demonstrates how standard TD is not stable off-policy with function approximation.

---

## 2. `tdc_baird.ipynb` — Gradient-TD (GTD/TDC)
- **Algorithm:** TDC (also known as GTD(0))  
- **Idea:** Adds a secondary weight vector to perform true gradient descent on MSPBE  
- **Result:** Reproduces **Figure 11.5**:
  - PBE → converges to 0  
  - VE → decreases slowly  
  GTD methods maintain stability and avoid divergence.

---

## 3. `emphatic_baird.ipynb` — Emphatic TD
- **Algorithm:** Expected Emphatic TD  
- **Idea:** Uses state-dependent emphasis weights to correct the distribution mismatch  
- **Result:** Replicates **Figure 11.6**: all parameters converge and remain stable.  
  Shows that ETD avoids divergence without needing a secondary weight vector.

---

## About the MDP
- **States:** 7 total  
- **Approximation:** Shared linear features across states  
- **Behavior policy:** Stochastic; spreads visits across states  
- **Target policy:** Always chooses the “solid” action  
- **Core Problem:** Behavior-policy state distribution ≠ target-policy distribution → instability under bootstrapping.

---

## Running the Experiments
Install required packages:
