---
layout: page
title: Word Fairness
description: Evaluating LMs on word frequency distribution (2020)
img: assets/img/fair.png
importance: 1
category: work
related_publications: dudy2020some
---

## Fairness in word type prediction

This research aimed to investigate the relationship between word frequency and prediction accuracy in a word prediction rate. Or how well do LM predict less frequent words. This question is an offshoot of a longer work that formed my thesis that is aimed at overcoming the blindspot of LM where the less they are trained (or fine-tuned) with certain events the harder they would do in predicting them -- which is the long-tail problem. 

## What's going on in this work

This work is focused on comparing performances on what were then SOTA models on a word prediction task, which means there is a clear output expected to be predicted based on the reference. The technical challenge was to write a Depth-First search component in order to compare only complete words to the reference word (and this is what the repo is offering), as the subword units and methods vary across different LM.

## Findings

In the first part we found that not only are models less accurate in terms of predicting correctly a word on lower frequency bands, they are also less diverse. In the final part of the paper we can also see that models struggle assigning the right meaning to low frequency words. 


## Repo link
{% if site.data.repository5.github_repos %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repository5.github_repos %}
    {% include repository/repo.html repository=repo %}
  {% endfor %}
</div>
{% endif %}

You can read more about it {% cite dudy2020some %} or watch it [here](https://www.youtube.com/watch?v=xflaZmDf3IU), but I have to warn you the sound is not the best ;-)

<div class="row justify-content-sm-center"> 
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/para_task.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="caption">
    A paraphrasng task showing that LM relatively fail to correctly score paraphrases when they involve rare words
    </div>
