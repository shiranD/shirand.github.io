---
layout: page
title: Icon Language
description: Developing icon-based LMs (2018)
img: assets/img/2icons.png
importance: 1
category: work
related_publications: dudy2018compositional
---

## Icon language 

Icon language is a language employed by speech-language clinicians as a conversational means with people who may have experienced Traumatic Brain injuries, where they struggle to interpret meaning just by the shape of a word. Icons then, are offering a more intuitive solution to communicate with their environment. Icons are also used with the younger population as well, for instance, kids with cerebral palsy may use icons as they may experience difficulty reading.

## The back story

As part of working on the brain-computer speller I mentioned in previous projects, we wanted to expand the language symbol sets incorporated into our system. For that we were able to collaborate with a commercial partner on the SymbolStix icon set. The goal, as expected, was to train a language model for immediate integration, but the problem turned out to be that we had no patterns of the icon language. And therefore that became our project, which is how to create a language for a patternless symbol set.

<div class="row justify-content-sm-center"> 
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/icon_lm.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="caption">
    The figure describes an illustration of an icon language model
    </div>
</div>

You can read more on how we created an icon language model in {% cite dudy2018compositional %} but you can also watch a 10 minutes [talk I gave on it](https://www.youtube.com/watch?v=ZGnUPWMePOQ) at NW-NLP conference (back in 2018) as well. The repo is below.

## Repo link
{% if site.data.repository4.github_repos %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repository4.github_repos %}
    {% include repository/repo.html repository=repo %}
  {% endfor %}
</div>
{% endif %}

