---
layout: page
title: OCLM
description: Online Contextual LM (2018)
img: assets/img/tree.png
importance: 1
category: work
related_publications: dudy2018multi, dong2019noisy
---

## Finite State Transducers
FSTs or Finite State Transducers (or Automatons) are tool one can use for creating language models. They were especially popular in the era that pre-dated deep learning, (so before not only transformers were introduced, rather RNNs). FSTs are considered to be generative language models (LMs) since their outcome contains a graphical representation of all the strings found in that language, but no worries they can handle situations in which there is little data on particular patterns in the training (via backoff, for instance). Generally, these LMs can handle better low resourced data, compared to some deep learning approaches. 


## A little more
The context for this project revolves around the Brain-Computer interface project I took part in during my PhD, where we developed a language model to integrate to a speller system, assisting people with severe speech-language impairments communicate with their environment. The system has a rapid letter (symbol) display, such that once a patient recognizes their target symbol an EEG distribution over the step of symbols is transferred to the LM model. In turn, the model is required to disambiguate the word they are trying to spell. This means the most likely symbols from a given distribution remain, and are added to additional ones until a valid word is formed. Belowe there are two consecutive time slots demonstrating that.

## Repo link
{% if site.data.repository3.github_repos %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repository3.github_repos %}
    {% include repository/repo.html repository=repo %}
  {% endfor %}
</div>
{% endif %}


This is this externally what is going on, internally the poster (as well as the paper on OCLM {% cite dudy2018multi %}) explains how we arrive at those word paths employing FSTs and relying both on information from words as well as characters.


<div class="row justify-content-sm-center"> 
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.html path="assets/img/d1.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.html path="assets/img/d2.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="caption">
    On the left and right time steps T and T+1 accordingly introducing the current evidence coming from EEG, the likely next char, and the likely next word being formed (# indicates space). 
    </div>
    </div>


In the figure shown on the left, the next char is very likely to be **i** or **y**, forming **tonight** or **gonna**. On the right, on time step T+1 the system predicts **space** or **a** forming **tony** or **tonya**.


We had a followup where our system was compared to what then was the SOTA -- LSTM -- led by {% cite dong2019noisy %} to further evaluate hownoisy likelihoods effect prediction by different models. 
