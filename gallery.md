---
layout: default
title: Gallery
subtitle: Snapshots from around the lab
show_sidebar: false
permalink: /gallery/
---

<p class="has-text-centered mb-6 lab-gallery-intro">A few favorite moments — click a photo to see it larger.</p>

<div class="columns is-multiline is-variable is-5 lab-gallery">
    {% for item in site.data.gallery %}
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
