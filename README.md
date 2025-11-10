# 🤖 Q-Learning & Double Q-Learning — Advanced Reinforcement Learning in Gridworld  
> **Exploration vs. Exploitation • Dynamic Obstacles • Multi-Agent Ready Framework**

<p align="center">
  <img src="https://img.shields.io/badge/Algorithm-Q%20Learning-1E90FF?logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Variant-Double%20Q%20Learning-FF69B4?logo=pytorch&logoColor=white" />
  <img src="https://img.shields.io/badge/Category-Reinforcement%20Learning-8A2BE2" />
  <img src="https://img.shields.io/badge/Environment-Custom%20Gridworld-green" />
  <img src="https://img.shields.io/badge/Visualization-Matplotlib-yellow" />
</p>

---

## ✨ Overview

This project implements **Q-Learning** and its robust variant **Double Q-Learning** in a **stochastic Gridworld environment** filled with **holes**, **obstacles**, and **goals**.  
It visualizes **policy evolution**, **learning curves**, and **reward optimization** — highlighting how agents learn optimal behavior through trial and error.

💡 **Goal:** Enable an agent to navigate complex terrain while maximizing total rewards using reinforcement learning principles.

---

## 🚀 Features

- ⚙️ **Q-Learning & Double Q-Learning**
  - Compare traditional vs. double estimators for value correction  
- 🧭 **Customizable Gridworld**
  - Multiple goals, holes, traps, and dynamic start positions  
- 🧩 **Adaptive Exploration**
  - ε-greedy policy with exponential decay for stable convergence  
- 🧮 **Reward Optimization**
  - Configurable reward matrices for different training difficulties  
- 📊 **Visualization Suite**
  - Training curves, reward histograms, and policy maps  
- 💾 **Exportable Knowledge**
  - Save learned `Q`, `Q1`, and `Q2` tables to CSV for reuse  

---

## 🧠 Algorithmic Insight

### 🔹 Q-Learning Update Rule
\[
Q(s,a) \leftarrow Q(s,a) + \alpha [R(s,a) + \gamma \max_{a'} Q(s',a') - Q(s,a)]
\]

### 🔹 Double Q-Learning Update Rule
\[
Q_1(s,a) \leftarrow Q_1(s,a) + \alpha [R + \gamma Q_2(s', \arg\max_{a'} Q_1(s',a')) - Q_1(s,a)]
\]
\[
Q_2(s,a) \leftarrow Q_2(s,a) + \alpha [R + \gamma Q_1(s', \arg\max_{a'} Q_2(s',a')) - Q_2(s,a)]
\]

🧩 The **Double Q-Learning** approach minimizes overestimation bias by splitting the value function estimation between two independent Q-tables.

---

## 📈 Visualizations

🎨 Generated automatically in the notebook:

- 🗺️ **Final Policy Map** – optimal moves for each state  
- 📈 **Reward Convergence Plot** – mean episodic reward progression  
- 🔥 **Exploration-Exploitation Trend** – epsilon decay visualization  
- 🧩 **Trajectory Visualization** – shows agent navigation paths  
- 💾 **Q-Table Heatmap** – visual structure of learned action-values  

---

## 💻 Tech Stack

<p align="center">
  <img src="https://img.shields.io/badge/Language-Python-3776AB?logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Libraries-NumPy%20%7C%20Matplotlib%20%7C%20Pandas-FFDD00?logo=plotly&logoColor=white" />
  <img src="https://img.shields.io/badge/Progress-tqdm-00C853" />
  <img src="https://img.shields.io/badge/Notebook-Jupyter%20%7C%20Colab-orange" />
</p>

---

## 🧩 How It Works

1️⃣ Define the **Gridworld Environment** — including holes, obstacles, and rewards  
2️⃣ Initialize **Q-tables** (or **Q1 & Q2**) with zeros  
3️⃣ Apply **ε-greedy policy** for exploration vs. exploitation  
4️⃣ Update Q-values iteratively based on agent experience  
5️⃣ Visualize and **export learned policies and metrics**

---

## 🧠 Key Learnings

- **Double Q-Learning** stabilizes learning by reducing bias  
- **Reward shaping** impacts convergence speed and exploration  
- **Exploration decay** balances random exploration and exploitation  
- **State–action heatmaps** reveal decision clustering  

---

## 🧪 Future Enhancements

- 🧠 Integrate **Deep Q-Network (DQN)** for function approximation  
- 🔄 Add **moving obstacles** or time-varying rewards  
- 🕹️ Support **multi-agent learning and collaboration**  
- 🎥 Generate **animated training visualization (GIF)**  
- 📊 Compare **SARSA vs. Q-Learning vs. Double Q-Learning**

---

## 👨‍💻 Author

**Sam Dennis**  
🎓 MSc AI & ML — Christ University  
💼 Research Focus: Reinforcement Learning & IoT Security  
🌐 [LinkedIn](https://www.linkedin.com/in/samdennis) • [GitHub](https://github.com/your-username)

---

> “True intelligence isn’t about knowing the path — it’s about learning to walk it.” 🌍
