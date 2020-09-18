---
title: Locally Linear Embeddings
tags:
  - pattern_recognition
keywords: "topic" # new keywords requiere to create a new tag file
last_updated: "June 1, 2020"
summary: Locally linear embedding is a method for computing low-dimensional embeddings of data distributed as nonlinear manifolds in the higher-dimension space
published: true
sidebar: data_reduction_sidebar #name of yml sidebar file withouth extension
permalink: lle.html
folder: data_reduction
---

{% include note.html content="Please utilize the template below as a reference for your contribution. Adapt the template when deemed necessary" %}

## What is locally-linear embedding (LLE)?

Locally-linear embedding is a method for computing low-dimensional embeddings from high-dimensional data. It is especially useful when data are distributed along nonlinear manifolds in the original high-dimensional space. Other common methods for data reduction find projections of the data onto linear components. For instance, each component of a principal component analysis corresponds to a linear plane in the original space, with the different components all orthogonal to one another. If the distribution of data is "curved" in the original space, linear embeddings can provide poor low-dimensional descriptions of the structure of the data.

Locally linear embeddings overcome this limitation by finding low-dimensional descriptions that preserve *local* similarity relations amongst data-points. That is, the linear distances from a given data point to its nearest neighbors will be similar in the embedding and the original data, but distances between more distal datapoints will be unrelated in the embedding and original space. By preserving the local similarity structure (ie distances to nearest neighbors only), the embedding can reveal structure in data that lies along nonlinear manifolds in the higher-dimensional space. Other embedding methods that likewise preserve local structure include tSNE and k-nearest-neighbor approaches.

In behavioral sciences, nonlinear data reduction methods are useful because, empirically, many naturally-occurring high-dimensional datasets appear to exhibit nonlinear structure. The perceptual structure of hand-written digits provides a canonical example; others might include understanding how information is represented in neural-network models, finding multivariate structure in functional brain images, characterizing patterns of movement in human kinematics or robotics, or decoding semantic structure in large corpora of natural text.

## Useful videos

* [Video 1](https://www.youtube.com/watch?v=scMntW3s-Wk/) explains what the Locally linear embedding method is, elaborating on how LLE preserves the total geometry of the data while reducing the dimension.

* [Video 2](https://www.youtube.com/watch?v=afkSR1Jweu8/) provides a short description of locally-linear embedding,
goes through some Python code to explain each parameter of the scikit_learn code for LLE. 

## Applied papers
* [Locally linear embedding (LLE) for MRI based Alzheimer's disease classification](https://www.sciencedirect.com/science/article/abs/pii/S1053811913006708). This paper applies LLE to extract characteristic MR features of brain alterations, then uses the embedding as input to a classifier trying to predict disease diagnosis.

* [A facial expression recognition system based on supervised locally linear embedding](https://www.sciencedirect.com/science/article/pii/S0167865505001273?casa_token=1he1OBTxw8MAAAAA:PMIphAOZqBYIRQUY4FEp1gkJwEPgTO-xBcz7yUvStqVdZuBJqqXhEII0biV2Ayy950CylS7vCw). This paper applies supervised variants of LLE to develop a system for classifying the emotional expressions on images of faces.

## Theory papers
* [An Introduction to Locally Linear Embedding](https://cs.nyu.edu/~roweis/lle/papers/lleintro.pdf). In this scientific paper, the authors  illustrated the Locally Linear Embedding method on images of lips used in audiovisual speech synthesis.

* [Nonlinear Dimensionality Reduction by Locally Linear Embedding](https://science.sciencemag.org/content/290/5500/2323). The original paper that describes Locally Linear Embedding.

## Online tutorials

* [Online tutorial 1](https://scikit-learn.org/stable/auto_examples/manifold/plot_lle_digits.html#sphx-glr-auto-examples-manifold-plot-lle-digits-py) provides Python code for computing LLEs on the MNIST dataset of handwritten digits.

* [Blog post with linked Github repo](https://towardsdatascience.com/step-by-step-signal-processing-with-machine-learning-manifold-learning-8e1bb192461c). This post compares LLE with another non-linear embedding method (isomap), applied to the MNIST dataset of hand-written digits. In addition to providing a concise overview of the central ideas, it links to a GitHub repo for experimenting with these techniques.

{% include links.html %}
