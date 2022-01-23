# What universities are requiring the COVID-19 jab for students?

---

Go [Home](/). Jump to: <a href="/companies.html">Companies</a>. Jump to: <a href="/events.html">Events</a>.

---

<a name="universities"></a>

## Universities -- {{ site.data.universities | size }}

{% assign statuses = "" | split: "" %}
{% for university in site.data.universities %}
    {% assign status = university[1].status | downcase %}
    {% assign statuses = statuses | push: status %}
{% endfor %}
{% assign jabtolearn_count = statuses | where_exp:"status", "status contains 'jabtolearn'" | size %}
*Universities requiring jab for students: **{{jabtolearn_count}}***

{% for university_hash in site.data.universities -%}
{% assign university = university_hash[1] %}
- {{university.name}}: {{university.status}} (Last update: {{university.last_update}})
{%- endfor %}

---

Back to top: <a href="#universities">Universities</a>. Jump to: <a href="/companies.html">Companies</a>. Jump to: <a href="/events.html">events</a>. Go [Home](/).
