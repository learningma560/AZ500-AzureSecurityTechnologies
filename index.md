---
title: Online Hosted Instructions
permalink: index.html
layout: home
---

# Content Directory

Required labs files can be [downloaded here](https://github.com/learningma560/AZ500-AzureSecurityTechnologies/archive/master.zip)

Hyperlinks to each of the lab exercises and demos are listed below.

## Labs

{% assign labs = site.pages | where_exp:"page", "page.url contains '/Instructions/Labs'" %}
| Module | Lab |
| --- | --- | 
{% for activity in labs  %}| {{ activity.lab.module }} | [{{ activity.lab.title }}{% if activity.lab.type %} - {{ activity.lab.type }}{% endif %}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}

## Archived Labs

These labs were moved to the archive by the original authors and are no longer part of the current course. They are kept here for reference.

{% assign archived = site.pages | where_exp:"page", "page.url contains '/Instructions/Archived_Labs'" | sort: "path" %}
| Module | Lab |
| --- | --- | 
{% for activity in archived  %}| {{ activity.lab.module }} | [{{ activity.lab.title }}{% if activity.lab.type %} - {{ activity.lab.type }}{% endif %}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}
