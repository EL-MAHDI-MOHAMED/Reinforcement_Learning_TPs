# Taxi-v3 Reinforcement Learning Solutions

![Taxi Environment](https://gymnasium.farama.org/_images/taxi.gif)

## Project Overview

This repository implements progressively sophisticated reinforcement learning methods to solve Gymnasium's Taxi-v3 environment. The solution evolves from random exploration to advanced policy optimization techniques.

## Key Implementations

### 1. Random Agent Baseline
- Establishes performance floor with random actions
- Demonstrates environment dynamics
- Rendered visualization available

### 2. Policy Gradient Method
- Tabular policy representation
- Discounted reward calculations
- Simultaneous policy and value function updates
- 100 training episodes

### 3. Proximal Policy Optimization (PPO)
- Experience replay buffer
- Batched policy updates
- Advantage normalization
- Clipped objective for training stability
- 1000 training episodes

## Technical Specifications

| Component          | Configuration           |
|--------------------|-------------------------|
| State Space        | 500 discrete states     |
| Action Space       | 6 discrete actions      |
| Learning Algorithm | Tabular PPO             |
| Training Episodes  | 100 (PG), 1000 (PPO)    |
| Evaluation Runs    | 20 episodes             |

Core hyperparameters:
```python
gamma = 0.99          # Discount factor
lr_policy = 0.01      # Policy network learning rate  
lr_value = 0.1        # Value function learning rate
clip_epsilon = 0.2    # PPO clipping parameter
batch_size = 10       # Experience replay batch size
