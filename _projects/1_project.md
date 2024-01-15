---
layout: page
title: FST Specializer
description: a tool for employing FST special symbols (2017)
img: assets/img/phi.png
importance: 1
category: work
related_publications: dudy2018multi
---

## Finite State Transducers
FSTs or Finite State Transducers (or Automatons) are tool one can use for creating language models. They were especially popular in the era that pre-dated deep learning, (so before not only transformers were introduced, rather RNNs). FSTs are considered to be generative language models (LMs) since their outcome contains a graphical representation of all the strings found in that language, but no worries they can handle situations in which there is little data on particular patterns in the training (via backoff, for instance). Generally, these LMs can handle better low resourced data, compared to some deep learning approaches. 

## Repo link
{% if site.data.repository1.github_repos %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repository1.github_repos %}
    {% include repository/repo.html repository=repo %}
  {% endfor %}
</div>
{% endif %}

## A little more
This repo builds on the [OpenFST](https://www.openfst.org/twiki/bin/view/FST/WebHome) library. The Specializer is a tool that was built to effeciently process operations between one FST to another. We learned that in order to do so in python, we needed to work directly with the FST project written in C++ via Cython. There are several operations that this tool enables and are shown in the table. Each happens when two graphical representations (or lattices) are convoluted (or via a similar operation). The desired outcome will happen only when any of these symbols are on one of the lattices (of course this is a necessary but not sufficient condition)


How did I use it? In the project  {% cite dudy2018multi %}, we used the specializer to create the second baseline (PreLM) 


<div class="row justify-content-sm-center"> 
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/fst_table.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="caption">
    The special symbols behavior. Taken from the OpenFST documentation
    </div>
