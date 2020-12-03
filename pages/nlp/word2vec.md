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
* [Neural Networks](neural_networks_landing_page.html)
* [Semantic Vectors](semantic_vectors.html)


## Understanding Word2vec

### Video

- This introduction by Jordan Boyd-Graber (U of Maryland Computer Science), gives an explanation of word2vec, how it works, and some of the situations in which it might be useful
<iframe width="560" height="315" src="https://www.youtube.com/embed/QyrUentbkvw" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>



### Online tutorials

* <a href="https://github.com/bmschmidt/wordVectors" target="_blank"> Basic in R.</a> A simple, hands on, introduction to word2vec in R. It provides access to a training corpus (cookbooks!) and demonstrates some ways to interrogate the semantic space that results. 

* <a href="https://www.kaggle.com/pierremegret/gensim-word2vec-tutorial" target="_blank"> A little more in depth (python).</a> 
This tutorial is a bit more hands on, with some of the steps that were automated for you in the prior tutorial are now executed by you, via code snippets

* <a href="https://derekchia.com/an-implementation-guide-to-word2vec-using-numpy-and-google-sheets/" target="_blank"> In depth/crunchy.</a> This tutorial uses numpy and google sheets to look more closely at how w2v works


### Theory papers 
* <a href="https://arxiv.org/abs/1301.3781" target="_blank"> Efficient Estimation of Word Representations in Vector Space - Mikolov et al., 2013</a>

*  <a href="https://arxiv.org/abs/1310.4546" target="_blank"> Distributed Representations of Words and Phrases and Their Compositionality - Mikolov et al., 2013</a> 

* <a href="https://web.stanford.edu/~jurafsky/slp3/6.pdf" target="_blank"> This chapter on word vectors and embeddings offers a good foundation on word2vec and some of the principles on which it is based - from Dan Jurafsky and James Martin's book (draft) Speech and Language Processing. </a> 

### Applied papers

* <a href="https://psyarxiv.com/7qd3g" target="_blank"> Gender Stereotypes are Reflected in the Distributional Structure of 25 Languages - Lewis & Lupyan, 2020</a> 

* <a href="http://journals.sagepub.com/doi/abs/10.1177/1745691619861372" target="_blank"> Vector Space Models of Semantic Representation from a Cognitive Perspective - Gunther et al., 2019</a>


{% include links.html %}
