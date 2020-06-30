---
title: Kernel Methods in Pattern Recognition
tags:
  - getting_started
keywords: "topic" # new keywords requiere to create a new tag file
last_updated: "June 1, 2020"
summary: "Kernel methods refer to a class of algorithms for pattern recognition where data points in the native representation space are mapped to higher dimensions using a 'kernel function' without actually computing the coordinates in the higher dimensions."
published: true
sidebar: kernel_methods_sidebar #name of yml sidebar file withouth extension
permalink: kernel_methods_landing_page.html
folder: kernel_methods
---

## What are Kernel methods?

Kernel methods are a class of algorithms used for data classification and pattern analysis in general. They became popular in the 1990s due to the **support vector machine**, a special instance of kernel-based algorithms that performed at par with neural networks at the time.
They continue to be powerful machine learning algorithms that are capable of finding decision boundaries in data that initially appear to have no clear decision boundary.

## When are they useful?

Kernel methods are especially useful for classification problems with nonlinear decision boundaries in the native data space. The specialty of kernel-based methdods lie in their use of **kernel functions**, special functions that map the raw data points into a higher dimensional vector space through the inner products of the data points in the transformed space. That is, data points that are **linearly inseparable** in the native feature space are mapped to a higher dimension space where they may be linearly separable. A further advantage of this approach is that it is computationally efficient: the explicit coordinates of all data points in the higher dimensional space do not need to be computed. Instead the kernel function directly specifies the inner products (or pairwise distance) of the points in the transformed space.

## Kernel methods topics

You can explore kernel methods topics in the sidebar menu on the left, or in the table of contents below:

* [Support Vector Machines][support_vector_machines]
* [Topic 2][topic_2]
* [Refresh][kernel_methods_landing_page]


{% include links.html %}
