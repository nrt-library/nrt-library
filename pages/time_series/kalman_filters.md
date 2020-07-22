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

## What is TOPIC-NAME?

_From [this blog](http://www.bzarg.com/p/how-a-kalman-filter-works-in-pictures/)_

You can use a Kalman filter in any place where you have uncertain information about some dynamic system, and you can make an educated guess about what the system is going to do next. Even if messy reality comes along and interferes with the clean motion you guessed about, the Kalman filter will often do a very good job of figuring out what actually happened. And it can take advantage of correlations between crazy phenomena that you maybe wouldn’t have thought to exploit!

Kalman filters are ideal for systems which are continuously changing. They have the advantage that they are light on memory (they don’t need to keep any history other than the previous state), and they are very fast, making them well suited for real time problems and embedded systems.

## Video courses

* Video 1
* Video 2

## Applied papers 
* Paper 1
* Paper 2

## Online tutorials

* Online tutorial 1
* Online tutorial 2

## Theory papers 
* Paper 1
* Paper 2

{% include links.html %}
