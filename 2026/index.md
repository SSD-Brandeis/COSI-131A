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

<div class="quick-facts">
  <div class="quick-fact">
    <h3><u>Instructor</u></h3>
    <p><a href="https://subhadeep.net" target="_blank">Subhadeep Sarkar</a></p>
  </div>
  <div class="quick-fact">
    <h3><u>TA</u></h3>
    <p><a href="https://www.shubhamkaushik.com/" target="_blank">Shubham Kaushik</a></p>
  </div>
  <div class="quick-fact">
    <h3><u>Class Timings &amp; Location</u></h3>
    <p>Golding Judaica: 110<br/>Tue &amp; Thu 3:55 PM – 5:15 PM</p>
  </div>
  <div class="quick-fact">
    <h3><u>Recitation Timings &amp; Location</u></h3>
    <p>Golding Judaica: 110<br/>Wed 5:40 PM – 7:40 PM</p>
  </div>
</div>

## <u>Course Description</u>
This course is an introduction to computer systems organization and operating systems. The objectives of the course are for you to learn three things. The first thing is how computer systems, operating systems, and, more generally, computers work. The goal is to demystify the interactions between the software you have written in other courses and hardware. A student graduating with a CS degree should be able to describe the chain of computer system events that occurs from when a user hits the reboot button to when the user's program runs, reading input and displaying results, from the register level to the operating system level to the application level. This is philosophically important, but it is also of practical interest to developers who need to figure out how to make a system do what they want it to do. The second thing is for you to learn the fundamental concepts of virtualization, concurrency, and persistence. These ideas are often best explained as abstractions that some software layer (usually the operating system) provides above imperfect hardware to make that hardware usable by programmers and users. The intent is for you to understand such abstractions well enough to be able to synthesize new abstractions when faced with new problems. The ideas and abstractions that we will cover are relevant not only to operating systems but also to many large-scale systems. Thus, a third goal of this course is to enhance your ability to understand, design, and implement such systems.

## <u>Prerequisites</u>
COSI 12B and COSI 21A. A working knowledge of Linux and Java is expected. The programming assignments will be in Java and C and must run on Linux.

## <u>Learning Goals</u>
Students who successfully complete all components of this course will be able to demonstrate the following by the end of the semester.

1. Understanding of the hardware abstraction layer and machine organization: how instructions, memory, and I/O are represented and executed at the machine level.
2. Understanding of the operating system's virtualization of the CPU — processes, threads, kernel/user mode, and CPU scheduling policies.
3. Ability to reason about concurrency and write correct synchronized programs using locks, condition variables, and related primitives, and to recognize and avoid deadlock.
4. Understanding of the operating system's virtualization of memory — memory management and virtual memory (paging).
5. Working proficiency in C, including awareness of common memory-safety risks and mitigations, and the ability to translate higher-level (Java) designs into C.
6. Understanding of persistence: file systems, disk organization, naming, and crash-consistent recovery/transactions.
7. Familiarity with virtual machines and how they relate to the rest of the systems stack.
{: type="a"}

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
