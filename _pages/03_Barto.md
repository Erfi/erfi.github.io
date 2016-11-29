---
layout: page
title: Barto
permalink: /barto/
img_h: 300
img_w: 400
---
<div class="row" markdown="1">
<div class="col-md-12 col-sm-12" markdown="1">
### Graphs prepared from:
[Reinforcement Learning by Richard S. Sutton and Andrew G. Barto](http://webdocs.cs.ualberta.ca/~sutton/book/ebook/the-book.html)

***

### Epsilon-Greedy algorithm for choosing actions:
<img src="/assets/Barto_2p2_EpsilonGreedy_AvgReward.png" class="img-thumbnail C-graph-center" alt="Epsilon-Greedy: reward over time" width="{{ page.img_w }}" height="{{ page.img_h }}">

<img src="/assets/Barto_2p2_EpsilonGreedy_PercentOptimalAction.png" class="img-thumbnail C-graph-center" alt="Epsilon-Greedy: percent optimal action over time" width="{{ page.img_w }}" height="{{ page.img_h }}">

***

### Softmax algorithm for choosing actions:
Softmax probabilities are created using:
{% raw %}
$$\frac{e^{Q(a)/\tau}}{\sum_{b=1}^{n}e^{Q(b)/\tau}}$$
where $$\tau$$ is the computational tempetrure.
{% endraw %}

<img src="/assets/Barto_2p3_softmax_reward.png" class="img-thumbnail C-graph-center" alt="Softmax: reward over time" width="{{ page.img_w }}" height="{{ page.img_h }}">

<img src="/assets/Barto_2p3_softmax_optimalAction.png" class="img-thumbnail C-graph-center" alt="Softmax: percent optimal action over time" width="{{ page.img_w }}" height="{{ page.img_h }}">

***

### 10-arm bandit problem with **nonstationary** arm values (Barto 2.6)
Using constant $$\epsilon=0.1$$

The action-value method is being updated using $$Q_{k+1} = Q_{k} + \alpha [r_{k+1} - Q_{k}]$$. 

One bandit using $$\alpha=0.1$$ and the other bandit using $$\alpha=\frac{1}{k+1}$$ where k is the number of times an individual arm (or action) has been played.

<img src="/assets/Barto_2-6_nonStationary_rewards.png" class="img-thumbnail C-graph-center" alt="Average Reward over time" width="{{ page.img_w }}" height="{{ page.img_h }}">

<img src="/assets/Barto_2-6_nonStationary_optimalAction.png" class="img-thumbnail C-graph-center" alt="Percent Optimal action over time" width="{{ page.img_w }}" height="{{ page.img_h }}">

***

### 10-arm bandit problem using **Reinforcement Comparison** method (Barto 2.8)
Varying the values of $$\alpha$$ and $$\beta$$ parameters which are used in updating the action preferences and global average reward.

The following two graphs were created by using three different values of $$\alpha$$ while keeping the $$\beta$$ the same.

<img src="/assets/Barto_RC_alpha_reward.png" class="img-thumbnail C-graph-center" alt="RC: Average Reward over time - alpha varying" width="{{ page.img_w }}" height="{{ page.img_h }}">

<img src="/assets/Barto_RC_alpha_optimal.png" class="img-thumbnail C-graph-center" alt="RC: Percent Optimal action over time - alpha varying" width="{{ page.img_w }}" height="{{ page.img_h }}">


The following two graphs were created similarly, by using three different values for $$\beta$$ while keeping the $$\alpha$$ the same.

<img src="/assets/Barto_RC_beta_reward.png" class="img-thumbnail C-graph-center" alt="RC: Average Reward over time - beta varying" width="{{ page.img_w }}" height="{{ page.img_h }}">

<img src="/assets/Barto_RC_beta_optimal.png" class="img-thumbnail C-graph-center" alt="RC: Percent Optimal action over time - beta varying" width="{{ page.img_w }}" height="{{ page.img_h }}">


Below are the two graphs comparing the performance of Epsilon-Greedy and Reinforcement Comparison methods.

<img src="/assets/avgReward_epsGreedy_vs_reinfComp.png" class="img-thumbnail C-graph-center" alt="Eps vs RC: Avg Reward" width="{{ page.img_w }}" height="{{ page.img_h }}">

<img src="/assets/optimal_epsGreedy_vs_reinfComp.png" class="img-thumbnail C-graph-center" alt="Eps vs RC: %optimal" width="{{ page.img_w }}" height="{{ page.img_h }}">


</div>
</div>

