---
layout: page
title: Docker's FST
description: a wrapper for OpenFST and PywrapFST library (2016)
img: assets/img/docker.png
importance: 1
category: work
related_publications: dudy2018multi
---

## Finite State Transducers
FSTs or Finite State Transducers (or Automatons) are tool one can use for creating language models. They were especially popular in the era that pre-dated deep learning, (so before not only transformers were introduced, rather RNNs). FSTs are considered to be generative language models (LMs) since their outcome contains a graphical representation of all the strings found in that language, but no worries they can handle situations in which there is little data on particular patterns in the training (via backoff, for instance). Generally, these LMs can handle better low resourced data, compared to some deep learning approaches. 


## A little more
Technically these repos is based on the [OpenFST library](https://www.openfst.org/twiki/bin/view/FST/WebHome) implementation, [Pynini](https://github.com/kylebgorman/pynini) implementation by Kyle Gorman, and [OpenGRM](https://github.com/mjansche/opengrm-ngram/tree/master) implementation.
The repos here may assist you when you are working on a python compiler and are interested in working with OpenFST library, Pynini, and GRM. While by the time you read it, these repos may no longer maintain the latest version, it can inspire you to set one of your own based on the recipes available in each of the docker images associated with the corresponding library. The Dockerization of those tools/libraries is aimed at preventing a messy installation and help have a smooth start when prepraring to work with them.

## Repos link
The images below and their associated repos can be found in [Docker repos](https://hub.docker.com/r/shirand/fst_1.6.1)

How did I use it? In the project {% cite dudy2018multi %} we used the specializer to create the second baseline (PreLM). 

We have this


<div class="row justify-content-sm-center">
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.html path="assets/img/grm.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.html path="assets/img/fst.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="row justify-content-sm-center"> 
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.html path="assets/img/pynini.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
