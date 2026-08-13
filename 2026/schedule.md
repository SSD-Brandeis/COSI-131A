---
layout: page
title: Schedule
nav_order: 1
description: Fundamentals of Computer Systems (COSI 131A)
banner_heading: "Schedule"
banner_description: "Course Schedule and Important Dates"
---

{% for schedule in site.modules %}
{{ schedule }}
{% endfor %}