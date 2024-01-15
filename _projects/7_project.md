---
layout: page
title: Interruption Detection
description: Speech based interruption detection (2023)
img: assets/img/interupt.png
importance: 1
category: work
related_publications: einstein1956investigations, einstein1950meaning
---

## What is it about

During my postdoc I was working on developing an AI partner that is aimed to be taking part in small group collaboration, placed in classrooms. The role of this AI partner was to empower these kids to engage in a discussion around the different topics of class. Throughout the co-design sessions conducted with teachers (via professional development meetings) they expressed a need to monitor the group conversations for interruptions, in order to understand underlying aspects of the social dynamic of the participants. 

## What’s does it mean

This project is a speech processing project, where the repo below offers code to evaluate interruptions in speech of up to four participants (that’s at least the data we worked with) via two main approaches. I will soon attach a draft for a work that describes the technical details and compares results against different SOTA baselines. In this work we assume we have access to the speakers.


## Repo link
{% if site.data.repository7.github_repos %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repository7.github_repos %}
    {% include repository/repo.html repository=repo %}
  {% endfor %}
</div>
{% endif %}

## Next steps

There are interesting questions to consider around the limitation of speech processing to detect interruption, and discuss the roles and the kinds of interruptions we employ in our conversations. More on that will be shared soom 


<div class="row justify-content-sm-center"> 
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/block_diagram_f.pdf" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="caption">
    The processes of detecting interruption in a conversational snippet
    </div>
