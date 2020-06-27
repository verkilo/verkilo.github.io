---
title: Settings
regenerate: true
settings: true
---

 {% assign sorted = site.data.settings | sort %}
 {% for setting in sorted %}
 {% assign t = setting | first %}
 {% assign settings = setting | last | sort: 'name' %}
 <h2>{{t | replace: '-', ' ' | upcase}}</h2>
 <dl>{% for s in settings %}
 <dt id='{{s.name}}'>{{s.name|upcase|replace: '-',' '}} ({{s.type}}) <code>{{s.name}}</code></dt>
 <dd>
 {{s.desc}}
 </dd>
 {% endfor %}</dl>
 {% endfor %}
