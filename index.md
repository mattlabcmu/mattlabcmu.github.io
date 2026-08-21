---
title: The Matt Lab
subtitle: We do Robot Autonomy for the real-world!
layout: page
show_sidebar: false
---

# About Us

We are part of the [Robotics Institute](https://www.ri.cmu.edu/) at [Carnegie Mellon University](https://www.cmu.edu/).

# Recent News

<div class="columns is-multiline">
    {% for post in site.news reversed limit: 2 %}
        <div class="column is-6">
            {% include post-card-news.html %}
        </div>
    {% endfor %}
</div>

<p class="has-text-right mb-6"><a href="{{ '/news/' | relative_url }}">All news →</a></p>

# Latest Research

<div class="columns is-multiline">
    {% assign sorted_publications = site.publications_list | sort: 'date' | reverse %}
    {% for post in sorted_publications limit: 2 %}
        <div class="column is-6 research-card">
            {% include post-card.html %}
        </div>
    {% endfor %}
</div>

<p class="has-text-right"><a href="{{ '/publications/' | relative_url }}">All publications →</a></p>
