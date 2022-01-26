# What universities are requiring the COVID-19 jab for students?

---

Go [Home](/). Jump to: <a href="/companies.html">Companies</a>. Jump to: <a href="/events.html">Events</a>.

---

<a name="universities"></a>

## Universities -- {{ site.data.universities | size }}

{% assign sorted = site.data.university | sort: 'name' %}
{% assign student_policy_required = site.data.university | where_exp:"item", "item.student_policy contains 'required'" | size %}
{% assign professor_policy_required = site.data.university | where_exp:"item", "item.professor_policy contains 'required'" | size %}
{% assign university_testing_option = site.data.university | where_exp:"item", "item.university_testing_option contains 'yes'" | size %}
{% assign details = site.data.university | where_exp:"item", "item.details" | size %}

---

  *Universities requiring jab for students: **{{student_policy_required}}***
  *Universities requiring jab for professors: **{{professor_policy_required}}***
  *Universities giving option for PCR clown test: **{{university_testing_option}}***
  
--- 

| University | Student Jab Policy | Professor Jab Policy | Option for PCR Clown Test | Details | Last Update |
| --- | --- | --- | --- | --- | --- |
{% for university in sorted %}| {{university.name}} | {{university.student_policy}} | {{university.professor_policy}} |{{university.university_testing_option}} | {{university.details}} | {{university.last_update}} |
{% endfor %}

---

Back to top: <a href="#universities">Universities</a>. Jump to: <a href="/companies.html">Companies</a>. Jump to: <a href="/events.html">events</a>. Go [Home](/).
