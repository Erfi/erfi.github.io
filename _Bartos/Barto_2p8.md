---
layout: headline_page
headline: Reinforcement Comparison (Barto 2.8)
permalink: /barto/barto_2p8/
img_h: 300
img_w: 400
---

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