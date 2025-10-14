# Coarseness of Coarse Coding

This repository contains a Python implementation that reproduces the results from Figure 9.8 of Sutton and Barto's *Reinforcement Learning: An Introduction*. The experiment demonstrates the effect of receptive field size (coarseness) on learning with linear function approximation based on coarse coding.

# Experiment Details

The goal is to learn a one-dimensional square-wave function using gradient-descent learning.

- **Task**: Approximate a 1D square-wave function using its values as training targets.  
- **Features**: In this one-dimensional case, the receptive fields for coarse coding are intervals of varying widths.  
- **Key Variable**: The experiment is repeated with three different feature widths:  
  - Narrow (width = 0.2)  
  - Medium (width = 0.4)  
  - Broad (width = 1.0)  
- **Control**: The density of features is kept the same in all three cases (about 50 features across the domain) to ensure a fair comparison.  
- **Training**: Training examples are generated uniformly at random from the domain. Learning progress is observed after 10, 40, 160, 640, 2560, and 10240 samples.  

# Results and Conclusion

The notebook generates plots showing the learned function at different stages of training for each feature width.

- **Early Learning**: The width of the features strongly impacts early generalization.  
  - Broad features produce a smooth, broad generalization.  
  - Narrow features result in a more localized and "bumpy" approximation because updates only affect close neighbors of a trained point.  
- **Asymptotic Performance**: With more training examples, the final learned function is only slightly affected by feature width. All three cases converge to a good approximation of the target square wave.  

**Key Takeaway**: Receptive field shape strongly affects early generalization but has little impact on the asymptotic quality of the solution.
