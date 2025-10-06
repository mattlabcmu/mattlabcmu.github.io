---
layout: page
title: Multi-Modal Perception UnderGround (MMPUG)
subtitle: Developing modular, resilient, and scalable multi-robot systems for real-world field applications
image: /img/projects/mmpug/mmpug_hero.jpg
link: /projects/mmpug
tags: 
    - Perception
    - Multi-Robot Coordination
    - SLAM
    - Heterogenous Robot Control
---

<div class="content">
  <p>The <strong>MMPUG</strong> project focuses on developing autonomous systems for rapid mapping and exploration in large, unknown, and often hazardous environments. Our goal is to assist a human operator by reducing their workload and enabling effective coordination of multi-robot teams in time-sensitive scenarios like search and rescue.</p>
</div>

<div class="columns is-centered">
    <div class="column is-three-fifths">
        <figure class="image">
            <img src="{{ page.image }}" alt="MMPUG Robot Fleet">
        </figure>
    </div>
</div>


<hr>

### Our Design Philosophy
Our architecture is built on crucial lessons learned from real-world deployments, including our team's participation in the DARPA Subterranean (SubT) Challenge. These principles guide every aspect of our system design:
* **Operator-Adjustable Autonomy:** The operator must be able to flexibly adjust the robot's level of autonomy to adapt to changing situations.
* **System Interoperability:** Seamless integration between different types of robots (e.g., wheeled and legged) is essential for dynamic deployment.
* **Centralized Control Flow:** Careful management of commands is necessary to prevent conflicts and ensure coordinated behavior across the team.
* **Adaptive User Interface:** The operator's interface should dynamically adapt to the current context, presenting only valid actions to reduce cognitive load.
* **Extensible System Design:** The architecture must be modular to allow for the rapid development and integration of new capabilities.

<hr>

### Key Architectural Features

Our system is designed from the ground up to embody these lessons, resulting in a powerful and flexible platform for multi-robot operations.

<div class="block">
<div class="columns is-vcentered">
  <div class="column is-6">
    <div class="content">
      <h4>Hierarchical Control & Sliding-Mode Autonomy</h4>
      <p>At the core of our system is the principle of <strong>"sliding-mode autonomy,"</strong> giving the operator the flexibility to blend human intuition with machine precision. This is managed by a <strong>Behavior Tree</strong> on each robot, allowing the operator to seamlessly switch between four distinct levels of control:</p>
      <ul>
        <li><b>Full Manual:</b> Direct teleoperation where the operator has complete, low-level control over the robot's movements.</li>
        <li><b>Smart Joystick:</b> An assisted driving mode where the operator provides a general direction, and the robot's onboard planner intelligently navigates around obstacles.</li>
        <li><b>Waypoint Mode:</b> The operator assigns a specific goal on the map, and the robot autonomously plans and executes the entire path to get there, as shown in the video.</li>
        <li><b>Exploration Mode:</b> The highest level of autonomy, where the robot is tasked to explore an unknown area and makes its own decisions to efficiently map the environment.</li>
      </ul>
    </div>
  </div>
  <div class="column is-6">
    {% include youtube.html video="mvTMi0uOae4" %}
    <p class="has-text-centered is-size-7"><em>A high-speed UGV navigating a complex corridor and obstacle course using Waypoint mode.</em></p>
  </div>
</div>
</div>

<div class="block">
<div class="columns is-vcentered is-flex-direction-row-reverse">
    <div class="column is-6">
        <div class="content">
            <h4>Advanced SLAM for Challenging Environments</h4>
            <p>Standard mapping algorithms often fail in visually repetitive or sparse environments. We have developed custom <strong>SLAM (Simultaneous Localization and Mapping)</strong> capabilities designed to be robust in difficult scenarios, such as long, feature-poor hallways and large, multi-floor structures. Our system maintains accurate localization and creates consistent, globally-aligned maps where other methods would accumulate significant drift.</p>
        </div>
    </div>
    <div class="column is-6">
        {% include youtube.html video="IhcWP8s4mYU" %}
        <p class="has-text-centered is-size-7"><em>Demonstration of our robust SLAM performance in a long, feature-poor corridor.</em></p>
    </div>
</div>
</div>

