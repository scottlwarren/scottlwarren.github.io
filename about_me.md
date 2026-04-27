---
layout: default
title: About Me
---
<!---
  ## Case Studies
  
  {% for cs in site.data.case_study %}
    <div class="cs-desc">
      <h4>{{ cs.title | markdownify }}</h4>
      <p>{{ cs.about | markdownify}}</p>
    </div>
  {% endfor %}
*
--->



<hr style="margin-top: 2rem; border: 0; border-top: 1px solid #eee;">
## Work History

{% for job in site.data.work_history %}
  <div class="cv-job">
    <h4><b>{{ job.role }}</b> | {{ job.company}}</h4>
    <p><em>{{ job.date }}</em></p>
    <p>{{ job.description | markdownify}}</p>
  </div>
{% endfor %}


<hr style="margin-top: 2rem; border: 0; border-top: 1px solid #eee;">
## Edcuation and Qualifications

{% for edu in site.data.education %}
  <div class="edu">
    <h4><b>{{ edu.qual }}</b> | {{ edu.inst }} | {{ edu.date }}</h4>
    <!---<p><em>{{ edu.date }}</em></p>--->
    <p>{{ edu.notes | markdownify}}</p>
  </div>
{% endfor %}
<hr style="margin-top: 2rem; border: 0; border-top: 1px solid #eee;">
## Publications

{% for pub in site.data.publication %}
  <div class="pubs">
    <h4><b>{{ pub.title }}</b></h4>
    
    <p><em>{{ pub.authors | markdownify | remove: '<p>' | remove: '</p>' }} | <strong>{{ pub.journal }}</strong> ({{ pub.date }})</em></p>
   
    <div>{{ pub.notes | markdownify }}</div>
    <a href="{{ pub.url }}">View Source</a>

  </div>
{% endfor %}