# 🙌 Unveiling the Truth and Facilitating Change: Towards Agent-based Large-scale Social Movement Simulation
This is the repository for the preprint paper: [Unveiling the Truth and Facilitating Change: Towards Agent-based Large-scale Social Movement Simulation](https://arxiv.org/abs/2402.16333).  
The webpage can be visited at [https://xymou.github.io/social_simulation/](https://xymou.github.io/social_simulation/).

## Table of Contents
- [Abstract](#Abstract)
- [Methodology](#Methodology)
- [Dataset](#Dataset)
- [Citation](#Citation)

## Abstract
Social media has emerged as a cornerstone of social movements, wielding significant influence in driving societal change. Simulating the response of the public and forecasting the potential impact has become increasingly important. However, existing methods for simulating such phenomena encounter challenges concerning their efficacy and efficiency in capturing the behaviors of social movement participants. In this paper, we introduce a hybrid framework for social media user simulation, wherein users are categorized into two types. Core users are driven by Large Language Models, while numerous ordinary users are modeled by deductive agent-based models. We further construct a Twitter-like environment to replicate their response dynamics following trigger events. Subsequently, we develop a multi-faceted benchmark SoMoSiMu-Bench for evaluation and conduct comprehensive experiments across real-world datasets. Experimental results demonstrate the effectiveness and flexibility of our method.

## Methodology
![fm](./static/images/fm.png)
To handle the challenges in conducting large-scale online social movement simulation, this paper introduces a novel hybrid framework for social media user simulation.  
### RQ1: How to Simulate Large-scale Social Movement Participants?
User engagement in social networks often exhibits a Pareto distribution, where the bulk of content originates from a small fraction of individuals. Thus, those more active and influential such as opinion leaders should be modeled finely, while the silent majority can be controlled by simpler models. The overall framework is illustrated in Figure 2, where social media users are divided into **core users** and **ordinary users**. The two types of users are driven by different models, to address the cost and efficiency issues of using thousands of LLMs. Core users are empowered by large language models, while the ordinary users are driven by conventional agent-based models.

### RQ2: How to accurately simulate core users and replicate their behaviors within the community?
We build an agent architecture by empowering LLMs with the necessary capabilities for core user simulation. An overview of the agent's architecture is illustrated in the left part of Figure 2. Empowered by LLMs, the agent is equipped with a profile module, a memory module, and an action module.

### RQ3: How to Evaluate the Effectiveness of the Simulation?
To comprehensively evaluate the effectiveness of simulation, we consider both micro-level evaluation and macro-level evaluation, focusing on individual user alignment and systemic outcomes respectively.
- Micro Alignment Evaluation: simulate in single rounds by providing authentic contextual information to each core user agent and assess their decision-making, in terms of *stance*, *content* and *behavior*.
- Macro System Evaluation: quantify the attitude distribution in a complete multi-round simulation, considering both *static attitude distribution* and *time series* of the average attitude.

## Dataset


## Citation
Please consider citing this paper if you find this repository useful:
```bash
@article{mou2024unveiling,
      title={Unveiling the Truth and Facilitating Change: Towards Agent-based Large-scale Social Movement Simulation}, 
      author={Xinyi Mou and Zhongyu Wei and Xuanjing Huang},
      year={2024},
      journal = {arXiv preprint arXiv: 2402.16333},
}
```