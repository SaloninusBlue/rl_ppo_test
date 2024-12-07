## Project - MountainCarContinuous with PPO (vectorized environments)

###  Environment   
Usually, solving the environment require an average total reward of over the threshold over 100 consecutive episodes.      
However, in this case the solution is achieved very fastly: in __21 episodes__ in __1 minute__ !  This is due to the fact    
that there are 16 processes in use in this PPO implementation notebook. We can think that the real number of episodes    
is __21x16 = 336__.   

![](images/4_diagrams_0.7.png)

We use PPO with vectorized environments, the basic paper: [Proximal Policy Optimization Algorithms](https://arxiv.org/abs/1707.06347).    
**Vectorized Environments** (in our case there are  16 environments) is a method that means that the agent is trained in     
16 environments simultaneously.

### Training score

![](images/plot_MountainCarCont_16proc_21epis_score152.png)
 

### MountainCar, different models

* [MountainCar, Q-learning](https://github.com/Rafael1s/Deep-Reinforcement-Learning-Algorithms/tree/master/MountainCar-Q-Learning)
* [MountainCar, DQN](https://github.com/Rafael1s/Deep-Reinforcement-Learning-Algorithms/tree/master/MountainCar-DQN)
* [MountainCarContinuous, TD3](https://github.com/Rafael1s/Deep-Reinforcement-Learning-Algorithms/tree/master/MountainCarContinuous-TD3) 

### Other PPO projects

  * [BipedalWalker](https://github.com/Rafael1s/Deep-Reinforcement-Learning-Algorithms/tree/master//BipedalWalker-PPO-VectorizedEnv),   16 parallel agents 
  * [CarRacing](https://github.com/Rafael1s/Deep-Reinforcement-Learning-Algorithms/tree/master/CarRacing-From-Pixels-PPO),  Single agent, Learning from pixels   
  * [C r a w l e r  ](https://github.com/Rafael1s/Deep-Reinforcement-Learning-Algorithms/tree/master/Project-2_Continuous-Control-Crawler-PPO), 12 parallel agents   
  * [Pong](https://github.com/Rafael1s/Deep-Reinforcement-Learning-Algorithms/tree/master/Pong-Policy-Gradient-PPO), 8 parallel agents

### References
* [Proximal Policy Optimization](https://openai.com/blog/openai-baselines-ppo/).   
"_PPO has become the default reinforcement learning algorithm at OpenAI._"   

* [Vectorized Environments](https://stable-baselines.readthedocs.io/en/master/guide/vec_envs.html)  
"_Vectorized Environments are a method for stacking multiple independent environments into a single environment. 
Instead of training an RL agent on 1 environment per step, it allows us to train it on n environments per step._"

