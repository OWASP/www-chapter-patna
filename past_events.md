---
title: PastEvents
displaytext: Past Events
layout: null
tab: true
order: 2
tags: patna
---

# Our Past Events

{% assign past_events = site.data.past_events | reverse %}

{% if past_events and past_events.size > 0 %}
  <ul>
    {% for event in past_events %}
      <li>
        <strong>Session {{ event.session }}:</strong> {{ event.title }}
        <br>
        Date: {{ event.date | date: "%d-%m-%Y" }}
        <br>
        Speaker: <a href="{{ event.speaker_linkedin }}">{{ event.speaker }}</a>
        <br>
        {% if event.video_url %}
          Video: <a href="{{ event.video_url }}">{{ event.title }}</a>
          <br>
        {% endif %}
        {% if event.ppt_url %}
          Presentation: <a href="{{ event.ppt_url }}">Download Slides</a>
        {% else %}
          Presentation: Link will be added soon.
        {% endif %}
      </li>
      <br>
    {% endfor %}
  </ul>
{% else %}
  <p>No past events recorded yet.</p>
{% endif %}

<hr>

## Stay Updated!

Follow us on our [Meetup page](https://www.meetup.com/OWASP-Patna-Chapter/) to know about upcoming events. Session videos will be linked here after they are uploaded.
