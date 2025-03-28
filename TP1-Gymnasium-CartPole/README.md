# CartPole-v1 Reinforcement Learning Experiments

![CartPole Environment](https://gymnasium.farama.org/_images/cart_pole.gif)

This repository contains a series of experiments with the CartPole-v1 environment from Gymnasium, demonstrating fundamental reinforcement learning concepts through practical implementations.

## Table of Contents
- [Environment Overview](#environment-overview)
- [Experiments](#experiments)
  - [Random Agent Baseline](#1-random-agent-baseline)
  - [Action-Observation Analysis](#2-action-observation-analysis)
  - [Manual Control](#3-manual-control)
  - [Statistical Analysis](#4-statistical-analysis)
- [Key Metrics](#key-metrics)
- [Requirements](#requirements)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Environment Overview

The CartPole-v1 environment features:
- **State space**: 4 continuous values
  - Cart position
  - Cart velocity
  - Pole angle
  - Pole angular velocity
- **Action space**: 2 discrete actions
  - 0: Push cart to the left
  - 1: Push cart to the right
- **Reward**: +1 for every step the pole remains upright
- **Termination conditions**:
  - Pole angle > 12° from vertical
  - Cart position > 2.4 units from center
  - Episode length > 500 steps

## Experiments

### 1. Random Agent Baseline
Demonstrates basic environment interaction with random actions:
```python
for _ in range(100):
    action = env.action_space.sample()
    observation, reward, terminated, truncated, info = env.step(action)
