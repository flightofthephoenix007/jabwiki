# What companies are requiring COVID-19 vaccines?

---

Go [Home](/). Jump to: <a href="/events.html">Events</a>. Jump to: <a href="/universities.html">Universities</a>.

---

<a name="companies"></a>
## Companies - {{ site.data.companies | size }}
{% assign sorted = site.data.companies | sort: 'name' %}
{% assign employee_policy_required = site.data.companies | where_exp:"item", "item.employee_policy contains 'Required'" | size %}
{% assign employee_policy_customersRequired = site.data.companies | where_exp:"item", "item.employee_policy contains 'customersRequired'" | size %}

*Covid vaccine required for employees: **{{ employee_policy_required}}**, Covid vaccine required for customers: **{{ employee_policy_customersRequired }}***

| Company | Employee Policy | Customer Policy | Last Update |
| --- | --- | --- | --- | --- | --- |
{% for company in sorted %}| {{company.name}} | {{company.employee_policy}} | {{company.customer_policy}} | {{company.last_update}} |
{% endfor %}

---

Back to top: <a href="#companies">Companies</a>. Jump to: <a href="/events.html">Events</a>. Jump to: <a href="/universities.html">Universities</a>. Go [Home](/).
