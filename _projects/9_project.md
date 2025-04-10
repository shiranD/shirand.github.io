---
layout: page
title: geographical divide
description: Unequal Opportunities: Examining the Bias in Geographical Recommendations by Large Language Models (2025). Won Honorable Mention Award!
img: assets/img/urban_rural_divide.png
importance: 1
category: work
related_publications: dudy2025unequal 
---

## Some background

Over the past couple of years there has been a gradual shift from search engines to using LLMs for all sorts of needs. Search engines goal is to provide users with opportunities. Given that LLMs objective is to produce the most likely string as an output and their statitical nature of training, can LLMs live up to this goal? In this work we evalaute how well they provide opportunities to their users. Who gets to benefit? Who stands to lose? Are LLMs complementary or similar to each other in the opportunities they provide? 

## What's going on in this work

We designed queries to solicit location recommendations from state-of-the-art large language models (LLMs) for three specific use cases: relocating, traveling, and starting a business within a particular U.S. state. Our study proceeds in two parts. First, we conduct a textual analysis of the LLMs' responses, identifying notable similarities in the cities recommended and the underlying reasoning provided. In the second part, we examine the demographic characteristics of the suggested locations and uncover consistent demographic biases across all models, raising concerns not only about the specific similarities of bias, but also about their homogeneity of their behavior. 
 
## Findings

Our findings indicate that the locations recommended by LLMs were disproportionately skewed toward areas with wealthier and more highly educated populations. In contrast, locations known to support individuals with disabilities were underrepresented relative to ground-truth data. While the textual analysis did not reveal overt patterns of similarity, the demographic evaluation uncovered significant alignment in the types of locations suggested.

The similarities in LLM responses run deeper than what surface-level textual analysis can reveal.
LLMs produced strikingly similar outputs, raising concerns about a monocultural representation of knowledge—shaping not only what we know, but also how we know and think.
The models appear to narrow users' access to opportunity by consistently steering them toward a limited set of privileged locations.

## Repo link
{% if site.data.repository9.github_repos %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repository9.github_repos %}
    {% include repository/repo.html repository=repo %}
  {% endfor %}
</div>
{% endif %}
