---
layout: headline_page
headline: Tracking a Nonstationary Probelm (Barto 2.6)
permalink: /barto/barto_2p6/
img_h: 300
img_w: 400
---

Using constant $$\epsilon=0.1$$

The action-value method is being updated using $$Q_{k+1} = Q_{k} + \alpha [r_{k+1} - Q_{k}]$$. 

One bandit using $$\alpha=0.1$$ and the other bandit using $$\alpha=\frac{1}{k+1}$$ where k is the number of times an individual arm (or action) has been played.

<img src="/assets/Barto_2-6_nonStationary_rewards.png" class="img-thumbnail C-graph-center" alt="Average Reward over time" width="{{ page.img_w }}" height="{{ page.img_h }}">

<img src="/assets/Barto_2-6_nonStationary_optimalAction.png" class="img-thumbnail C-graph-center" alt="Percent Optimal action over time" width="{{ page.img_w }}" height="{{ page.img_h }}">