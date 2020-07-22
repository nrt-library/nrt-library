---
title: Support Vector Machines
tags:
  - pattern_recognition
keywords: "topic" # new keywords requiere to create a new tag file
last_updated: "June 1, 2020"
summary: "Support vector machines are a specific instance of kernel-methods used for data classification."
published: true
sidebar: pattern_classification_sidebar #name of yml sidebar file withouth extension
permalink: support_vector_machines.html
folder: pattern_classification
---


## Framing

Support Vector Machines (SVMs) deal with a fundamentally simple problem – how does one divide up data points using some form of meaningful decision boundary in a supervised learning setting?

This approach gets its name from support vectors, a subset of the labeled data points whose dot products help in determining the decision boundary. The decision boundary is arranged such that the distance between these support vectors, or the *margin width* is maximized.  

<img src= "pages/pattern_classification/svm.png" style="max-width: 400px;"/>

In contrast to approaches like *simple* neural networks or least-squares classifiers SVMs have 3 distinct features that are important to consider together:

1. 	They do not get stuck in local minima. If the data are linearly separable, the algorithm will always find the same ‘best’ decision boundary

2. 	If the data aren’t linearly separable, the SVM approach supports a transformation of the data into some higher dimensional space where the data are linearly separable. The approach is supported because mathematically, computing the decision boundary comes down to simply computing the dot products between pairs of vectors. The materials below go into more depth about this point.

3. Additionally, there often exist *kernel functions* that help us know the dot product of vectors in the high dimensional space as a function of the pair in the original space. This makes it even easier to compute the dot product and consequently the decision boundary!
This is what’s known as the ‘kernel-trick’ in SVMs.

SVMs are a great tool to use when you don't have large datasets, which neural networks usually require, and some non-trivial decision boundary between data points.
It is easiest to use SVMs as binary classifiers, though it is possible to generalize to multinomial cases with some modifications.

## Recommended Path for Learning

### Videos


<!--* <a href="https://www.youtube.com/watch?v=_PwhiWxHK8o" target="_blank">Patrick Winston’s lecture on SVMs is one of the easiest to follow and assumes a very minimal background in linear algebra and multivariable calculus.</a>-->

* Patrick Winston’s lecture on SVMs is one of the easiest to follow and assumes a very minimal background in linear algebra and multivariable calculus.
<iframe width="560" height="315" src="https://www.youtube.com/embed/_PwhiWxHK8o" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>



* One might like Andrew Ng’s lecture on the same from 2018, which is a bit more recent, but SVMs haven’t changed much over the past decade (begins at 46:22). 
<iframe width="560" height="315" src="https://www.youtube.com/embed/lDwow4aOrtg" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


### Code Implementations

* To get a stronger grasp on the mathematics behind SVMs and do some ‘hands-on’ work with them we recommend this site:
<a href="https://www.svm-tutorial.com/" target="_blank">Welcome to SVM tutorial - SVM Tutorial</a>. 

There are sections that detail different mathematical tools that SVMs employ and there’s a nice R tutorial on doing text-classification using SVMs.
 
* A python based implementation of SVM using scikit-learn:
<a href="https://stackabuse.com/implementing-svm-and-kernel-svm-with-pythons-scikit-learn/" target="_blank"> Implementing SVM and Kernel SVM with Python's Scikit-Learn.</a>
 
 
Here’s another jupyter notebook based python implementation of SVMs using scikit-learn:
<a href="https://www.learnopencv.com/svm-using-scikit-learn-in-python/" target="_blank">SVM using Scikit-Learn in Python.</a>

### Blogs & Articles

Here are 2 papers that employ SVMs in NLP and cognitive neuroscience settings:
* <a href="https://www.aclweb.org/anthology/N04-1030/" target="_blank">Shallow Semantic Parsing using Support Vector Machines.</a>
 
* <a href="https://www.ncbi.nlm.nih.gov/pubmed/20112242" target="_blank">Effective functional mapping of fMRI data with support-vector machines.</a>


{% include links.html %}
