---
title: "Developing Data Products"
author: "LB"
date: "28 11 2016"
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---


## Developing Data Products Course Project

### Estimating the Perplexity of a Probabilistic Model


---

## Perplexity Background

Perplexity is defined as 2 raised to the Cross-Entropy:

2^(-logq(x)*q(x))

Perplexity is a measure of how well a model fits some data, used to evaluate e.g., language models and for comparison purposes in various language technology applications.

It is a measure of how surprised the model is to see the data, which means that a lower model fits the data better.  Thus, it is a measure of uncertainty.  If the model is uniform, there is maximum uncertainty.  This is not always intuitive, and I have created an application which can visualize this property.

--- 
## Perplexity Maximization

The perplexity is maximized when the events are equiprobable.  This can be shown by means of a mathematical proof.  This application lets the user simulate a number of events (modeled by random numbers), whose frequency determine their probability.  The user can choose an interval from which random numbers will not be selected (say from 40 to 60 in a 1-100 range) to make the distribution of events less equal, while still retaining the property of a probability distribution, namely that the probability of all outcomes sum to one.


---

This gap is controllable by the user:

![plot of chunk unnamed-chunk-1](figure/unnamed-chunk-1-1.png)

---
Application user interface.  The perplexity of the model is updated as the sliders are moved.

![height](appui.png)
