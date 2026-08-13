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
This course presents a comprehensive introduction to the fundamentals of computer systems — the layers of abstraction that let software run correctly and efficiently on real hardware. We will study how programs are represented, compiled, linked, and executed; how the memory hierarchy shapes performance; how the operating system virtualizes the CPU and memory; and how concurrency, processes, and I/O tie these layers together. Throughout the course, we will connect low-level system behavior to high-level programming practice, so that you leave the course able to reason about *why* your programs behave (and misbehave) the way they do.

## <u>Prerequisites</u>
<!-- TODO: confirm against the official syllabus. -->
A working knowledge of C/C++ programming and a fundamental understanding of data structures is required.

## <u>Learning Goals</u>
<!-- TODO: replace with the official syllabus learning goals. -->
Students who successfully complete all components of this course will be able to demonstrate the following by the end of the semester.
1. Understanding of how high-level code is translated into machine-executable programs (compilation, assembly, linking).
2. Ability to reason about data representation, memory layout, and the memory hierarchy (caching, virtual memory).
3. Understanding of the process abstraction, exceptional control flow, and system-level exception handling.
4. Knowledge of concurrent programming using processes, threads, and synchronization primitives.
5. Ability to reason about the performance tradeoffs inherent in systems-level design decisions.
6. Practical experience building and debugging systems-level programs.

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
