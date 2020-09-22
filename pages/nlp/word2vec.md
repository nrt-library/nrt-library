---
title: Word2Vec
tags:
keywords: # new keywords requiere to create a new tag file
last_updated: "June 1, 2020"
summary: 
published: true
sidebar: nlp_sidebar #name of yml sidebar file withouth extension
permalink: word2vec.html
folder: nlp
---


{% include note.html content="Please utilize the template below as a reference for your contribution. Adapt the template when deemed necessary" %}

## Word2vec

Word2vec is a set of related models for creating vector representations of words. It uses a shallow, feed-forward nerural network to attempt to predict the relationship between a word and the words that most often appear with it, based on a set a corpus of text, provided as input. You can either ask word2Vec to learn how to predict a target word, based on a given context (Continuous Bag of Words) or predict which words are most likely to be the context for a given word (Skip-gram).  For each word, word2vec will output a vector containing the weights of the hidden layer that were learned for that word. Each word (as represented by its vector), can be thought of as occupying a given position, along with all other words, in an n-dimensional space, where n=the number of hidden units or features in the hidden layer.
 
Because this process results in each word's vector being located in a semantic space that's shared with all of the other words in the training set, one can then ask, given the training set I provided, how is the resulting space organized? Which words are most similar to others? 
 
Word2vec is not among the most sophisticated or state-of-the-art language models, but it is relatively accessible, intuitive, computationally inexpensive, and is somewhat responsive to smaller training materials/corpora.

## List of ideas/topics associated with this topic
* Word Embeddings
* [Natural Language Processing](nlp_landing_page.html)
* [Neural Networks] (neural_networks_landing_page.html)
* [Semantic Vectors](semantic_vectors.html)


## Understanding Word2vec

### Video

* [This video](https://www.youtube.com/watch?v=QyrUentbkvw), by Joran Boyd-Graber (U of Maryland Computer Science), gives an explanation of word2vec, how it works, and some of the situations in which it might be useful
Understanding Word2Vec

* Video 2

### Online tutorials

* [Basic (in R)](https://github.com/bmschmidt/wordVectors) 
A simple, hands on, introduction to word2vec in R. It provides access to a training corpus (cookbooks!) and demonstrates some ways to interrogate the semantic space that results.

* [More in-depth (python)](https://www.kaggle.com/pierremegret/gensim-word2vec-tutorial)
This tutorial is a bit more hands on, with some of the steps that were automated for you in the prior tutorial are now executed by you, via code snippets

* [In-depth/crunchy](https://towardsdatascience.com/an-implementation-guide-to-word2vec-using-numpy-and-google-sheets-13445eebd281)
This tutorial might be useful if you'd like to see how word2vec works - a much more in depth way get acquainted, using numpy and google sheets


### Theory papers 
* Initial word2vec paper - [Mikolov et al., 2013](https://arxiv.org/abs/1301.3781)
* [This chapter on word vectors and embeddings](https://web.stanford.edu/~jurafsky/slp3/6.pdf) offers a good foundation on word2vec and some of the principles on which it is based. It's from Dan Jurafsky and James Martin's book (draft) Speech and Language Processing.

{% include links.html %}
