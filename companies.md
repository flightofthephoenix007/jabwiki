# What companies are requiring COVID-19 vaccines?

---

Go [Home](/). Jump to: <a href="/events.html">Events</a>. Jump to: <a href="/universities.html">Universities</a>.

---

<a name="companies"></a>
## Companies - {{ site.data.companies | size }}
{% assign sorted = site.data.companies | sort: 'name' %}
{% assign employeePolicy_required = site.data.companies | where_exp:"item", "item.employeePolicy contains 'Required'" | size %}
{% assign customerPolicy_required = site.data.companies | where_exp:"item", "item.customerPolicy contains 'Required'" | size %}

*Covid vaccine required for employees: **{{ employeePolicy_required}}**, Covid vaccine required for customers: **{{ customerPolicy_required }}***

| Company | Employee Policy | Customer Policy | Last Update |
| --- | --- | --- | --- |
{% for company in sorted %}| {{company[1].name}} | {{company[1].employeePolicy}} | {{company[1].customerPolicy}} | {{company.last_update}} |
{% endfor %}

---

Back to top: <a href="#companies">Companies</a>. Jump to: <a href="/events.html">Events</a>. Jump to: <a href="/universities.html">Universities</a>. Go [Home](/).
