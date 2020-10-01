---
title: Kalman Filters
tags:
keywords: "topic" # new keywords requiere to create a new tag file
last_updated: "June 1, 2020"
summary: "Method for predicting the next state of a system given some uncertainty."
published: true
sidebar: time_series_sidebar #name of yml sidebar file withouth extension
permalink: kalman_filters.html
folder: kernel_methods
---


{% include note.html content="Please utilize the template below as a reference for your contribution. Adapt the template when deemed necessary" %}

## What is a Kalman Filter?

_From [this blog](http://www.bzarg.com/p/how-a-kalman-filter-works-in-pictures/)_

You can use a Kalman filter in any place where you have uncertain information about some dynamic system, and you can make an educated guess about what the system is going to do next. Even if messy reality comes along and interferes with the clean motion you guessed about, the Kalman filter will often do a very good job of figuring out what actually happened. And it can take advantage of correlations between crazy phenomena that you maybe wouldn’t have thought to exploit!

Kalman filters are ideal for systems which are continuously changing. They have the advantage that they are light on memory (they don’t need to keep any history other than the previous state), and they are very fast, making them well suited for real time problems and embedded systems.

The Kalman filter is an efficient recursive algorithm to compute a linear MMSE estimate of some unobservable system state based on observations. The recursive nature arises in that the algorithm uses previously computed estimates of the system state given a vector of observations to compute the new estimate when a new observation is available. The system state and observation state are usually a linear (time-varying) dynamical system with noise.

## Typical Uses of Kalman filters
* Navigation/control of a robot
* Prediction, filtering, and interpolation/smoothing/denoising of time series data

## Recommended Learning Path 
[How a kalman Filter works in picutures](http://www.bzarg.com/p/how-a-kalman-filter-works-in-pictures/) This blog post provides a very nice introduction to the Kalman filter (with pictures!) that is accessible to anyone. The nice thing about this blog post is that it also has derivations of the actual algorithm.


## Video courses

* This 11 minute nontechnical video discusses how the Kalman filter is used for time-series analysis.
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/RxIdLu18SsE" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


## Applied papers 
* [An Introduction to Kalman Filters](https://www.cs.unc.edu/~welch/media/pdf/kalman_intro.pdf) This is a paper deriving the Kalman filter. This essentially follows Kalman’s original 1960 paper where he proposed the Kalman filter.


## Online tutorials

* [The Kalman Filter](http://www.cs.unc.edu/~welch/kalman/index.html#Anchor-23522) This webpage has links to a bunch of code for the Kalman filter in various languages, e.g., matlab, C++, Java. You can also just implement the Kalman filter yourself in a few lines of code since it’s a fairly simple algorithm, e.g., [here’s](https://scipy-cookbook.readthedocs.io/items/KalmanFiltering.html) how to do it in Python.



{% include links.html %}
