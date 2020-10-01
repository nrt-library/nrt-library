---
title: Spectral Clustering
tags:
  - pattern_recognition
keywords: "topic" # new keywords requiere to create a new tag file
last_updated: "June 1, 2020"
summary: 
published: true
sidebar: data_reduction_sidebar #name of yml sidebar file withouth extension
permalink: spectralcluster.html
folder: data_reduction
---


{% include note.html content="Please utilize the template below as a reference for your contribution. Adapt the template when deemed necessary" %}

## What is a Spectral Clustering?

Spectral clustering is a family of methods by which one can find clusters in a data set, which is under the umbrella of unsupervised learning. 
The rough structure of what spectral clustering does on a given data set is three parts. 

Step 1: Define some sort of geometry/distance/similarity score between elements of your data set.  
Step 2:  Capture "important" information of the metric and use it to transform your data to new "spectral" coordinates. (This is like pca, but using eigenvectors of a different matrix, (a graph Laplacian) instead of the covariance matrix.)
Step 3: Perform another clustering method such as K-means on the transformed data set. It may do a much better job than clustering on the original data set.

## Recommended knowledge before starting:

To understand what it does, one needs to understand linear algebra enough to be familiar with eigenvectors and eigenvalues.  It also helps to have at least some understanding of graphs and networks, as the methods constructs a graph on your data set and uses the graph’s properties to cluster find a space on which custering will be (hopefully) more effective.

## How does one do it?

**Step 1:**  Define a similarity graph on your data set. Here one basically decides how "close" any two elements are to each other, or instead how much they "communicate" with one another. 
This information is recorded in a matrix where the closeness between two elements i,j in a data set are stored as the (i,j) entry in what we call the similarity matrix. This induces a graph over a data set where similar elements are connected to one another.
 
This similarity can be binary, where  two elements either  are connected/communicate/are similar:  1, 
or are not connected/don't communicate/aren't similar: 0.  The result is an unweighted adjacency matrix on the data set.
Or, this can be weighted by how close any two elements are, or how much they communicate,etc.  Usually one wants these weights to be non-negative There are many different standard kinds of similarity matrices one can form from the same data, and all affect the result one achieves.  These are discussed in the Luxburg reference below.
 
**Step 2 a:**  From the similarity matrix defined in step 1, we form the graph Laplacian by subtracting the similarity matrix from a diagonal matrix where the elements on the diagonal are the total weight of edges out of the corresponding data element. There are also variants of how exactly the Laplacian is constructed as it can be normalized in different ways. It also has different meanings based on which kind of similarity matrix was used.
 
**Step 2 b:** Pick some k. Compute the top k  eigenvectors of the graph Laplacian from 2a, you now have a spectral embedding of your data as the rows of these k columns.  This is analogous to the projection done in pca. Except here instead of using the spectrum of the covariance matrix on your data, we use the spectrum of the graph Laplacian matrix.  How to pick a good k is discussed in the blogpost and pdf below.
 
**Step 3:** Cluster the rows of your eigenvectors using any clustering method (usually done with k-means). Each row corresponds to an element of your data set, so now you have clusters in a spectral embedding which can be quite effective.
 
## Resources 
All of these resources roughly assume the reader is at least somewhat familiar with linear algebra as far as being aware that eigenvectors and eigenvalues are things. They go into varying levels of detail about them.
 
 
## Applied Paper
[Spectral graph clustering and optimal number of clusters estimation: An overview of spectral graph clustering and a python implementation of the eigengap heuristic by Madalina Ciortan:](https://towardsdatascience.com/spectral-graph-clustering-and-optimal-number-of-clusters-estimation-32704189afbe)
This is a short, low key guide with a description of spectral clustering and implementaion via code examples in python. It references the Luxburg tutorial and some papers for more information. The post "explains the functioning of the spectral graph clustering algorithm, then it looks at a variant named self tuned graph clustering." There are also references to recent papers and application papers in this post.

 
## Theory Paper
[A Tutorial on Spectral Clustering by Ulrike von Luxburg:](https://www.cs.cmu.edu/~aarti/Class/10701/readings/Luxburg06_TR.pdf)
An informative description in a 26 page pdf of what it is, why it works (or doesn't work) and several viewpoints on how to tune the parameters from a mathier perspective. There are also references to the main papers and books on this method with ways to dive deeper on the theory side of this method. 

 
## Videos 
An Implementation Video. This is a 4 minute run through of a python spectral clustering implementation on YouTube.

Spectral Clustering from the Scratch using Python by Ardian Umam:
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/Z10BXWPFnas" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
 
A Spectral Theory Video. In general there's lots of good information here, but it's a little more technical. It's supposed to be aimed at a general scientific audience, and I think overall it's pretty good about that, but there can be some confusing parts if it's one’s first time seeing some of it. This talk has a random walk/heat flow visualization and some description of the eigengap properties of Graph Laplacians and what those mean about a data set. It's more about spectral graph theory in general, though the end does talk specifically about clustering.

The Unreasonable Effectiveness of Spectral Graph Theory: A Confluence of Algorithms, Geometry, and Physics by James R. Lee:

<iframe width="560" height="315" src="https://www.youtube.com/embed/8XJes6XFjxM?start=1794" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


{% include links.html %}
