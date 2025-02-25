# Key Deep Reinforcement Learning Research Papers & Algorithms
List of papers in RL that are worth reading. This is a brief, and curated list from already existing list by [Spinning-Up](https://spinningup.openai.com/en/latest/spinningup/keypapers.html) to reduce their work to (in my opinion) most important top-50 papers. Each week, I will be reading at least one of these papers, and share my insights on the same. I will also attempt to demonstrate that algorithm/research, depending on the nature of the work. This will help me breakdown complex topics into smaller bites for easier understanding of self, as well as the readers of these *blog-ish* tutorials.

## Foundational Reinforcement Learning Algorithms

1. **[Playing Atari with Deep Reinforcement Learning](https://arxiv.org/abs/1312.5602)**  
   *Mnih et al., 2013.*  
   *Algorithm:* DQN.

   **Challenge?** The paper tackles the long-standing challenge of enabling agents to learn control policies directly from high-dimensional sensory inputs (here, vision), using RL. Previous RL relied heavily on hand-crafted features, limiting its applicability to complex real-world scenarios.

   **Proposed Approach?** A system using a CNN trained with a variant of Q-learning. The network takes raw pixel data as input and outputs a value function estimating future rewards.

   **Key results?** Outperformed previous methods on six out of the seven games. It also surpassed human expert performance on three of them.

**(BONUS) DeepSeekMath : \<TODO-Add content here\>**

3. **[Deep Recurrent Q-Learning for Partially Observable MDPs](https://arxiv.org/abs/1507.06527)**  
   *Hausknecht and Stone, 2015.*  
   *Algorithm:* Deep Recurrent Q-Learning.

   **Challenge?** Standard Deep Q-Networks (DQNs) struggle with Partially Observable Markov Decision Processes (POMDPs) because they rely on complete state information (the game screen) at each decision point. DQNs use a limited history (typically 4 frames) and cannot remember events further in the past, making them unsuitable for games where long-term memory is crucial.

   **Proposed Approach?** introduce Deep Recurrent Q-Network (DRQN) which incorporates an LSTM (Long Short-Term Memory) layer to integrate information over time and address partial observability.

   **Key results?** DRQN handles noisy observations in POMDPs better by using an LSTM to integrate information through time. DRQN can perform well even when receiving only a single frame at each timestep. It provides a strong alternative to using frame stacking in regular DQN networks. While DRQN shows better generalization between MDPs and POMDPs, it does not show a systematic performance improvement versus regular DQNs.

4. **[Diffusion Policy: Visuomotor Policy Learning via Action Diffusion](https://diffusion-policy.cs.columbia.edu/)**
   *Cheng Chi, Siyuan Feng, Yilun Du, Zhenjia Xu, Eric Cousineau, Benjamin Burchfiel, Shuran Song, 2024.*
   *Algorithm: Diffusion Policy*

   **Challenge?** Traditional visuomotor policy learning approaches, such as behavior cloning (BC) and reinforcement learning (RL), struggle with multimodal action distributions, compounding errors, and unstable training dynamics. Standard BC methods assume a unimodal action distribution, leading to suboptimal performance in complex tasks requiring diverse strategies.  
  
   **Proposed Approach?** Introduce *Diffusion Policy*, a novel approach that models the action distribution as a conditional denoising diffusion process. This technique allows for multimodal action prediction by learning to iteratively refine noisy action samples into meaningful control outputs. The method builds upon the diffusion generative model framework, ensuring stable training and better exploration of diverse action trajectories.  
  
   **Key Results?** Diffusion Policy outperforms standard BC baselines in robot manipulation tasks, demonstrating superior generalization and robustness to out-of-distribution states. The approach effectively captures multimodal behavior, allowing agents to adapt to different strategies rather than committing to a single deterministic action. The paper shows that Diffusion Policy achieves state-of-the-art performance on several real-world robot control benchmarks.

   Detailed breakdown is presented on YouTube at [Diffusion Policy with MaiaV Robotics!](https://www.youtube.com/watch?v=CtJDROYBmSs)

   External resources that I found insightful:
   - [Diffusion Policy Explained by Fotios (Fotis) Lygerakis](https://medium.com/@ligerfotis/diffusion-policy-explained-14a3075ba26c#:~:text=By%20progressively%20adding%20and%20then%20removing%20noise,just%20dominant%20modes%20from%20the%20collected%20dataset.&text=So%2C%20if%20we%20train%20a%20Diffusion%20Model,to%20learn%20how%20to%20remove%20the%20noise.)
   - [What are Diffusion Models? by Lilian Weng](https://lilianweng.github.io/posts/2021-07-11-diffusion-models/)

6. **[Dueling Network Architectures for Deep Reinforcement Learning](https://arxiv.org/abs/1511.06581)**  
   *Wang et al., 2015.*  
   *Algorithm:* Dueling DQN.  

7. **[Deep Reinforcement Learning with Double Q-learning](https://arxiv.org/abs/1509.06461)**  
   *Van Hasselt et al., 2015.*  
   *Algorithm:* Double DQN.

8. **[Prioritized Experience Replay](https://arxiv.org/abs/1511.05952)**  
   *Schaul et al., 2015.*  
   *Algorithm:* Prioritized Experience Replay (PER).

9. **[Rainbow: Combining Improvements in Deep Reinforcement Learning](https://arxiv.org/abs/1710.02298)**  
   *Hessel et al., 2017.*  
   *Algorithm:* Rainbow DQN.

10. **[Asynchronous Methods for Deep Reinforcement Learning](https://arxiv.org/abs/1602.01783)**  
   *Mnih et al., 2016.*  
   *Algorithm:* A3C.

## Policy Optimization and Actor-Critic Methods

8. **[Trust Region Policy Optimization](https://arxiv.org/abs/1502.05477)**  
   *Schulman et al., 2015.*  
   *Algorithm:* TRPO.

9. **[High-Dimensional Continuous Control Using Generalized Advantage Estimation](https://arxiv.org/abs/1506.02438)**  
   *Schulman et al., 2015.*  
   *Algorithm:* GAE.  

10. **[Proximal Policy Optimization Algorithms](https://arxiv.org/abs/1707.06347)**  
    *Schulman et al., 2017.*  
    *Algorithm:* PPO-Clip, PPO-Penalty.  

11. **[Soft Actor-Critic: Off-Policy Maximum Entropy Deep Reinforcement Learning with a Stochastic Actor](https://arxiv.org/abs/1801.01290)**  
    *Haarnoja et al., 2018.*  
    *Algorithm:* SAC.  

12. **[Deterministic Policy Gradient Algorithms](https://arxiv.org/abs/1509.02971)**  
    *Silver et al., 2014.*  
    *Algorithm:* DPG.  

13. **[Continuous Control with Deep Reinforcement Learning](https://arxiv.org/abs/1509.02971)**  
    *Lillicrap et al., 2015.*  
    *Algorithm:* DDPG.  

14. **[Addressing Function Approximation Error in Actor-Critic Methods](https://arxiv.org/abs/1802.09477)**  
    *Fujimoto et al., 2018.*  
    *Algorithm:* TD3.  

## Distributional Reinforcement Learning

15. **[A Distributional Perspective on Reinforcement Learning](https://arxiv.org/abs/1707.06887)**  
    *Bellemare et al., 2017.*  
    *Algorithm:* C51.

16. **[Distributional Reinforcement Learning with Quantile Regression](https://arxiv.org/abs/1710.10044)**  
    *Dabney et al., 2017.*  
    *Algorithm:* QR-DQN.  

17. **[Implicit Quantile Networks for Distributional Reinforcement Learning](https://arxiv.org/abs/1806.06923)**  
    *Dabney et al., 2018.*  
    *Algorithm:* IQN.

## Hybrid and Alternative Approaches

18. **[Q-Prop: Sample-Efficient Policy Gradient with An Off-Policy Critic](https://arxiv.org/abs/1611.02247)**  
    *Gu et al., 2016.*  
    *Algorithm:* Q-Prop.  

19. **[Bridging the Gap Between Value and Policy Based Reinforcement Learning](https://arxiv.org/abs/1702.08892)**  
    *Nachum et al., 2017.*  
    *Algorithm:* PCL.  

20. **[Combining Policy Gradient and Q-learning](https://arxiv.org/abs/1611.01626)**  
    *O'Donoghue et al., 2016.*  
    *Algorithm:* PGQL.

21. **[Evolution Strategies as a Scalable Alternative to Reinforcement Learning](https://arxiv.org/abs/1703.03864)**  
    *Salimans et al., 2017.*  
    *Algorithm:* Evolution Strategies (ES).  

## Exploration and Intrinsic Motivation

22. **[VIME: Variational Information Maximizing Exploration](https://arxiv.org/abs/1605.09674)**  
    *Houthooft et al., 2016.*  
    *Algorithm:* VIME.

23. **[Unifying Count-Based Exploration and Intrinsic Motivation](https://arxiv.org/abs/1606.01868)**  
    *Bellemare et al., 2016.*  
    *Algorithm:* CTS-based Pseudocounts.

24. **[Curiosity-driven Exploration by Self-supervised Prediction](https://arxiv.org/abs/1705.05363)**  
    *Pathak et al., 2017.*  
    *Algorithm:* Intrinsic Curiosity Module (ICM).  

25. **[Exploration by Random Network Distillation](https://arxiv.org/abs/1810.12894)**  
    *Burda et al., 2018.*  
    *Algorithm:* RND.

26. **[Hindsight Experience Replay](https://arxiv.org/abs/1707.01495)**  
    *Andrychowicz et al., 2017.*  
    *Algorithm:* HER.

## Episodic Control and Memory-Based Methods

27. **[Model-Free Episodic Control](https://arxiv.org/abs/1606.04460)**  
    *Blundell et al., 2016.*  
    *Algorithm:* MFEC.

28. **[Neural Episodic Control](https://arxiv.org/abs/1703.01988)**  
    *Pritzel et al., 2017.*  
    *Algorithm:* NEC.

## Game Applications and Breakthrough Systems

29. **[Neural Architecture Search with Reinforcement Learning](https://arxiv.org/abs/1611.01578)**  
    *Zoph and Le, 2016.*  
    *Algorithm:* NAS-RL.

30. **[AlphaGo Zero: Mastering the Game of Go without Human Knowledge](https://www.nature.com/articles/nature24270)**  
    *Silver et al., 2017.*  
    *Algorithm:* AlphaGo Zero.

31. **[Mastering Chess and Shogi by Self-Play with a General Reinforcement Learning Algorithm](https://arxiv.org/abs/1712.01815)**  
    *Silver et al., 2018.*  
    *Algorithm:* AlphaZero.

32. **[Mastering Atari, Go, Chess, and Shogi by Planning with a Learned Model](https://arxiv.org/abs/1911.08265)**  
    *Schrittwieser et al., 2019.*  
    *Algorithm:* MuZero.

##  Model-Based Reinforcement Learning

33. **[Neural Network Dynamics for Model-Based Deep Reinforcement Learning with Model-Free Fine-Tuning](https://arxiv.org/abs/1708.02596)**  
    *Nagabandi et al., 2018.*  
    *Algorithm:* Model-Based Dyna.

34. **[World Models](https://arxiv.org/abs/1803.10122)**  
    *Ha and Schmidhuber, 2018.*  
    *Algorithm:* World Models.

35. **[Imagination-Augmented Agents for Deep Reinforcement Learning](https://arxiv.org/abs/1707.06203)**  
    *Racanière et al., 2017.*  
    *Algorithm:* Imagination-Augmented Agents (I2A).

36. **[Learning to Think—Model-Based Control](https://arxiv.org/abs/1707.06203)**  
    *Weber et al., 2017.*  
    *Algorithm:* Value Prediction Networks (VPN).

## Hierarchical Reinforcement Learning and Temporal Abstractions

37. **[FeUdal Networks for Hierarchical Reinforcement Learning](https://arxiv.org/abs/1703.01161)**  
    *Vezhnevets et al., 2017.*  
    *Algorithm:* Feudal Networks.
    
38. **[Hierarchical Reinforcement Learning with Timed Subgoals](https://arxiv.org/abs/1604.06057)**  
    *Kulkarni et al., 2016.*  
    *Algorithm:* Hierarchical-DQN (h-DQN).

39. **[Learning with Hierarchical Attention](https://arxiv.org/abs/1805.08296)**  
    *Nachum et al., 2018.*  
    *Algorithm:* HIRO.

40. **[Options Framework for Hierarchical Reinforcement Learning](https://www.jair.org/index.php/jair/article/view/1031)**  
    *Sutton et al., 1999.*  
    *Algorithm:* Options.

41. **[Playing with Options](https://arxiv.org/abs/1609.05140)**  
    *Bacon et al., 2017.*  
    *Algorithm:* Option-Critic.

42. **[Hierarchical Deep Reinforcement Learning: Integrating Temporal Abstraction and Intrinsic Motivation](https://arxiv.org/abs/1604.06057)**  
    *Kulkarni et al., 2016.*  
    *Algorithm:* h-DQN with Intrinsic Motivation.

43. **[Intrinsic Motivation for Hierarchical Reinforcement Learning](https://arxiv.org/abs/1906.04009)**  
    *Nachum et al., 2019.*  
    *Algorithm:* Multi-level HIRO.

## Offline Reinforcement Learning

44. **[Batch Constrained Q-Learning](https://arxiv.org/abs/1812.02900)**  
    *Fujimoto et al., 2019.*  
    *Algorithm:* BCQ.

45. **[Conservative Q-Learning for Offline Reinforcement Learning](https://arxiv.org/abs/2006.04779)**  
    *Kumar et al., 2020.*  
    *Algorithm:* CQL.

46. **[Behavior Regularized Actor Critic](https://arxiv.org/abs/1911.11361)**  
    *Wu et al., 2019.*  
    *Algorithm:* BRAC.

47. **[Stabilizing Off-Policy Q-Learning via Bootstrapping Error Reduction](https://arxiv.org/abs/2003.05990)**  
    *Kumar et al., 2020.*  
    *Algorithm:* Bootstrapped Q-Learning.

48. **[Offline Meta-Reinforcement Learning with Advantage Weighting](https://arxiv.org/abs/2006.09359)**  
    *Fu et al., 2020.*  
    *Algorithm:* AWAC.

## Safe and Constrained Reinforcement Learning

49. **[Safe Exploration in Reinforcement Learning](https://arxiv.org/abs/1705.10710)**  
    *Berkenkamp et al., 2017.*  
    *Algorithm:* SafeRL.

50. **[Efficient Exploration through Bayesian Optimization for RL](https://arxiv.org/abs/1012.2599)**  
    *Srinivas et al., 2010.*  
    *Algorithm:* BO-RL.
