---
title: "Distributed Optimal Control Framework for High-Speed Convoys: Theory and Hardware Results"
authors: "Namya Bagree, Charles Noren, Damanpreet Singh, Matthew Travers and Bhaskar Vundurthy"
venue: "22nd IFAC World Congress 2023"
date: 2023-07-09
paper_link: "https://www.sciencedirect.com/science/article/pii/S2405896323015197" 
# external_url: ""
# internal_url: "" 
# github_url: ""
# video: ""
bibtex: |
  @article{bagree2023distributed,
    title={Distributed optimal control framework for high-speed convoys: Theory and hardware results},
    author={Bagree, Namya and Noren, Charles and Singh, Damanpreet and Travers, Matthew and Vundurthy, Bhaskar},
    journal={IFAC-PapersOnLine},
    volume={56},
    number={2},
    pages={2127--2133},
    year={2023},
    publisher={Elsevier}
  }
image: /img/publications/distributed_convoy.jpg
tags:
 - Model Predictive Control
 - Multi-Robot Systems

---

Practical deployments of coordinated fleets of mobile robots in different environments have revealed the benefits of maintaining small distances between robots, especially as they move at higher speeds. However, this is counter-intuitive in that as speed increases, reducing the amount of space between robots also reduces the time available to the robots to respond to sudden motion variations in surrounding robots. However, in certain examples, the benefits in performance due to traveling at closer distances can outweigh the potential instability issues, for instance, autonomous trucks on highways that optimize energy by vehicle “drafting” or smaller robots in cluttered environments that need to maintain close, line of sight communication, etc. To achieve this kind of closely coordinated fleet behavior, this work introduces a model predictive optimal control framework that directly takes non-linear dynamics of the vehicles in the fleet into account while planning motions for each robot. The robots are able to follow each other closely at high speeds by proactively making predictions and reactively biasing their responses based on state information from the adjacent robots. This control framework is naturally decentralized and, as such, is able to apply to an arbitrary number of robots without any additional computational burden. We show that our approach is able to achieve lower inter-robot distances at higher speeds compared to existing controllers. We demonstrate the success of our approach through simulated and hardware results on mobile ground robots.