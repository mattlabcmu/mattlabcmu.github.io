---
title: "Action-Informed Estimation and Planning: Clearing Clutter on Staircases via Quadrupedal Pedipulation"
authors: "Prasanna Sriganesh, Barath Satheeshkumar, Anushree Sabnis and Matthew Travers"
# venue: ""
date: 2025-09-25
paper_link: "https://arxiv.org/abs/2509.20516" 
external_url: "https://www.prassi.me/clearing-clutter-on-stairs" 
video: "https://www.youtube.com/watch?v=CTss0FFHwNU"
bibtex: |
  @article{sriganesh2025actioninformed,
    title={Action-Informed Estimation and Planning: Clearing Clutter on Staircases via Quadrupedal Pedipulation},
    author={Prasanna Sriganesh and Barath Satheeshkumar and Anushree Sabnis and Matthew Travers},
    journal={arXiv preprint arXiv:2509.20516},
    year={2025},
  }
image: /img/publications/action_informed_planning.jpg
tags:
  - Robot Perception
  - Robot Learning

---

For robots to operate autonomously in densely cluttered environments, they must reason about and potentially physically interact with obstacles to clear a path. Safely clearing a path on challenging terrain, such as a cluttered staircase, requires controlled interaction. For example, a quadrupedal robot that pushes objects out of the way with one leg while maintaining a stable stance with its three other legs. However, tightly coupled physical actions, such as one-legged pushing, create new constraints on the system that can be difficult to predict at design time. In this work, we present a new method that addresses one such constraint, wherein the object being pushed by a quadrupedal robot with one of its legs becomes occluded from the robot's sensors during manipulation. To address this challenge, we present a tightly coupled perception-action framework that enables the robot to perceive clutter, reason about feasible push paths, and execute the clearing maneuver. Our core contribution is an interaction-aware state estimation loop that uses proprioceptive feedback regarding foot contact and leg position to predict an object's displacement during the occlusion. This prediction guides the perception system to robustly re-detect the object after the interaction, closing the loop between action and sensing to enable accurate tracking even after partial pushes. Using this feedback allows the robot to learn from physical outcomes, reclassifying an object as immovable if a push fails due to it being too heavy. We present results of implementing our approach on a Boston Dynamics Spot robot that show our interaction-aware approach achieves higher task success rates and tracking accuracy in pushing objects on stairs compared to open-loop baselines.