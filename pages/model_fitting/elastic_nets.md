---
title: Elastic Net Regression
tags:
keywords: "topic" # new keywords requiere to create a new tag file
last_updated: "October 16, 2020"
summary: "Elastic net regression is a method of regularization for fitting linear and logistic models using a combination of ridge and lasso methods to penalize the models."
published: true
sidebar: model_fitting_sidebar #name of yml sidebar file withouth extension
permalink: elastic_nets.html
folder: model_fitting
---


{% include note.html content="Please utilize the template below as a reference for your contribution. Adapt the template when deemed necessary" %}

## What is elastic net regression?

Elastic net regression is a method of regularization for fitting linear and logistic models using a combination of ridge and lasso methods to penalize the models. Regularization complements machine learning models that may have large numbers of predictors or correlated predictors which result in more variance in the model. By penalizing the model, elastic net introduces some bias which makes the model more reliable. Ridge regression penalizes the sum of squared coefficients  (L2) and lasso regression penalizes the sum of absolute values of the coefficients (L1). Elastic net combines these two types of penalties to find a good variance-bias tradeoff for the model. The optimal size of the penalty for a model can be determined via tuning parameters with cross-validation.


## Recommended Path for Learning

* Video overview of the concepts behind elastic net regression. Part 3 of a series on regularization.
Regularization Part 3: Elastic Net Regression
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/1dKRdX9bfIo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

* Video overview of how to implement elastic net, lasso, and ridge regression in R. Assumes knowledge of the concepts behind these three types of regression as taught in the 3-part Regularization series by the same author.
Elastic net regression in R
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/ctmNq7FgbvI" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

* Item 3 (video/code tutorial/document)

## Further Learning

## Video

* Video 1
* Video 2

## Applied papers 

* Paper 1
* Paper 2

## Online tutorials

* Fitting an elastic net model in R tutorial
<a href="https://asmquantmacro.com/2016/04/26/fitting-elastic-net-model-in-r/" target="_blank"> Fitting elastic net.</a>

* Online tutorial 2

## Theory papers 
* Paper 1
* Paper 2

{% include links.html %}
