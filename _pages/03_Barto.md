---
layout: page
title: Barto
permalink: /barto/
---

### Graphs prepared from:
[Reinforcement Learning by Richard S. Sutton and Andrew G. Barto](http://webdocs.cs.ualberta.ca/~sutton/book/ebook/the-book.html)

***

### Epsilon-Greedy algorithm for choosing actions:
![Epsilon-Greedy: reward over time](/assets/Barto_2p2_EpsilonGreedy_AvgReward.png)
![Epsilon-Greedy: percent optimal action over time](/assets/Barto_2p2_EpsilonGreedy_PercentOptimalAction.png)

***

### Softmax algorithm for choosing actions:
Softmax probabilities are created using:
{% raw %}
$$\frac{e^{Q(a)/\tau}}{\sum_{b=1}^{n}e^{Q(b)/\tau}}$$
where $$\tau$$ is the computational tempetrure.
{% endraw %}
![Softmax: reward over time](/assets/Barto_2p3_softmax_reward.png)
![Softmax: percent optimal action over time](/assets/Barto_2p3_softmax_optimalAction.png)

***

### 10-arm bandit problem with **nonstationary** arm values (Barto 2.6)
Using constant $$\epsilon=0.1$$

The action-value method is being updated using $$Q_{k+1} = Q_{k} + \alpha [r_{k+1} - Q_{k}]$$. 

One bandit using $$\alpha=0.1$$ and the other bandit using $$\alpha=\frac{1}{k}$$ where k is the number of times an individual arm (or action) has been played.

![Average Reward over time](/assets/Barto_2-6_nonStationary_rewards.png)
![Percent Optimal action over time](/assets/Barto_2-6_nonStationary_optimalAction.png)



