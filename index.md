---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---

{{ site.description }}

<br>

{% assign projects = site.projects | sort: 'index' %}
{% for project in projects%}

<a class="big_candy" href="{{project.href}}">{{project.title}}</a>
<div>
{% for link in project.links %}
<a class="small_candy" href="{{ link[1] }}">{{ link[0] }}</a>
{% endfor %}
</div>

---

{{ project.content }}
<br>
{% endfor %}