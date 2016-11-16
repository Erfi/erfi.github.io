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


