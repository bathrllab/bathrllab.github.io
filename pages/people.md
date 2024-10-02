---
title: Team
layout: page
---

<!-- Staff -->
<h2 class="mb-3"><a id="staff"></a>Staff</h2>

{% assign members = site.profiles | where: 'staff', 'true' | sort: 'name' %}
<div class="row">
{% for member in members %}
    <div class="col-md-6">
        {% include team_member.html member=member %}
    </div>
    {% if forloop.index0 % 2 == 1 %}
        </div><div class="row">
    {% endif %}
{% endfor %}
</div>

<!-- Researchers -->
<!-- <h2 class="mb-3"><a id="researcher"></a>Researchers</h2>

{% assign members = site.profiles | where: 'category', 'postdoc' | sort: 'name' %}
<div class="row">
{% for member in members %}
    <div class="col-md-6">
        {% include team_member.html member=member %}
    </div>
    {% if forloop.index0 % 2 == 1 %}
        </div><div class="row">
    {% endif %}
{% endfor %}
</div> -->

<!-- Students -->
<h2 class="mb-3"><a id="student"></a>PhD Students</h2>

<!-- {% assign members = site.profiles | where: 'staff', 'false' | sort: 'name' %} -->
{% assign members = site.profiles | where_exp: "item", "item.staff != true" | sort: 'name' %}
<div class="row">
{% for member in members %}
    <div class="col-md-6">
        {% include team_member.html member=member %}
    </div>
    {% if forloop.index0 % 2 == 1 %}
        </div><div class="row">
    {% endif %}
{% endfor %}
</div>

<!-- Alumni -->
<!-- <h2 class="mb-3"><a id="alumni"></a>Alumni</h2>

{% assign members = site.profiles | where: 'category', 'alumni' | sort: 'name' %}
<div class="row">
{% for member in members %}
    <div class="col-md-6">
        {% include team_member.html member=member %}
    </div>
    {% if forloop.index0 % 2 == 1 %}
        </div><div class="row">
    {% endif %}
{% endfor %}
</div> -->
