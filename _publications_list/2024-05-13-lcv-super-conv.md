---
title: "Longitudinal Control Volumes: A Novel Centralized Estimation and Control Framework for Distributed Multi-Agent Sorting Systems"
authors: "James Maier, Prasanna Sriganesh and Matthew Travers"
venue: "2024 IEEE International Conference on Robotics and Automation (ICRA)"
date: 2024-05-13
paper_link: "https://arxiv.org/abs/2402.02232" 
# external_url: ""
# internal_url: "" 
# github: ""
video: "https://www.youtube.com/watch?v=zHBTYLz28O0"
bibtex: |
  @inproceedings{maier2024longitudinal,
    title={Longitudinal Control Volumes: A Novel Centralized Estimation and Control Framework for Distributed Multi-Agent Sorting System},
    author={Maier, James and Sriganesh, Prasanna and Travers, Matthew},
    booktitle={2024 IEEE International Conference on Robotics and Automation (ICRA)},
    pages={4420--44279},
    year={2024},
    organization={IEEE},
  }
image: /img/publications/superconv_icra.jpg
tags:
 - Bayesian Inference
 - Model Predictive Control

---

Centralized control of a multi-agent system improves upon distributed control especially when multiple agents share a common task e.g., sorting different materials in a recycling facility. Traditionally, each agent in a sorting facility is tuned individually which leads to suboptimal performance if one agent is less efficient than the others. Centralized control overcomes this bottleneck by leveraging global system state information, but it can be computationally expensive. In this work, we propose a novel framework called Longitudinal Control Volumes (LCV) to model the flow of material in a recycling facility. We then employ a Kalman Filter that incorporates local measurements of materials into a global estimation of the material flow in the system. We utilize a model predictive control algorithm that optimizes the rate of material flow using the global state estimate in real-time. We show that our proposed framework outperforms distributed control methods by 40-100% in simulation and physical experiments.