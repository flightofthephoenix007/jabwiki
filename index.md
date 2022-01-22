# Who's requiring COVID-19 vaccines?

This is the running list of the companies, events, and universities requiring covid jabs. Pull requests gratefully accepted, especially around design or data formatting or correctness. If you are a journalist and would like to speak to someone about the list, email flightofthephoenix@protonmail.com. <a href="https://github.com/flightofthephoenix007/jabwiki.github.io/blob/main/README.md">Instructions for contributing are here</a>.

---

Jump to: <a href="/companies.html">Companies</a>. Jump to: <a href="/events.html">Events</a>. Jump to: <a href="/universities.html">Universities</a>.

---

<a name="companies"></a>
## [Companies - {{ site.data.companies | size }}](/companies.html)
{% assign sorted = site.data.companies | sort: 'name' %}
{% assign employee_policy_required = site.data.companies | where_exp:"item", "item.employee_policy contains 'Required'" | size %}

*Covid-19 jab required for employees: **{{ employee_policy_required}}***

### [See full list of companies](/companies.html)

---

<a name="events"></a>
{% assign jabtoenter = site.data.events | where_exp:"item", "item.status contains 'jabtoenter'" | size %}

## [Events - {{ site.data.events | size }}](/events.html)

*Events/festivals requiring the jab to attend: **{{jabtoenter}}***

### [See full list of events](/events.html)

---

<a name="universities"></a>

## [Universities -- {{ site.data.universities | size }}](/universities.html)

{% assign statuses = "" | split: "" %}
{% for university in site.data.universities %}
    {% assign status = university[1].status | downcase %}
    {% assign statuses = statuses | push: status %}
{% endfor %}
{% assign jabtolearn_count = statuses | where_exp:"status", "status contains 'jabtolearn'" | size %}
*Universities requiring jab for students: **{{jabtolearn_count}}***

### [See full list of universities](/universities.html)

---

Jump to: <a href="/companies.html">Companies</a>. Jump to: <a href="/events.html">Events</a>. Jump to: <a href="/universities.html">Universities</a>.
