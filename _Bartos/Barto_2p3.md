---
layout: headline_page
headline: Softmax Action Selection (Barto 2.3)
permalink: /barto/barto_2p3/
img_h: 300
img_w: 400
---

{% raw %}

### Softmax Action Selection

In last section, (Barto 2.2), Epsilon-Greedy action selection was introduced as a method for balancing exploration and eploitation. In this section we will focus on another method called **Softmax Action Selection**.
Although simple to implement, Epsilon-Greedy will select an action at random with equal probability among all the actions. This means that the probability of selecting the best and the worst action is the same which may result in unsatisfactory results. 

Softmax action selection tries to address this issue by changing the probability of selcting an action based on the action's estimated value. The greedy action will still have the highest probability. All other actions are then ranked and weighted as a funciton of their estimated values.
One of the common softmax methods is the Gibbs, or Boltzmann, distribution. The probability of selecting action $$a$$ at time $$t$$ is given as:

$$\frac{e^{Q(a)/\tau}}{\sum_{b=1}^{n}e^{Q(b)/\tau}}$$

where $$\tau$$ is the computational tempetrure. Temperature here functions similarly to [simulated annealing](https://en.wikipedia.org/wiki/Simulated_annealing). as $$\tau \to \infty$$ the probabilities of choosing different actions become the same and equal to $$\frac{1}{n}$$, where $$n$$ is number of availible actions. On the other hand in the limit as $$\tau \to 0$$ the softmax selection becomes the same as greedy action selection.

The graphs below show the performance of Softmax method using Gibbs/Botzmann distribution under different temperatures. We can see that in high temperatures ($$\tau = 10$$) the action selection seems random whereas at very low temperatures ($$\tau=0.01$$) the action selection becomes similar to greedy action selection.
{% endraw %}

***

#### [View Code](https://github.com/Erfi/barto/blob/master/bandit.py)

***

<img src="/assets/Barto_2p3_softmax_reward.png" class="img-thumbnail C-graph-center" alt="Softmax: reward over time" width="{{ page.img_w }}" height="{{ page.img_h }}">

<img src="/assets/Barto_2p3_softmax_optimalAction.png" class="img-thumbnail C-graph-center" alt="Softmax: percent optimal action over time" width="{{ page.img_w }}" height="{{ page.img_h }}">