---
layout: headline_page
headline: Tracking a Nonstationary Probelm (Barto 2.6)
permalink: /barto/barto_2p6/
img_h: 300
img_w: 400
---

{% raw %}

### Tracking Nonstationary Problems

Averaging methods discussed earlier are useful for stationary problems meaning that, in the case of n-arm bandit problem, the actual values of each arm does not change over time. If these values change over the time of the simulation then it would make sense to weight the more recent rewards more heavily than long past ones otherwise our estimation of the action values will not be able to keep up with the changes in the actual action values.

One popular way of addressing nonstationary problems is to change out averaging method to what is refered to as *exponential, recently-weighted average*. Implementing such a change is pretty straight forward.
Notice our updating rule:

$$Q_{k+1} = Q_{k} + \alpha [r_{k+1} - Q_{k}]$$ 

**For stationary problems** we use $$\alpha=\frac{1}{k}$$ which will result in sample averaging. Where k is the number of times an individual arm (or action) has been played.

**For nonstationary problems** we can use a constant $$0 < \alpha \leq 1$$ which will result in exponential, recently-weighted average.

Below illustrates the differentce in performace of using constant vs. varying $$\alpha$$ for a nonstationary problem. As we can see the constant $$\alpha$$ shows better tracking. Here we have used the Epsilon-Greedy with $$\epsilon=0.1$$, constant $$\alpha=0.1$$ and varying $$\alpha=\frac{1}{k}$$.

***

#### [View Code](https://github.com/Erfi/barto/blob/master/bandit2.py)

***

{% endraw %}
<img src="/assets/Barto_2-6_nonStationary_rewards.png" class="img-thumbnail C-graph-center" alt="Average Reward over time" width="{{ page.img_w }}" height="{{ page.img_h }}">

<img src="/assets/Barto_2-6_nonStationary_optimalAction.png" class="img-thumbnail C-graph-center" alt="Percent Optimal action over time" width="{{ page.img_w }}" height="{{ page.img_h }}">