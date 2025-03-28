# Taxi-v3 Reinforcement Learning Implementations

![Taxi-v3 Environment](../../images/taxi_env.png)  
*The Gymnasium Taxi-v3 environment showing agent (yellow), passenger (blue), and destinations (RGBY)*

This Python file contains multiple reinforcement learning approaches for solving Gymnasium's Taxi-v3 environment, progressing from simple to more advanced techniques.

## Contents

1. **Random Agent Baseline**
   - Takes random actions to demonstrate environment basics
   - Runs for 100 steps with environment rendering

2. **Extended Random Agent**
   - Runs 20 episodes with step-by-step logging
   - Tracks and displays total reward per episode

3. **Basic Policy Gradient**
   - Tabular policy implementation
   - Discounted reward calculation
   - Policy and value function updates
   - 100 training episodes

4. **Policy Evaluation**
   - Tests the trained policy over 20 episodes
   - Reports average and individual episode rewards

5. **Proximal Policy Optimization (PPO)**
   - Advanced policy gradient with experience replay
   - Batch updates and advantage normalization
   - Clipped policy updates for stability
   - 1000 training episodes with periodic evaluation

## Key Parameters

| Parameter           | Value  | Description                          |
|---------------------|--------|--------------------------------------|
| `gamma`            | 0.99   | Discount factor                     |
| `lr_policy`        | 0.01   | Policy learning rate                |
| `lr_value`        | 0.1    | Value function learning rate        |
| `clip_epsilon`    | 0.2    | PPO clipping parameter              |
| `num_episodes`    | 100/1000 | Training episodes                  |
| `batch_size`      | 10     | PPO batch size                      |

## Usage

```python
# Run specific sections by uncommenting:
# 1. Random agent
# env = gym.make("Taxi-v3", render_mode="human") 

# 2. Policy Gradient training
# env = gym.make("Taxi-v3")

# 3. PPO training
# env = gym.make("Taxi-v3")