<div class="block">
<div class="columns is-vcentered">
  <div class="column is-6">
    <div class="content">
      <h4>Coordinated Behaviors: Dynamic Convoy Formation</h4>
      <p>The modular design simplifies the development of complex multi-agent behaviors. In <strong>convoy mode</strong>, an operator controls only the lead vehicle. Follower robots use a dedicated 'convoy coordinator' module to autonomously maintain formation. Our system is designed for flexibility, allowing new robots to be seamlessly added to the convoy on the fly, without interrupting the mission.</p>
    </div>
  </div>
  <div class="column is-6">
    {% include youtube.html video="g0br5gaPTPM" %}
    <p class="has-text-centered is-size-7"><em>Robots forming up and maintaining a convoy, with new members joining dynamically.</em></p>
  </div>
</div>
</div>

<div class="block">
<div class="columns is-vcentered is-flex-direction-row-reverse">
  <div class="column is-6">
    <div class="content">
        <h4>Coordinated Behaviors: Communication-Aware Peel-Off</h4>
        <p>Operating in communication-degraded environments is a major challenge. Our convoy can perform a strategic <strong>"peel-off"</strong> maneuver, where trailing robots are commanded to autonomously stop and act as static communication relays. This intelligently extends the network range, ensuring the lead robots stay connected to the base station as they push deeper into an unknown area.</p>
    </div>
  </div>
  <div class="column is-6">
    {% include youtube.html video="your_video_id_for_peel_off" %}
    <p class="has-text-centered is-size-7"><em>A follower robot peeling off from the convoy to become a comms relay.</em></p>
  </div>
</div>
</div>

<hr>

### Advanced Vertical Mobility & Staircase Navigation

Navigating between floors is a critical capability for exploring complex urban and subterranean structures. Our system features a comprehensive suite of tools for detecting and traversing staircases using a heterogeneous team.

<div class="block">
<div class="columns is-vcentered">
  <div class="column is-6">
    <div class="content">
        <h4>Long-Range Traversal</h4>
        <p>Our legged Spot robot is capable of autonomously navigating long and challenging staircases, including multiple flights in a single traversal, enabling rapid access to upper and lower floors.</p>
    </div>
  </div>
  <div class="column is-6">
    {% include youtube.html video="oiZEK4yqoMY" %}
    <p class="has-text-centered is-size-7"><em>Spot traversing multiple continuous flights of stairs while mapping and estimating the staircases.</em></p>
  </div>
</div>
</div>

<div class="block">
<div class="columns is-vcentered is-flex-direction-row-reverse">
  <div class="column is-6">
    <div class="content">
        <h4>Heterogeneous Map Merging & Tasking</h4>
        <p>Our system enables true robot collaboration. A high-speed wheeled robot can first discover and map a staircase on the ground floor. This staircase location is then automatically shared across the network, allowing a legged Spot robot to be tasked with autonomously navigating to that precise location to begin exploration of the next level.</p>
    </div>
  </div>
  <div class="column is-6">
    {% include youtube.html video="your_video_id_for_stair_merging" %}
    <p class="has-text-centered is-size-7"><em>A wheeled robot detects a staircase, and a Spot robot uses this shared data to navigate to it.</em></p>
  </div>
</div>
</div>

<div class="block">
<div class="columns is-vcentered">
  <div class="column is-6">
    <div class="content">
        <h4>Single-Command Multi-Floor Exploration</h4>
        <p>The ultimate goal is to reduce operator workload. With our system, an operator can issue a single high-level command to get to a specific floor. The robot then autonomously plans based on all the detected staircases and traverses them without further human intervention.</p>
    </div>
  </div>
  <div class="column is-6">
    {% include youtube.html video="uW5ALUqfOZs" %}
    <p class="has-text-centered is-size-7"><em>A Spot robot autonomously navigating a multi-floor building from a single operator command.</em></p>
  </div>
</div>
</div>

<hr> 

<div class="block">
  <div class="content">
      <h4>Adaptive Operator Interface</h4>
      <p>To minimize operator cognitive load, our interface is split into two main displays: an <strong>RViz window</strong> for 3D situational awareness (maps, camera feeds) and a custom <strong>touch-enabled GUI</strong> for robot commanding and feedback. The GUI is adaptive; based on feedback from the robot's behavior tree, it dynamically updates to present only valid actions to the operator. For example, the 'Start Convoy' action only becomes available when multiple robots are selected, preventing errors and simplifying control.</p>
      <div class="columns is-centered">
          <div class="column is-three-fifths">
              <figure class="image">
                  <img src="/img/projects/mmpug/operator_interface.jpg" alt="MMPUG Operator Interface">
                   <figcaption class="has-text-centered is-size-7"><em>The dual-screen operator setup with RViz for situational awareness and a touch GUI for control.</em></figcaption>
              </figure>
          </div>
      </div>
  </div>
</div>