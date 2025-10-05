---
title: "A Bayesian Modeling Framework for Estimation and Ground Segmentation of Cluttered Staircases"
authors: "Prasanna Sriganesh, Burhanuddin Shirose and Matthew Travers"
venue: "IEEE Robotics and Automation Letters (RA-L)"
date: 2025-03-10
paper_link: "https://ieeexplore.ieee.org/document/10918822" 
external_url: "https://www.prassi.me/bayesian-staircase-estimation" 
# internal_url:
github: 'https://github.com/Prassi07/staircase_autonomy'
video: "https://www.youtube.com/watch?v=8baHgQ_rGLs"
bibtex: |
 @article{sriganesh2025bayesian,
  title={A Bayesian Modeling Framework for Estimation and Ground Segmentation of Cluttered Staircases},
  author={Sriganesh, Prasanna and Shirose, Burhanuddin and Travers, Matthew},
  journal={IEEE Robotics and Automation Letters},
  year={2025},
  volume={10},
  number={5},
  pages={4164-4171},
  publisher={IEEE}
 }
image: /img/publications/stair_bayesian_estimation.jpg
tags:
  - Robot Perception
  - Bayesian Inference

---
Autonomous robot navigation in complex environments requires robust perception as well as high-level scene understanding due to perceptual challenges, such as occlusions, and uncertainty introduced by robot movement. For example, a robot climbing a cluttered staircase can misinterpret clutter as a step, misrepresenting the state and compromising safety. This requires robust state estimation methods capable of inferring the underlying structure of the environment even from incomplete sensor data. In this paper, we introduce a novel method for robust state estimation of staircases. To address the challenge of perceiving occluded staircases extending beyond the robot's field-of-view, our approach combines an infinite-width staircase representation with a finite endpoint state to capture the overall staircase structure. This representation is integrated into a Bayesian inference framework to fuse noisy measurements enabling accurate estimation of staircase location even with partial observations and occlusions. Additionally, we present a segmentation algorithm that works in conjunction with the staircase estimation pipeline to accurately identify clutter-free regions on a staircase. Our method is extensively evaluated on real robot across diverse staircases, demonstrating significant improvements in estimation accuracy and segmentation performance compared to baseline approaches.