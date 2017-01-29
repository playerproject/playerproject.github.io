---
layout: page
title: Members
permalink: /members/
---
The Player Project github organization is made up of the following users:

{% for member in site.github.organization_members %}
* [{{ member.login }}]({{ member.html_url }})
{% endfor %}

