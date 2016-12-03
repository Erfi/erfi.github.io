---
layout: headline_page
headline: Reinforcement Comparison (Barto 2.8)
permalink: /barto/barto_2p8/
img_h: 400
img_w: 500
---

{% raw %}

### Reinforcement Comparison

*Reinforcement Comparison* is different from *Epsilon-Greedy* and *Softmax* in the sense that it does not require an estimate of true values of each action. Instead it keeps a preference for each action and updates that preference using  reward from that action. Same intuition still applies here, we would like the actions foloowed by high rewards be more likely to recur and actions with low reward be less likely to recur. However since we are not keeping an estimate of each action we need another basis for evaluating the rewards as "high" or "low". In reinforcement learning a global average reward is stored and used as the basis for comparing the upcoming rewards. Value of the global average reward is then updated as new rewards are attained.

The action preferences are used to gain the acion selection probabilities according to a softmax relationship. If $$P_{t}(a)$$ is the action preference of action $$a$$ at time $$t$$ then the action probability of $$a$$ is defines as:

$$\pi_{t}(a)=Pr\{a_{t}=a\}=\frac{e^{P_{t}(a)}}{\sum^{n}_{b=1}e^{P_{t}(b)}}$$

$$\pi_{t}(a)$$ denotes the probability of selecting action $$a$$ at time $$t$$. After taking the action and recieveing the reward $$r$$ both preference for action $$a$$ and the global average reward $$\bar{r}$$ are updated as follows:

$$P_{t+1}(a_{t}) = P_{t}(a_{t}) + \beta[r_{t} - \bar{r}_{t}]$$

$$\bar{r}_{t+1} = \bar{r}_{t} + \alpha[r_{t} - \bar{r}_{t}]$$

$$\beta$$ is a positive stepsize parameter esuring that high rewards increases the probability of $$a_{t}$$ being reselected and low rewards decreses the said probability. 

$$\alpha$$ is the usual step size such that $$0< \alpha \leq 1$$. Using the constant $$\alpha$$ turns the average into an *exponential, recently-weighted average* for $$\bar{r}$$.

For implementation purposes, $$\bar{r_{0}}$$ can be set optimistically to a large number, in order to encourage exploration, or can be set according to prior knowledge. Action preferences can all be set to zero initiallly. The choice of constant $$\alpha$$ works well for reinforcement comparison beacuse reward distribution is changing over time in a nonstationary manner as action selection improves. As the result it makes the learning problem nonstationary eventhough the underlying problem itself is stationary. 

In order to highlight the effect of $$\alpha$$ and $$\beta$$ parameters I ahve kept one of them constant and varied the other one in the next four plots. 

{% endraw %}

<img src="/assets/Barto_RC_alpha_reward.png" class="img-thumbnail C-graph-center" alt="RC: Average Reward over time - alpha varying" width="{{ page.img_w }}" height="{{ page.img_h }}">

<img src="/assets/Barto_RC_alpha_optimal.png" class="img-thumbnail C-graph-center" alt="RC: Percent Optimal action over time - alpha varying" width="{{ page.img_w }}" height="{{ page.img_h }}">


The following two graphs were created similarly, by using three different values for $$\beta$$ while keeping the $$\alpha$$ the same.

<img src="/assets/Barto_RC_beta_reward.png" class="img-thumbnail C-graph-center" alt="RC: Average Reward over time - beta varying" width="{{ page.img_w }}" height="{{ page.img_h }}">

<img src="/assets/Barto_RC_beta_optimal.png" class="img-thumbnail C-graph-center" alt="RC: Percent Optimal action over time - beta varying" width="{{ page.img_w }}" height="{{ page.img_h }}">


Below are the two graphs comparing the performance of *Epsilon-Greedy* and *Reinforcement Comparison* methods for action selection. Notice that although *Reinforcement Comparison* seems to yeild higher reward in this case and with this parameter settings the overall performance of these action selection methods are highly dependant on the nature and dynamics of the problem itself.

<img src="/assets/avgReward_epsGreedy_vs_reinfComp.png" class="img-thumbnail C-graph-center" alt="Eps vs RC: Avg Reward" width="{{ page.img_w }}" height="{{ page.img_h }}">

<img src="/assets/optimal_epsGreedy_vs_reinfComp.png" class="img-thumbnail C-graph-center" alt="Eps vs RC: %optimal" width="{{ page.img_w }}" height="{{ page.img_h }}">

