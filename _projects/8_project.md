---
layout: page
title: Mixed Emotions
description: Evaluating Cultural Represntation of Mixed Emotions (2024). Won Best Paper Award!
img: assets/img/flower.png
importance: 1
category: work
related_publications: dudy2024analyzing 
---

## Cultural Representation of Emotions n LLMs

This research aimed to examine how accurately well-established scholarly phenomena are reflected in Large Language Models (LLMs), particularly in relation to diverse values and identities. While LLMs have shown proficiency in multiple languages beyond English, we question whether these languages also convey the cultural characteristics of the communities they are most closely associated with.

## What's going on in this work

This study evaluates the cultural representation of emotions in Large Language Models (LLMs) by replicating the findings of Miyamoto et al. (2010) in their work [Culture and Mixed Emotions: Co-occurrence of Positive and Negative Emotions in Japan and the United States](https://psycnet.apa.org/buy/2010-09991-009). We assess how closely LLMs align with the original human-based study, which revealed differences in the prevalence of mixed emotions between Japanese and American participants. Additionally, we explore the strength of contextual signals and their influence on LLM responses, identifying which models are more sensitive to input and which are less so.
 
## Findings

We find that the investigated LLMs demostrate limited alignment with the mixed emotions phenomenon. We learn that LLMs are more sensitive to the language rather than the content (of participant's origin) they were provided with. 

## Repo link
{% if site.data.repository8.github_repos %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repository8.github_repos %}
    {% include repository/repo.html repository=repo %}
  {% endfor %}
</div>
{% endif %}
