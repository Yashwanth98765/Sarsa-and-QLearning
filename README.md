# Sarsa and Q-Learning: Cliff Walking Problem 🤖⛰️

This repository contains a comparative study and implementation of two fundamental **Temporal Difference (TD) Reinforcement Learning** algorithms: **Sarsa (On-policy)** and **Q-Learning (Off-policy)**. The project demonstrates how these agents learn to navigate the classic "Cliff Walking" gridworld environment.

---

## 📌 Project Overview
The objective is to train an agent to move from a **Start (S)** to a **Goal (G)** in a gridworld while avoiding a **Cliff (C)**. 
- **The Challenge:** Falling into the cliff results in a large negative reward (-100) and resets the agent.
- **The Comparison:** This project visualizes why Sarsa learns a "safer" path while Q-Learning learns the "optimal but risky" path.

---

## 🧠 Algorithms Implemented

### 1. Sarsa (On-Policy)
Sarsa updates its Q-values based on the action actually taken by the current policy (including exploration steps).
> **Update Rule:** > $$Q(S, A) \leftarrow Q(S, A) + \alpha [R + \gamma Q(S', A') - Q(S, A)]$$

### 2. Q-Learning (Off-Policy)
Q-Learning updates its Q-values based on the maximum possible reward of the next state, assuming the agent will act optimally in the future.
> **Update Rule:** > $$Q(S, A) \leftarrow Q(S, A) + \alpha [R + \gamma \max_{a} Q(S', a) - Q(S, A)]$$

---

## 🛠️ Tech Stack
* **Language:** Python 3.x
* **Libraries:** * `NumPy`: For Q-Table management and mathematical operations.
    * `Matplotlib`: For plotting reward convergence and path analysis.
    * `Gymnasium/Gym`: For the CliffWalking-v0 environment.

---

## 📊 Key Insights & Results
The implementation includes a detailed comparison of:
* **Learning Curves:** Plotting the sum of rewards per episode to observe convergence speed.
* **Policy Comparison:** * **Sarsa** avoids the edge of the cliff to account for the $\epsilon$ probability of a random move.
    * **Q-Learning** walks right along the edge of the cliff, which is the shortest path but riskier during training.

---

## 🚀 How to Use
1. **Clone the repository:**
   ```bash
   git clone
