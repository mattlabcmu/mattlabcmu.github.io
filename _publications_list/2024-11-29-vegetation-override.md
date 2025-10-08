---
title: "Interaction-aware control for robotic vegetation override in off-road environments"
authors: "Charles Noren, Bhaskar Vundurthy, Sebastian Scherer and Matthew Travers"
venue: "Journal of Terramechanics 117 (2025)"
date: 2024-11-29
paper_link: "https://www.sciencedirect.com/science/article/pii/S0022489824000764" 
# external_url: "" 
# video: ""
bibtex: |
  @article{noren2025interaction,
    title={Interaction-aware control for robotic vegetation override in off-road environments},
    author={Noren, Charles and Vundurthy, Bhaskar and Scherer, Sebastian and Travers, Matthew},
    journal={Journal of Terramechanics},
    volume={117},
    pages={101034},
    year={2025},
    publisher={Elsevier}
  }
image: /img/publications/vegetation_override.jpg
tags:
  - Trajectory Optimization

---

Robotic systems tasked with completing off-road economic, military, or humanitarian missions often encounter environmental objects when traversing unstructured terrains. Certain objects (e.g. safety cones) must be avoided to ensure operational integrity, but others (e.g. small vegetation) can be interacted with (e.g. overridden/pushed) safely. Pure object-avoidance assumptions in conventional robotic system navigation policies may lead to inefficient (slow) or overly-cautious (immobilized) traversal behaviors in off-road terrains. To address this gap in system performance, we draw inspiration from existing hybrid dynamic system control literature. We have designed a nonlinear trajectory optimization controller that utilizes vegetation-interaction models as a jump map in the dynamics constraint. In contrast to purely vision-based navigation policies which classify the traversability of obstacles, the allowable subset of objects with which the vehicle can safely interact is now characterized by a data-driven collision model and the existence of a dynamically-feasible trajectory which satisfies the contact constraints. The controller’s capabilities are demonstrated on a full-sized autonomous utility task vehicle where objects including posts and trees of up to 25.4 [mm] and 81.8 [mm] diameter are overridden.