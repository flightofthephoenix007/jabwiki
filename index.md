# Who's requiring COVID-19 vaccines?

## Updated 2022-01-25 - still a work in progress
This is the running list of the companies, events, and universities requiring covid jabs. 

This site was created after discovering my former-favorite shoe brand, Vans, was practicing medical tyrrany, requiring their employees to get it.  What other brands are doing this? This is where we will keep the live, running list. 

Pull requests gratefully accepted, especially around design or data formatting or correctness. 

If you are a journalist and would like to speak to someone about the list, email flightofthephoenix@protonmail.com. <a href="https://github.com/flightofthephoenix007/jabwiki.github.io/blob/main/README.md">Instructions for contributing are here</a>.

---

Jump to: <a href="/companies.html">Companies</a>. Jump to: <a href="/events.html">Events</a>. Jump to: <a href="/universities.html">Universities</a>.

---

<a name="companies"></a>

## Companies -- {{ site.data.companies | size }}](/companies.html)

{% assign sorted = site.data.companies | sort: 'name' %}
{% assign employee_policy_required = site.data.companies | where_exp:"item", "item.employee_policy contains 'Required'" | size %}
{% assign customer_policy_required = site.data.companies | where_exp:"item", "item.customer_policy contains 'Required'" | size %}

### [See full list of companies](/companies.html)

---

<a name="events"></a>

## Events -- {{ site.data.events | size }}](/events.html)

{% assign sorted = site.data.events | sort: 'name' %}
{% assign attendee_policy_required = site.data.events | where_exp:"item", "item.attendee_policy contains 'required'" | size %}
{% assign attendee_testing_option = site.data.events | where_exp:"item", "item.attendee_policy contains 'true'" | size %}
{% assign details = site.data.events | where_exp:"item", "item.details" | size %}


### [See full list of events](/events.html)

---

<a name="universities"></a>

## Universities -- {{ site.data.universities | size }}(/universities.html)

{% assign sorted = site.data.universities | sort: 'name' %}
{% assign student_policy_required = site.data.universities | where_exp:"item", "item.student_policy contains 'required'" | size %}
{% assign professor_policy_required = site.data.universities | where_exp:"item", "item.professor_policy contains 'required'" | size %}
{% assign university_testing_option = site.data.universities | where_exp:"item", "item.university_testing_option contains 'yes'" | size %}
{% assign details = site.data.universities | where_exp:"item", "item.details" | size %}

---

### [See full list of universities](/universities.html)

---

Jump to: <a href="/companies.html">Companies</a>. Jump to: <a href="/events.html">Events</a>. Jump to: <a href="/universities.html">Universities</a>.
