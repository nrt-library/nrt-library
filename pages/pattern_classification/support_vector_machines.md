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

Support Vector Machines (SVMs) deal with a fundamentally simple problem – how does one divide up data points using some form of meaningful decision boundary in a supervised learning setting? They fall under a broader class of methods known as *Kernel Methods*.

### What are Kernel methods?

Kernel methods are a class of algorithms used for data classification and pattern analysis in general. They became popular in the 1990s specifically to the **support vector machine**, a special instance of kernel-based algorithms that performed at par with neural networks at the time.
<!--They continue to be powerful machine learning algorithms that are capable of finding decision boundaries in data that initially appear to have no clear decision boundary.-->

### When are they useful?

Kernel methods are especially useful for classification problems with nonlinear decision boundaries in the native data space. The specialty of kernel-based methdods lie in their use of **kernel functions**, special functions that map the raw data points into a higher dimensional vector space through the inner products of the data points in the transformed space. That is, data points belonging to classes that are **linearly inseparable** in the native feature space are mapped to a higher dimension space where they may be linearly separable. A further advantage of this approach is that it is computationally efficient: the explicit coordinates of all data points in the higher dimensional space do not need to be computed. Instead the kernel function directly specifies the inner products (or pairwise distances) of the points in the transformed space.

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


<!--* <a href="https://www.youtube.com/watch?v=_PwhiWxHK8o" target="_blank">Patrick Winston’s lecture on SVMs is one of the easiest to follow and assumes a very minimal background in linear algebra and multivariable calculus.</a>-->

* Patrick Winston’s lecture on SVMs is one of the easiest to follow and assumes a very minimal background in linear algebra and multivariable calculus.
<iframe width="560" height="315" src="https://www.youtube.com/embed/_PwhiWxHK8o" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

* To get a stronger grasp on the mathematics behind SVMs and do some ‘hands-on’ work with them we recommend this site:
<a href="https://www.svm-tutorial.com/" target="_blank">Welcome to SVM tutorial - SVM Tutorial</a>.  

There are sections that detail different mathematical tools that SVMs employ and there’s a nice R tutorial on doing text-classification using SVMs.

## Further Learning

### Videos

* One might like Andrew Ng’s lecture on the same from 2018, which is a bit more recent, but SVMs haven’t changed much over the past decade (begins at 46:22). 
<iframe width="560" height="315" src="https://www.youtube.com/embed/lDwow4aOrtg" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


### Code Implementations
 
* A python based implementation of SVM using scikit-learn:
<a href="https://stackabuse.com/implementing-svm-and-kernel-svm-with-pythons-scikit-learn/" target="_blank"> Implementing SVM and Kernel SVM with Python's Scikit-Learn.</a>
 
Here’s another jupyter notebook based python implementation of SVMs using scikit-learn:
<a href="https://www.learnopencv.com/svm-using-scikit-learn-in-python/" target="_blank">SVM using Scikit-Learn in Python.</a>

### Blogs & Articles

Here are 2 papers that employ SVMs in NLP and cognitive neuroscience settings:
* <a href="https://www.aclweb.org/anthology/N04-1030/" target="_blank">Shallow Semantic Parsing using Support Vector Machines.</a>
 
* <a href="https://www.ncbi.nlm.nih.gov/pubmed/20112242" target="_blank">Effective functional mapping of fMRI data with support-vector machines.</a>


{% include links.html %}
