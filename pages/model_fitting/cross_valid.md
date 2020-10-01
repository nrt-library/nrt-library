---
title: Cross Validation
tags:
keywords: "topic" # new keywords requiere to create a new tag file
last_updated: "June 1, 2020"
summary: "Cross Validation is a method of assessing model performance by partioning data into multiple training and testing sets"
published: true
sidebar: model_fitting_sidebar #name of yml sidebar file withouth extension
permalink: cross_valid.html
folder: model_fitting
---

## What is Cross Validation (CV)?

While cross validation is a common technique for estimating expected performance of a model in new data, cross validation can also be used to select the “best” configuration of a model (i.e. select the model that is expected to perform best in new data and is therefore closest to the true data generating process). Cross validation for parameter selection includes both hyperparameter tuning (or choosing the best parameter values for different statistical models) as well as choosing the best model configuration (e.g. using CV for selecting covariates, deciding on X transformations, outlier identification approaches, or selecting between different statistical models).


## Recommended knowledge before starting

To get the most out of these materials, it is recommended that you have a base level knowledge of what cross validation is. Here are recommended selected readings on cross validation from two *free* online books: [James et al. (2013) Chapter 5: Resampling Methods (pp 175 - 186)](http://faculty.marshall.usc.edu/gareth-james/ISL/) and [Kuhn and Johnson (2018) Chapter 4: Resampling Techniques (pp 67 - 78)](https://vuquangnguyen2016.files.wordpress.com/2018/03/applied-predictive-modeling-max-kuhn-kjell-johnson_1518.pdf)

It is also recommended, but not necessary, to have some knowledge of basic model fitting and evaluation techniques (materials included here use mostly regression, decision trees, and [neural nets](neural_networks_landing_page) in their examples). Many code tutorials contain data cleaning and feature engineering leading up to the code describing how to use CV for parameter selection, which may be confusing if the reader has not had some exposure to machine learning model building pipelines before.

## You should use cross validation for parameter selection if…
-You are fitting a statistical model with hyperparameters that need tuning
-You are considering multiple combinations of model configurations (e.g.  features or statistical algorithms) 
-You want to build predictive models that will generalize to predict well in new data


## Ideas, concepts, or tools that are associated with this topic
R/RStudio (especially the caret package, tidymodels, and parsnip packages)
Python
Cross validation/CV (particularly bootstrapped CV, k-fold CV, and nested CV)
Basic knowledge of standard machine learning (ML) models (mostly lasso and elastic net regression, tree based methods, neural nets)
Bias/variance trade offs in model fitting and evaluation
Generalizability of predictive models (why its important, how to prioritize it, and how to assess it)


## Recommended path for learning:
I have included examples in both python and R, but would recommend viewing them all as they each address different components of using CV for parameter selection. Start with the first online tutorial  (A “short” introduction to model selection), then watch the two videos in order, then read the “Model training and tuning” help guide for the caret package,  then read through the second online tutorial (Product Price Prediction), and finish with the Varma & Simon (2006) paper for a more nuanced discussion of the impact of different types of CV for parameter selection.

## Online tutorial:
**START HERE (1).** This is a big picture discussion post that is an overview over hyperparameter selection & algorithm selection with big and small data. Easy to read and very accessible: [A “short” introduction to model selection](https://towardsdatascience.com/a-short-introduction-to-model-selection-bb1bb9c73376)

## Videos:
(2) This video is a good walkthrough using K-fold cross-validation in python to select optimal tuning parameters, choose between models, and select features. Selecting the best model in scikit-learn using cross-validation
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/6dbrR-WymjI" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

(3) A short 4 minute tutorial about how to tune various types of statistical learning models within cross validation using the caret package in R. It doesn't discuss much of the theory and is more appropriate for application focused users who are just trying to figure out how to implement parameter tuning within CV.
R Tutorial - Hyperparameter tuning in caret
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/xGZVxxvgzI4" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Online tutorials (blogs and code examples):
(4) This is an R Markdown file written by the creator of the caret package in R that explains how to tune the various types of hyperparameters using CV within carets train function (very related to video 3). Even if you don’t plan to use R, it is helpful to see what types of parameters are tuned for different models and provides examples of creating and evaluating search grids, alternate performance metrics, and more. [Model training and tuning](https://topepo.github.io/caret/model-training-and-tuning.html)

(5) This is a nice (but lengthy) R Markdown example of approaching a classic machine learning problem (product price estimation) and showcases hyperparameter tuning of a couple of different algorithms (and their comparison): [Product Price Prediction: A Tidy Hyperparameter Tuning and Cross Validation Tutorial](https://www.r-bloggers.com/2020/01/product-price-prediction-a-tidy-hyperparameter-tuning-and-cross-validation-tutorial/)
This is geared towards a more advanced beginner - It still walks you through everything, but you may be lost if you don't understand the data cleaning and exploration lead up

## Paper:
(6) This paper describes the impact of using different CV types for parameter selection and model evaluation: [Bias in error estimation when using cross-validation for model selection.](https://link.springer.com/article/10.1186/1471-2105-7-91)
This requires intermediate level understanding of using CV for parameter selection. Many people using machine learning in applied contexts are using improper CV methods that bias their model performance estimates. We should be using nested CV (or bootstrap CV with a separate validation set) if we are planning to select model parameters and generate trustworthy performance metrics


{% include links.html %}
