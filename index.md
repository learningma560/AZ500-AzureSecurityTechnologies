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

## Legacy Labs

Older versions of the course labs, restored from the Wayback Machine (snapshots from 2022-2024). They no longer exist in the current course, or exist only in a newer form above.

| Lab | Notes |
| --- | --- |
| [Lab 02: Azure Policy]({{ site.github.url }}/Instructions/Legacy/LAB_02_AzurePolicy.html) | Removed from the current course |
| [Lab 03: Resource Manager Locks]({{ site.github.url }}/Instructions/Legacy/LAB_03_AzureLocks.html) | Removed from the current course |
| [Lab 13: Azure Monitor]({{ site.github.url }}/Instructions/Legacy/LAB_13_Azure_Monitor.html) | Removed from the current course |
| [Lab 07: Network Security Groups and Application Security Groups]({{ site.github.url }}/Instructions/Legacy/LAB_07_NSGs.html) | Older version of the NSGs lab |
| [Lab 08: Azure Firewall]({{ site.github.url }}/Instructions/Legacy/LAB_08_AzureFirewall.html) | Older version of the Azure Firewall lab |
