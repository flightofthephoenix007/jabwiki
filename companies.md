---
layout: default
title: Jab.Wiki | What brands & companies are requiring covid jabs?
description: A community-managed GitHub repository keeping track of the companies requiring covid jabs for employees.
tags: covid jab vaccine covid-19
---

# What companies are requiring COVID-19 vaccines?

---

Go [Home](/). Jump to: <a href="/events.html">Events</a>. Jump to: <a href="/universities.html">Universities</a>.

---

<a name="companies"></a>
## Companies - {{ site.data.companies | size }}
{% assign sorted = site.data.companies | sort: 'name' %}
{% assign employee_policy_required = site.data.companies | where_exp:"item", "item.employee_policy contains 'Required'" | size %}
{% assign customer_policy_required = site.data.companies | where_exp:"item", "item.customer_policy contains 'Required'" | size %}

---

  *Events requiring Covid jab: **{{attendee_policy_required}}** 

  *Events giving option for PCR clown test: **{{attendee_testing_option}}**

--- 

| Company | Employee Policy | Customer Policy | Last Update |
| --- | --- | --- | --- |
{% for company in sorted %}| {{company.name}} | {{company.employee_policy}} | {{company.customer_policy}} | {{company.last_update}} |
{% endfor %}

---

Back to top: <a href="#companies">Companies</a>. Jump to: <a href="/events.html">Events</a>. Jump to: <a href="/universities.html">Universities</a>. Go [Home](/).
