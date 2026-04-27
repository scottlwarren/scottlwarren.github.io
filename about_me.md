---
layout: default
title: About Me
---
## Case Studies

{% for cs in site.data.case_study %}
  <div class="cs-desc">
    <h4>{{ cs.title }}</h4>
    <p>{{ cs.about }}</p>
  </div>
{% endfor %}

## Technology


## Work History

{% for job in site.data.work_history %}
  <div class="cv-job">
    <h4>{{ job.role }} | {{ job.company }}</h4>
    <p><em>{{ job.date }}</em></p>
    <p>{{ job.description }}</p>
  </div>
{% endfor %}

