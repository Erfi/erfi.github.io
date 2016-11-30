---
layout: headline_page
headline: Action-Value Methods (Barto 2.2)
permalink: /barto/barto_2p2/
img_h: 300
img_w: 400
---
<div class="row" markdown="1">
<div class="col-md-12 col-sm-12" markdown="1">

{% raw %}
### Action-Value methods:
Action-Value methods try to estimate the value of each action and then use those estimates to select the next action. The estimate value for each action $$a$$ at time $$t$$, $$Q_{t}(a)$$, can be calculated by averaging the rewards recieved from taking each action as written below:

$$Q_{t}(a) = \frac{r_{1} + r_{2} + ... + r_{k_{a}}}{k_{a}}$$

Here $$k_{a}$$ is the number of times action $$a$$ is selected prior to time $$t$$.

As $$t\to\infty$$ then $$Q_{t}(a) \to Q^{*}_{t}(a)$$ which is the actual value of action $$a$$.



### Epsilon-Greedy action selection:
One way to address the *Exploration vs. Exploitaion* problem is to use Epsilon-Greedy action selection. *Epsilon* refers to the percentage or portion of times that a random action is selected instead of the *Greedy* action, which is the action with highest estimated value. 
The main idea is that allowing random actions a small percentage of the time will yeild to higher reward eventually.

The graphs below are using *Epsilon-Greedy* action selection in order to select the actions for a [10-arm bandit problem](https://en.wikipedia.org/wiki/Multi-armed_bandit). These graphs are similar to graphs in the book but they are extended to 10000 plays in order to illustrate the fact that average reward using $$\epsilon = 0.01$$ eventually passes the average reward using $$\epsilon = 0.1$$. The reason is that with smaller $$\epsilon$$ we are still exploring (although at a slower rate) which will allow us to find better actions over time, however, we are also using the action with the highest estimate value more often. 

{% endraw %}
<img src="/assets/Barto_2p2_EpsilonGreedy_AvgReward.png" class="img-thumbnail C-graph-center" alt="Epsilon-Greedy: reward over time" width="{{ page.img_w }}" height="{{ page.img_h }}">

<img src="/assets/Barto_2p2_EpsilonGreedy_PercentOptimalAction.png" class="img-thumbnail C-graph-center" alt="Epsilon-Greedy: percent optimal action over time" width="{{ page.img_w }}" height="{{ page.img_h }}">

</div>
</div>