# **Tic-Tac-Toe Reinforcement Learning Project**  

This project is a **Reinforcement Learning (RL) implementation** of the classic **Tic-Tac-Toe** game.  
Developed as part of my university program at **NPUA (National Polytechnic University of Armenia)**, the goal is to train an RL agent to play **Tic-Tac-Toe optimally** and compete against either **another RL agent** or a **human player**.  

---

## **🚀 Features**  

### **🧠 Reinforcement Learning Player (RLPlayer)**  
- Uses **Temporal-Difference Learning** to estimate state values.  
- Implements **ε-greedy strategy** for exploration during training.  
- Supports **saving and loading** learned policies for reuse.  

### **🎮 Human Player**  
- Allows a human to play against the trained RL agent.  

### **⚖️ Judge (Game Manager)**  
- Manages the game flow between two players (**RL vs RL** or **RL vs Human**).  

### **🔢 State Management**  
- Represents the **Tic-Tac-Toe board** and computes unique **hash values** for each state.  
- Checks for game-ending conditions (**win, lose, or tie**).  

---

## **🛠️ How It Works**  

### **📌 Training Mode**  
- Two **RL players** train by playing against each other for a specified number of epochs.  
- **Win rates** are tracked and displayed periodically.  

### **🏆 Competition Mode**  
- Two trained **RL players** compete against each other to evaluate their performance.  

### **🎮 Play Mode**  
- A **human player** can challenge the trained RL agent to test its performance.  

---

## **💻 How to Run**  

### **1️⃣ Clone the Repository**  
```bash
git clone https://github.com/VArakelyan/Reinforcement-Learning-projects
cd Reinforcement-Learning-projects/tic-tac-toe
