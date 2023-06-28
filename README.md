# Project Goal:
- Implementing the PPO Algorithm
- Selecting and conducting experiments with two environments
- Improving the performance of the agents in your environments

## Requirements
- Complete the `...` parts in the skeleton code
- Train the PPO Agent with your code
- Contracting your source codes, evaluation pictures, game video, and presentation slides to zip file and submit to Blackboard

# HumanoidStandup-v4
Goal: Make the humanoid standup and then keep it standing

## Best Results
<p align="center">
  <img src="./humanoidstandup_test_video.gif" width="500" title="HumanoidStandup-v4 Result" alt="">
</p>

- MLP: state_dim -> 128 -> 64 -> action_dim
- Timesteps: 5M
- ent_coef: 0.0001
- rpo_coef: 0.5
- sym_action_coef: 0.02

### Robust Policy Optimization
[Robust Policy Optimization (CleanRL)](https://docs.cleanrl.dev/rl-algorithms/rpo/)
- Modified from PPO
- RPO leverages a method of perturbing the distribution representing actions
- Improved Performance compared to PPO


### Additional: Symmetric Action Loss
- Why do Humanoid use only one arm or leg? -> Use additional loss
- Symmetric Action Loss guided the use of both arms and legs and improve performance!


# HalfCheetah-v4
Goal: Make the cheetah run forward as fast as possible

## Best Results
<p align="center">
  <img src="./halfcheetah_test_video.gif" width="500" title="HumanoidStandup-v4 Result" alt="">
</p>

- MLP: state_dim -> 64 -> 64 -> action_dim
- Timesteps: 1M
- ent_coef: 0.5
- not use rpo (lower performance)