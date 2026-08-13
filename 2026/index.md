---
layout: default
title: Home
nav_order: 1
description: "Fundamentals of Computer Systems (COSI 131A)"
banner_heading: "Fundamentals of Computer Systems"
banner_description: "COSI 131A"
season_year: "Fall 2026"
permalink: /
---

|----------|----------|
| __Instructor__{: .fs-4} | [<u>Subhadeep Sarkar</u>](https://subhadeep.net){:target="_blank"}
| __TA__{: .fs-4} | Shubham Kaushik
| __Class Timings & Location__{: .fs-4} | *Room: TBD* <br/> Tue & Thu 3:55 PM – 5:15 PM |
| __Recitation Timings & Location__{: .fs-4} | *Room: TBD* <br/> Wed 5:40 PM – 7:40 PM |

## <u>Course Description</u>
<!-- TODO: replace with the official syllabus description once shared. -->
TBD

## <u>Prerequisites</u>
<!-- TODO: confirm against the official syllabus. -->
TBD

## <u>Learning Goals</u>
<!-- TODO: replace with the official syllabus learning goals. -->
TBD

## Instructor

{% assign instructors = site.staffers | where: 'role', 'Instructor' %}
{% for staffer in instructors %}
{{ staffer }}
{% endfor %}

{% assign teaching_assistants = site.staffers | where: 'role', 'Teaching Assistant' | sort: "order" %}
{% assign num_teaching_assistants = teaching_assistants | size %}
{% if num_teaching_assistants != 0 %}

## Teaching Assistants

{% for staffer in teaching_assistants %}
{{ staffer }}
{% endfor %}
{% endif %}
