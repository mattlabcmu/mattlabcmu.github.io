---
layout: default
title: Gallery
subtitle: Snapshots from around the lab
show_sidebar: false
permalink: /gallery/
---

<p class="has-text-centered mb-6 lab-gallery-intro">A few favorite moments — click a photo to see it larger.</p>

<div class="columns is-multiline is-variable is-5 lab-gallery">
    {% for item in site.data.gallery.photos %}
    <div class="column is-4-desktop is-6-tablet" x-data="{ open: false }">
        <button type="button" class="lab-gallery-polaroid" x-on:click="open = true" aria-label="View {{ item.title }}">
            <span class="lab-gallery-tape" aria-hidden="true"></span>
            <img src="{{ item.image | relative_url }}" alt="{{ item.title }}">
            <span class="lab-gallery-caption">{{ item.title }}</span>
        </button>
        <div class="modal" x-bind:class="open ? 'is-active' : ''" x-cloak>
            <div class="modal-background" x-on:click="open = false"></div>
            <div class="modal-content lab-gallery-modal">
                <img src="{{ item.image | relative_url }}" alt="{{ item.title }}">
                <p class="lab-gallery-modal-caption">{{ item.title }}</p>
            </div>
            <button class="modal-close is-large" aria-label="close" x-on:click="open = false"></button>
        </div>
    </div>
    {% endfor %}
</div>

{% if site.data.gallery.videos %}
<h2 class="title is-3 has-text-centered mt-6 mb-4">Videos</h2>

<div class="columns is-multiline is-centered">
    {% for item in site.data.gallery.videos %}
    <div class="column is-8-desktop is-10-tablet">
        <div class="lab-gallery-video">
            {% include youtube.html video=item.youtube_id %}
            <p class="lab-gallery-caption">{{ item.title }}</p>
        </div>
    </div>
    {% endfor %}
</div>
{% endif %}
