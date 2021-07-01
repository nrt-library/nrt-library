---
title: Elastic Net Regression
tags:
keywords: "topic" # new keywords requiere to create a new tag file
last_updated: "July 1, 2021"
summary: "Elastic net regression is a method of regularization for fitting linear and logistic models using a combination of L1 and L2 penalties"
published: true
sidebar: model_fitting_sidebar #name of yml sidebar file withouth extension
permalink: elastic_nets.html
folder: model_fitting
---


{% include note.html content="Please utilize the template below as a reference for your contribution. Adapt the template when deemed necessary" %}

## What is elastic net regression?

Elastic net regression is a method of regularization for fitting linear and logistic models using a combination of ridge and lasso methods to penalize the models. Regularization complements machine learning models that may have large numbers of predictors or correlated predictors which result in more variance in the model. By penalizing the model, elastic net introduces some bias which can make the model more generalizable to new data (i.e., lower variance) and reduce overfitting. Ridge regression penalizes the sum of squared coefficients  (L2) and lasso regression penalizes the sum of absolute values of the coefficients (L1). Elastic net combines these two types of penalties to find a good variance-bias tradeoff for the model. The optimal size of the penalty for a model can be determined via tuning parameters with cross-validation.   


## Recommended Path for Learning

**Bias, variance, and overfitting**    
* Machine learning fundamentals of bias-variance tradeoff    
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/EuBBz3bI-aA" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

* The problem of overfitting    
* Machine learning fundamentals of bias-variance tradeoff
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/u73PU6Qwl1I" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

**Types of regularization**   
\* Ridge regression: variables with minor contribution have their coefficients close to zero. However, all the variables are incorporated in the model. This is useful when all variables need to be incorporated in the model according to domain knowledge.    
Regularization Part 1: Ridge Regression
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/Q81RR3yKn30" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

\* Lasso regression: the coefficients of some less contributive variables are forced to be exactly zero. Only the most significant variables are kept in the final model.   
Regularization Part 2: Lasso Regression
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/NGf0voTMlcs" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

\* Elastic net regression: the combination of ridge and lasso regression. It shrinks some coefficients toward zero (like ridge regression) and set some coefficients to exactly zero (like lasso regression).   
Regularization Part 3: Elastic Net Regression
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/1dKRdX9bfIo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

**Apply elastic net regression**    
* Introduction to the {tidymodels} Machine Learning Ecosystem   
<a href="https://dnield.com/posts/tidymodels-intro/" target="_blank">Demo of lasso and elasticnet regression</a>  

* Tidy modeling in R documentation   
<a href="https://www.tmwr.org/" target="_blank">Tidy modeling</a>


## Further Learning

## Applied papers 

* Badger, LaRose, Mayer, Bashiri, Page, & Peissig 2019. “Machine learning for phenotyping opioid overdose events.” J Biomed Inform 94. <a href="https://pubmed.ncbi.nlm.nih.gov/31028874/" target="_blank">Pubmed</a>      

## Online tutorials

* Tidymodels for lasso, ridge, and elastic net regression in r  
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/huIGJaokKgM" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>    

* Fitting an elastic net model in R tutorial   
<a href="https://asmquantmacro.com/2016/04/26/fitting-elastic-net-model-in-r/" target="_blank">Fitting elastic net</a>  

* Video overview of how to implement elastic net, lasso, and ridge regression in R without using tidymodels    
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/ctmNq7FgbvI" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


## Theory papers 
* Yarkoni & Westfall. 2017. “Choosing Prediction Over Explanation in Psychology: Lessons From Machine Learning.” Perspectives on Psychological Science 12 (6): 1100–1122. <a href="https://pubmed.ncbi.nlm.nih.gov/28841086" target="_blank">Pubmed</a>    


## Text resources
* James, Witten, Hastie, & Tibshirani. 2013. An Introduction to Statistical Learning: With Applications in R. 8th ed. Springer Texts in Statistics. New York: Springer-Verlag.<a href="https://static1.squarespace.com/static/5ff2adbe3fe4fe33db902812/t/6009dd9fa7bc363aa822d2c7/1611259312432/ISLR+Seventh+Printing.pdf" class="uri">pdf</a>    
    
* Kuhn, & Johnson. 2018. Applied Predictive Modeling. 1st ed. 2013, Corr. 2nd printing 2018 edition. New York: Springer.  <a href="https://vuquangnguyen2016.files.wordpress.com/2018/03/applied-predictive-modeling-max-kuhn-kjell-johnson_1518.pdf" class="uri">pdf</a>    

{% include links.html %}
