#  CartPole-v1 Reinforcement Learning Experiments

![CartPole Simulation](https://gymnasium.farama.org/_images/cart_pole.gif)

*A hands-on exploration of reinforcement learning fundamentals using Gymnasium's classic control environment*

##  Table of Contents
- [Project Overview](#-project-overview)
- [Environment Specifications](#-environment-specifications)
##  Project Overview

This repository contains a series of progressively complex experiments with the CartPole-v1 environment, designed to:
- Demonstrate core RL concepts
- Provide hands-on coding examples
- Establish performance benchmarks
- Serve as a foundation for more advanced algorithms

## Environment Specifications

### Observation Space
| Index | Description        | Range          |
|-------|-------------------|---------------|
| 0     | Cart Position     | [-4.8, 4.8]   |
| 1     | Cart Velocity     | (-∞, ∞)       |
| 2     | Pole Angle        | [-24°, 24°]   |
| 3     | Pole Velocity     | (-∞, ∞)       |

### Action Space
- `0`: Push cart left
- `1`: Push cart right

### Reward System
- +1 for every timestep the pole remains upright

### Termination Conditions
- Pole angle > ±12°
- Cart position > ±2.4 units
- Episode length > 500 steps (solved)

##  Experiments

### Random Agent Baseline
```python
env = gym.make("CartPole-v1")
for _ in range(100):
    action = env.action_space.sample()
    obs, reward, done, _, _ = env.step(action)
    if done: env.reset()
