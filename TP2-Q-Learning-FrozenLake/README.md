# FrozenLake-v1 Q-Learning Implementation

![FrozenLake Environment](https://gymnasium.farama.org/_images/frozen_lake.gif)

## Project Overview

This implementation solves Gymnasium's FrozenLake-v1 environment using Q-Learning, demonstrating key reinforcement learning concepts. The agent learns to navigate a 4x4 frozen surface while avoiding holes to reach the goal.

## Key Features

- **Q-Learning Algorithm**: Implements the standard off-policy TD control algorithm
- **ε-Greedy Exploration**: Balances exploration and exploitation with decay schedule
- **Stochastic Environment**: Handles slippery surface conditions (is_slippery=True)
- **Performance Tracking**: Logs success rates and training metrics

## Implementation Details

The solution uses:
- 16 discrete states (4x4 grid)
- 4 possible actions (Left, Down, Right, Up)
- Learning rate (α) = 0.1
- Discount factor (γ) = 0.99
- ε-decay from 1.0 to 0.01 over 5000 episodes

```python
# Core Q-Learning Update
Q_table[state, action] += alpha * (reward + gamma * np.max(Q_table[next_state]) - Q_table[state, action])
