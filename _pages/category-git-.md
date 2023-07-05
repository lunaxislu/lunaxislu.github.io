---
title: "git"
layout: archive
permalink: /git
author_profile: true
sidebar:
    nav: "sidebar-category"
---

{% assign posts = site.categories.git %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}