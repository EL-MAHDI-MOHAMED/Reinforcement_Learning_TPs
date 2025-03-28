# Reinforcement Learning Gymnasium Projects

![Environments](https://gymnasium.farama.org/_static/gymnasium.gif)

This repository contains implementations of reinforcement learning algorithms for three classic Gymnasium environments.

## Table of Contents

### 1. Taxi-v3 Projects
- [1.1 Random Agent](#11-random-agent)
- [1.2 Policy Gradient](#12-policy-gradient)
- [1.3 PPO Implementation](#13-ppo-implementation)
- [1.4 Evaluation Metrics](#14-evaluation-metrics)

### 2. CartPole-v1 Projects
- [2.1 Random Agent Baseline](#21-random-agent-baseline)
- [2.2 Action-Observation Analysis](#22-action-observation-analysis)
- [2.3 Manual Control](#23-manual-control)
- [2.4 Statistical Analysis](#24-statistical-analysis)

### 3. FrozenLake-v1 Projects
- [3.1 Q-Learning Implementation](#31-q-learning-implementation)
- [3.2 Q-Table Analysis](#32-q-table-analysis)
- [3.3 Policy Evaluation](#33-policy-evaluation)

### 4. General Information
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

---

## 1. Taxi-v3 Projects

### 1.1 Random Agent
Basic implementation demonstrating random actions in the Taxi environment.

### 1.2 Policy Gradient
Tabular policy gradient implementation with:
- Discounted rewards
- Advantage estimates
- Value function baseline

### 1.3 PPO Implementation
Proximal Policy Optimization featuring:
- Experience replay buffer
- Batch updates
- Clipped policy updates
- Advantage normalization

### 1.4 Evaluation Metrics
Performance evaluation across 20 episodes showing:
- Average reward: +8 to +15
- Best episode performance
- Training progression

---

## 2. CartPole-v1 Projects

### 2.1 Random Agent Baseline
Basic environment interaction with random actions.

### 2.2 Action-Observation Analysis
Examines the relationship between actions and environment responses.

### 2.3 Manual Control
Human-controlled cartpole through terminal input.

### 2.4 Statistical Analysis
Quantitative evaluation of random agent performance:
- Average duration: 4.92s ± 0.85s
- Average steps: 21.4 ± 3.7

---

## 3. FrozenLake-v1 Projects

### 3.1 Q-Learning Implementation
Features:
- ε-greedy policy
- Bellman equation updates
- Learning rate: 0.1
- Discount factor: 0.99

### 3.2 Q-Table Analysis
Examination of the learned Q-values across states.

### 3.3 Policy Evaluation
Performance metrics:
- Success rate: 75% (slippery surface)
- Training episodes: 5000
- Final ε: 0.01

---

## General Information

### Requirements
- Python 3.7+
- Gymnasium
- NumPy

### Installation
```bash
git clone https://github.com/yourusername/rl-gymnasium-projects.git
cd rl-gymnasium-projects
pip install -r requirements.txt
