# **Multi-Armed Bandit Reinforcement Learning Project**  

This project simulates the **multi-armed bandit problem** using **epsilon-greedy strategies**.  
It generates **plots** to visualize the **average reward** and **percentage of optimal actions** over time for different **epsilon values**.  

---

## **🚀 Features**  
- Simulates **multi-armed bandit problems** with customizable **epsilon values**.  
- Generates **plots** for **average reward** and **percentage of optimal actions**.  
- Supports **sample-averages** and **constant step-size** methods for action-value estimation.  

---

## **🛠️ How It Works**  

### **🎰 Bandit Class**  
- Implements the **epsilon-greedy algorithm** for action selection.  
- Updates **action values** based on received rewards.  

### **📊 Simulation**  
- Runs multiple **independent experiments** with different **epsilon values**.  
- Calculates **mean rewards** and **optimal action selection percentages**.  

### **📈 Plotting**  
- Visualizes the results using **Matplotlib**.  
- Saves the plots as **high-resolution images**.  

---

## **📦 Requirements**  
Ensure all dependencies are installed:  

```bash
pip install -r requirements.txt
