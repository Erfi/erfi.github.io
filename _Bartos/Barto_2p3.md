---
layout: headline_page
headline: Softmax Action Selection (Barto 2.3)
permalink: /barto/barto_2p3/
img_h: 300
img_w: 400
---

Softmax probabilities are created using:
{% raw %}
$$\frac{e^{Q(a)/\tau}}{\sum_{b=1}^{n}e^{Q(b)/\tau}}$$
where $$\tau$$ is the computational tempetrure.
{% endraw %}

<img src="/assets/Barto_2p3_softmax_reward.png" class="img-thumbnail C-graph-center" alt="Softmax: reward over time" width="{{ page.img_w }}" height="{{ page.img_h }}">

<img src="/assets/Barto_2p3_softmax_optimalAction.png" class="img-thumbnail C-graph-center" alt="Softmax: percent optimal action over time" width="{{ page.img_w }}" height="{{ page.img_h }}">