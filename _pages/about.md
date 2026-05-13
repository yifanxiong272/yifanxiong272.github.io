---
permalink: /
title: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am Yifan Xiong, an incoming Ph.D. student in Computer Science at the [UIUC](https://illinois.edu/), advised by [Prof. Yiling Lou](https://yilinglou.github.io/), starting in Fall 2026. I received my B.Eng. degree from [Nanjing University](https://www.nju.edu.cn/en/), where I was fortunate to work with [Prof. Lei Bu](https://cs.nju.edu.cn/bulei/) and [Prof. Minxue Pan](https://minxuepan.github.io/), and to have the opportunity to work remotely with [Prof. Lingming Zhang](https://lingming.cs.illinois.edu/) in Summer 2024.

My research interests lie broadly in Software Engineering, including Software Testing, Program Analysis, and Formal Methods. I am particularly excited about how these foundations interact with modern LLMs and advanced Software Engineering Agents.

## News
- 2025.11: HAFuzz received the Distinguished Paper Award at the 18th National College Students' Innovation Annual Conference.

- 2025.06: HAFuzz was accepted to ICSE 2026.

## Selected Publications ([Full List](/publications/))

{% assign publications = site.publications | sort: "date" | reverse %}
<div class="publication-list publication-list--compact">
{% for post in publications limit: 3 %}
  {% include publication-entry.html post=post %}
{% endfor %}
</div>
<p class="publication-note"><sup>*</sup> Equal contribution.</p>

## Education

- Ph.D.Student in Computer Science, University of Illinois Urbana-Champaign. *Sep. 2026 -*

- Research Assistant in [SEG](https://seg.nju.edu.cn/index.action), Nanjing University. *Aug. 2025 - Dec. 2025*

- B.Eng. in Software Engineering, Naning University. *Sep. 2021 - July 2025*
