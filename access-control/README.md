## Access Control Queuing Task  

This project reproduces the **Access Control Queuing Task** experiment from **Chapter 10** of Sutton & Barto’s *“Reinforcement Learning: An Introduction.”*  
It demonstrates the effectiveness of **Sarsa(λ)** with **tile coding** on a continuous-time, stochastic control problem.

### The Task  
The environment simulates a **server managing incoming jobs** with varying priorities.  

- **Objective:** Maximize total reward by deciding whether to **accept or reject jobs**.  
- **Job Arrivals:** Jobs arrive as a Poisson process with priorities of **1, 2, 4, or 8**.  
- **Actions:**  
  - `Accept (1)` → receive reward = job priority (only if server is free)  
  - `Reject (0)` → reward = 0  
- **Constraint:** The server can process **only one job at a time**. If it’s busy and another job is accepted, the job is lost (reward = 0).  
- **Server Status:** After accepting a job, the server becomes busy. With **p = 0.06**, it may finish and become free at each time step.  
