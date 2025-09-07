---
title: "Events & Classes"
permalink: /events/
layout: splash
collection: events
description: "Workshops, classes, and series."
seo: true
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

{% assign _events = site.events %}
{% if _events == nil %}{% assign _events = '' | split: '' %}{% endif %}
{% assign dated = _events | where_exp: "e", "e.date != null" %}
{% assign upcoming = dated | where_exp: "e", "e.date >= site.time" | sort: 'date' %}
{% if upcoming and upcoming.size > 0 %}
  <div class="entries-list">
    {% for event in upcoming %}
      {% include archive-single.html type="list" post=event %}
    {% endfor %}
  </div>
{% else %}
  <p>No upcoming events right now. Check back soon.</p>
{% endif %}

## Past Events

{% assign past = dated | where_exp: "e", "e.date < site.time" | sort: 'date' | reverse %}
{% if past and past.size > 0 %}
  <div class="entries-list">
    {% for event in past %}
      {% include archive-single.html type="list" post=event %}
    {% endfor %}
  </div>
{% else %}
  <p>No past events to show yet.</p>
{% endif %}
