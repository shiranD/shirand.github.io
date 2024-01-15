---
layout: page
title: Long-tail prediction
description: Retrieval LM on rare frquency events (2021)
img: assets/img/plant.png
importance: 1
category: work
related_publications: dudy2020overcoming
---

## The back story

By the time we were working on the icon language modeling project, many language models had employed subword encodings to the tokenization process of words, making it more challenging for us to integrate our icons. We learned that the clinical setting in which these icons are used require clinicians to be adaptive to their patients expressive needs, where they may need to add new icons when new needs arise. The need of adaptability to new icons over time, the need to represent icons in our vocabulary and the worry of the effects of increased vocabulary size (considering its computational toll) led us to develop a new approach, which is a continuous prediction LM, or retrieval based LM as today is more known.

## What is this approach?

This approach is focused on predicting a vector representation of a token (often a word or a phrase) and decoding it based on a pre-trained embedding space (think word2vec) to figure out the predicted word. It splits the decoding from training and shrinks its final layer (to an embedding size ~500 and not vocabulary size ~50k).

<div class="row justify-content-sm-center"> 
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/learning_1.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="caption">
    a retrieval based approach for word prediction LM
    </div>
</div>


In my thesis {% cite dudy2020overcoming
%} I train on two well known datasets PubMed and GigaNews and show that the retrieval based model predicts more diverse words, especially ones that are less frequent. It does come with a tradeoff, where accuracy rates decrease. The typical model showed the exact opposite behavior. Here are the repos.


## Repo link
{% if site.data.repository6.github_repos %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repository6.github_repos %}
    {% include repository/repo.html repository=repo %}
  {% endfor %}
</div>
{% endif %}

