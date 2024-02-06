# OpenPaL: Building Open-Ended Embodied Agent via Language-Policy Bidirectional Adaptation

Building embodied agents on integrating Large Language Models (LLMs) and Reinforcement Learning (RL) have revolutionized human-AI interaction: researchers can now leverage language instructions to plan decision-making for open-ended tasks. However, existing research faces challenges in meeting the requirement of open-endedness. They typically either train LLM/RL models to adapt to a fixed counterpart, limiting exploration of novel skills and hindering the efficacy of human-AI interaction. To this end, we present OpenPAL, a co-training framework comprising two stages: (1) fine-tuning a pre-trained LLM to translate human instructions into goals for planning, and goal-conditioned training a policy for decision-making; (2) co-training to align the LLM and policy, achieving instruction open-endedness. We conducted experiments using Contra, an open-ended FPS game, demonstrating that an agent trained with OpenPAL not only comprehends arbitrary instructions but also exhibits efficient execution. These results suggest that OpenPAL holds the potential to construct open-ended embodied agents in practical scenarios.


## Environment & Demonstration

<p float="left">
<img width="33%" src="https://github.com/opendilab/OpenPaL/assets/18256149/f9c1d00a-62c1-4530-a0fc-26b9c1ecc330">
<img width="33%" src="https://github.com/opendilab/OpenPaL/assets/18256149/783c1e03-f7d6-4d89-8288-e3fae636ecaf">
<img width="33%" src="https://github.com/opendilab/OpenPaL/assets/18256149/20cec53a-3840-4805-99a8-7fb330f0c00b">
</p>

<p class="text-justify">Contra seamlessly merges the last-man-standing gameplay dynamics with the survival, exploration, and scavenging elements inherent in first-person shooting games. The game unfolds with multiple hostile teams, necessitating players to collaborate with teammates, withstand adversaries, and strive to outlast others in the ever-changing safe-zone. An agent in Contra mandates a sequential acquisition of skills, starting from fundamental abilities like walking, jumping, running, and item collection. As the learning proceeds, an agent must master more intricate skills such as evading enemy projectiles and coordinating tactics with teammates. This characteristic defines an open-ended learning process where the agent continually explores the game environment to refine mastered skills and acquire new ones.</p>


## Architecture

Our success stems from the introduction of OpenPAL, a co-training framework that bi-directionally aligns the language model and the policy. In conventional language-centered human-AI architectures, there is a preference for one-sided adaptation, i.e., training the language model to adapt to the policy model or vice versa. However, this approach has limitations for open-ended learning, as the learning model tends to overfit to the fixed one, constrained by a bounded oracle (the fixed one). Particularly in specific environments requiring specialized knowledge, it becomes essential for a language-centered paradigm to acquire novel knowledge through interaction and exploration with the policy to achieve open-endedness. Nevertheless, as the policy will be optimized to learn novel knowledge, it deviates from the range of the Language Model's comprehension, and vice versa. To address this challenge, we propose OpenPAL.

![new_frame](https://github.com/opendilab/OpenPaL/assets/18256149/50a62955-04c9-445f-bd85-699518206bb9)


## Citing OpenPaL

Read our [paper](/paper.pdf) for more details.

```bibtex
@misc{pjopenpal23,
    author = {Shaopeng Zhai and Jie Wang and Tianyi Zhang and Fuxian Huang and Qi Zhang and Ming Zhou and Jing Hou and Yu Qiao and Yu Liu},
    title = {Building Open-Ended Embodied Agent via Language-Policy Bidirectional Adaptation},
    url ={https://github.com/opendilab/OpenPaL/},
    year = {2023},
    month = {12},
}
```
