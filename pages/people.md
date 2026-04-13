---
title: People
layout: default
---

<h2 class="mb-3"><a id="staff"></a>Staff</h2>

{% assign members = site.profiles | where: 'staff', 'true' | sort: 'name' %}

<div class="grid-container">
{% for member in members %}
    {% if member.name == 'Özgür Şimşek' %}
    <div class="grid-item">
        {% include team_member.html member=member %}
    </div>
    {% endif %}
{% endfor %}
{% for member in members %}
    {% if member.name != 'Özgür Şimşek' %}
    <div class="grid-item">
        {% include team_member.html member=member %}
    </div>
    {% endif %}
{% endfor %}
</div>

<h2 class="mb-3"><a id="student"></a>PhD Students</h2>

{% assign members = site.profiles | where_exp: "item", "item.staff != true and item.alumni != true and item.intern != true" | sort: 'name' %}

<div class="grid-container">
{% for member in members %}
    <div class="grid-item">
        {% include team_member.html member=member %}
    </div>
{% endfor %}
</div>

<h2 class="mb-3"><a id="intern"></a>Other members</h2>

{% assign members = site.profiles | where: 'intern', true | sort: 'name' %}

<div class="grid-container">
{% for member in members %}
    <div class="grid-item">
        {% include team_member.html member=member %}
    </div>
{% endfor %}
</div>

<h2 class="mb-3"><a id="alumni"></a>Alumni</h2>

{% assign members = site.profiles | where: 'alumni', 'true' | sort: 'name' %}

<div class="grid-container">
{% for member in members %}
    <div class="grid-item">
        {% include team_member.html member=member is_alumni=true %}
    </div>
{% endfor %}
</div>

<h2 class="mb-3"><a id="interns-list"></a>Interns</h2>

<ul>
  <li><a href="https://www.linkedin.com/in/farazeid/">Farahmand Zeidaabadi</a> (Summer 2025: June &ndash; September)</li>
  <li><a href="https://sade-li.github.io/index.html">Sade Inniss</a> (Summer 2025: June &ndash; September)</li>
</ul>
