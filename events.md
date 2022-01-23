# What events/music festivals are requiring attendees to have COVID-19 jab or will accept a PCR test?

---

Go [Home](/). Jump to: <a href="/companies.html">Companies</a>. Jump to: <a href="/universities.html">Universities</a>.

---

<a name="events"></a>
{% assign jabtoplay_count = site.data.events | where_exp:"item", "item.status contains 'Required'" | size %}
{% assign testtoplay_count = site.data.events | where_exp:"item", "item.status contains 'Test'" | size %}

## Events - {{ site.data.events | size }}

*Events requiring Covid jab: **{{jabtoplay_count}}***
*Events requiring Covid test: **{{testtoplay_count}}***

{% for event in site.data.events %}
- {{event.name}}: {{event.status}}{% endfor %}

---

Back to top: <a href="#events">Events</a>. Jump to: <a href="/companies.html">Companies</a>. Jump to: <a href="/universities.html">Universities</a>. Go [Home](/)
