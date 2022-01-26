---
layout: default
title: Jab.Wiki | What events are requiring covid jabs?
description: A community-managed GitHub repository keeping track of the events requiring covid jabs for attendees. 
tags: covid jab vaccine covid-19
---
# What events/music festivals are requiring the COVID-19 jab?

---

Go [Home](/). Jump to: <a href="/companies.html">Companies</a>. Jump to: <a href="/universities.html">Universities</a>.

---
<a name="events"></a>
## Events - {{ site.data.events | size }}
{% assign sorted = site.data.events | sort: 'name' %}
{% assign attendee_policy_required = site.data.events | where_exp:"item", "item.attendee_policy contains 'required'" | size %}
{% assign attendee_testing_option = site.data.events | where_exp:"item", "item.attendee_testing contains 'yes'" | size %}
{% assign details = site.data.events | where_exp:"item", "item.details" | size %}

---

  *Events requiring Covid jab: **{{attendee_policy_required}}** 

  *Events giving option for PCR clown test: **{{attendee_testing_option}}**

--- 

| Event | Attendee Jab Policy | Option for PCR Clown Test | Details | Last Update |
| --- | --- | --- | --- | --- |
{% for event in sorted %}| {{event.name}} | {{event.attendee_policy}} | {{event.attendee_testing}} | {{event.details}} | {{event.last_update}}

---

Back to top: <a href="#events">Events</a>. Jump to: <a href="/companies.html">Companies</a>. Jump to: <a href="/universities.html">Universities</a>. Go [Home](/)
