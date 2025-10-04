# Dyna-Q and Planning Experiments

This project reproduces key experiments on model-based reinforcement learning from Chapter 8 of Sutton and Barto's textbook. It explores the Dyna-Q, Dyna-Q+, and Prioritized Sweeping algorithms in changing and static maze environments.

# Experiments

## 1. Dyna Maze
This experiment compares Dyna-Q agents with 0, 5, and 50 planning steps (n) in a 6×9 maze.  
The results show that planning (n > 0) dramatically accelerates learning compared to the non-planning (n=0) Q-learning agent.

## 2. Changing Mazes (Dyna-Q+)
This experiment evaluates Dyna-Q and Dyna-Q+ in two dynamic mazes:
- **Blocking Maze**: a path is blocked after initial learning.
- **Shortcut Maze**: a new, shorter path becomes available.

While both agents solve the blocking task, only Dyna-Q+, with its exploration bonus for long-untried actions, successfully discovers the new shortcut.

## 3. Prioritized Sweeping
This test compares the efficiency of standard Dyna-Q's random planning with Prioritized Sweeping on mazes of increasing size.  
Prioritized Sweeping, which focuses updates based on value changes, requires significantly fewer backups to find the optimal solution.
