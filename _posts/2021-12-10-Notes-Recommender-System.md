---
layout: post
title: Notes - Recommender System
date: 2021-12-10 16:40:16
description: Study notes for recommender system, such as hacker news formula, ranking, etc.
tags: MachingLearning
categories: notes
---

This is based on [udemy course recommender system](https://www.udemy.com/course/recommender-systems/learn/lecture/11686566#overview)

# Basics

## 1. Hacker News Formula

[Hacker News intro](http://www.righto.com/2013/11/how-hacker-news-ranking-really-works.html)

{% include figure.html path="assets/img/hackernew.png" class="img-fluid rounded z-depth-1" %}

Because the time has a larger exponent than the votes, an article's score will eventually drop to zero, so nothing stays on the front page too long. This exponent is known as _gravity_.

But for efficiency, stories are individually reranked only occasionally. When a story is upvoted, it is reranked and moved up or down the list to its appropriate spot, leaving the other stories unchanged. Thus, the amount of reranking is significantly reduced.

There is, however, the possibility that a story stops getting votes and ends up stuck in a high position. To avoid this, every 30 seconds one of the top 50 stories is randomly selected and reranked. The consequence is that a story may be "wrongly" ranked for many minutes if it isn't getting votes. In addition, pages can be cached for 90 seconds.The score for an article shoots up rapidly and then slowly drops over many hours.

{% include figure.html path="assets/img/hackernew1.png" class="img-fluid rounded z-depth-1" %}

The scoring formula accounts for much of this: an article getting a constant rate of votes will peak quickly and then gradually descend. But the observed peak is even faster - this is because articles tend to get a lot of votes in the first hour or two, and then the voting rate drops off.

Combining these two factors yields the steep curves shown.The green triangles and text show where "controversy" penalties were applied. The blue triangles and text show where articles were penalized into oblivion, dropping off the top 60. Milder penalties are not shown here.

## 2. Reddit Ranking

[reddit algorithms intro](https://medium.com/hacking-and-gonzo/how-reddit-ranking-algorithms-work-ef111e33d0d9)

Use log: Idea of diminishing return.score is getting bigger as time passes by

{% include figure.html path="assets/img/imagew.png" class="img-fluid rounded z-depth-1" %}

## 3. Average Rating

Confidence: Normal, binomial,

**Wilson Score Interval**

{% include figure.html path="assets/img/wilson.png" class="img-fluid rounded z-depth-1" %}

[Binomial proportion confidence interval](https://en.wikipedia.org/wiki/Binomial_proportion_confidence_interval)

[how to not sort by average rating](https://www.evanmiller.org/how-not-to-sort-by-average-rating.html)

Score = Lower bound of Wilson score confidence interval for a Bernoulli parameter

**Smoothing:**

{% include figure.html path="assets/img/smoothing.png" class="img-fluid rounded z-depth-1" %}

**Explore-exploit dilemma**

{% include figure.html path="assets/img/deli.png" class="img-fluid rounded z-depth-1" %}

**Bayesian**[Conjugate prior](https://en.wikipedia.org/wiki/Conjugate_prior)

{% include figure.html path="assets/img/bayes1.png" class="img-fluid rounded z-depth-1" %}

{% include figure.html path="assets/img/bayes2.png" class="img-fluid rounded z-depth-1" %}

{% include figure.html path="assets/img/bayes3.png" class="img-fluid rounded z-depth-1" %}

{% include figure.html path="assets/img/bayes4.png" class="img-fluid rounded z-depth-1" %}

{% include figure.html path="assets/img/bayes5.png" class="img-fluid rounded z-depth-1" %}
