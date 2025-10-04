---
title: The Matt Lab
subtitle: We do Robot Autonomy, for the real-world!
layout: page
show_sidebar: true
---

# About Us

We are part of the [Robotics Institute](https://www.ri.cmu.edu/) at [Carnegie Mellon University](https://www.cmu.edu/).

# Recent News

<div class="columns is-multiline">
    {% for post in site.news limit: 2 %}
        <div class="column is-6">
            {% include post-card-news.html %}
        </div>
    {% endfor %}
</div>