---
title: "A Max-min Tree Approach to the Automated Construction of Ad Hoc Wireless Networks in Unknown Environments"
authors: "Charles Noren, Bhaskar Vundurthy, Namya Bagree and Matthew Travers"
venue: "2025 IEEE 21st International Conference on Automation Science and Engineering (CASE)"
date: 2025-08-17
paper_link: "https://ieeexplore.ieee.org/document/11163847/" 
# external_url: "" 
# video: ""
bibtex: |
  @inproceedings{noren2025max,
    title={A Max-min Tree Approach to the Automated Construction of Ad Hoc Wireless Networks in Unknown Environments},
    author={Noren, Charles and Vundurthy, Bhaskar and Bagree, Namya and Travers, Matthew},
    booktitle={2025 IEEE 21st International Conference on Automation Science and Engineering (CASE)},
    pages={2702--2709},
    year={2025},
    organization={IEEE}
  }
image: /img/publications/max_min_tree_comms.jpg
tags:
  - Multi-Robot Systems
  - Path Planning
  - Robot Communications

---

Reliable communication networks are essential for the remote operation of automated teams of robotic agents. For unknown (no prior map) communications-deprived (no existing communication infrastructure) environments, the robotic agents must construct the network as the robots move through the terrain. We present a novel method for automated network construction tailored for mobile robotic teams that require communication with a central base station. Our key innovation is the introduction of a maximin spanning tree structure, which guarantees a minimum level of communication performance between nodes. By directly optimizing node placement based on signal-based metrics, instead of relying on geometric surrogates like distance and visibility, we also achieve significant decreases in agent utilization while maintaining coverage for the traversed area. By using the robotic agents themselves as mobile repeaters in a communication network, each robotic agent can be individually assigned to prioritize network connectivity during critical operations. Numerical simulations on common Multi-Agent Path Finding benchmarks demonstrate up to a 36% reduction in the number of required nodes compared to existing techniques. Furthermore, this work guarantees robust network connectivity in dynamic environments, outperforming strongest-neighbor approaches that are vulnerable to link disruptions. Lastly, hardware tests confirm the robustness of our method in challenging scenarios encountered in real-world deployments.