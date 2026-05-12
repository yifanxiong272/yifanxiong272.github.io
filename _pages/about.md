---
permalink: /
title: "Yifan Xiong"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a student at the University of Illinois Urbana-Champaign. This website collects my academic updates, publications, talks, and teaching materials.

My current academic interests and project details will be updated here.

## News

- 2026.05: Welcome to my homepage.

## Selected Publications ([Full List](/publications/))

{% assign publications = site.publications | sort: "date" | reverse %}
<div class="publication-list publication-list--compact">
{% for post in publications limit: 3 %}
  {% include publication-entry.html post=post %}
{% endfor %}
</div>
<p class="publication-note"><sup>*</sup> Equal contribution.</p>

## Education

- University of Illinois Urbana-Champaign.

## Talks

Coming soon.

## Teaching

Coming soon.
