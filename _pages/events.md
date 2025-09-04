---
title: "Events & Classes"
permalink: /events/
layout: splash
collection: events
description: "Workshops, classes, and series."
tagline: "Practice together. Learn, rest, and recover."
header:
  overlay_color: "#073f18ff"
---

I warmly invite you to join upcoming events, where each class and workshop is
designed to be gentle, welcoming, and accessible to everyone. Whether you’re
new or experienced, you can expect a supportive space focused on learning and
growing together at a comfortable pace. Even if specific details are still
being finalized, rest assured that every session prioritizes your safety and
well‑being as I explore breathwork and mindfulness practices with you. I look
forward to sharing this journey with you!

## Upcoming Events

{% assign upcoming = site.events | where_exp: 'e', 'e.date >= site.time' | sort: 'date' %}
{% if upcoming.size > 0 %}
<div class="entries-list">
  {% for event in upcoming %}
    {% include archive-single.html type="list" post=event %}
  {% endfor %}
  </div>
{% else %}
<p>No upcoming events right now. Check back soon.</p>
{% endif %}

## Past Events

{% assign past = site.events | where_exp: 'e', 'e.date < site.time' | sort: 'date' | reverse %}
{% if past.size > 0 %}
<div class="entries-list">
  {% for event in past %}
    {% include archive-single.html type="list" post=event %}
  {% endfor %}
</div>
{% else %}
<p>No past events to show yet.</p>
{% endif %}
