---
title: Linear Mixed Effects Models
tags:
keywords: "topic" # new keywords requiere to create a new tag file
last_updated: "June 1, 2020"
summary: 
published: true
sidebar: model_fitting_sidebar #name of yml sidebar file withouth extension
permalink: lmem.html
folder: model_fitting
---


{% include note.html content="Please utilize the template below as a reference for your contribution. Adapt the template when deemed necessary" %}

## Framing

Mixed linear models are a type of analysis used to evaluate data with non-independence that cannot otherwise be analyzed with regular linear regression.
        
#### What is non-independence/non-independent data?
Non-independence occurs when two or more data are connected (correlated) in some way. For example, you run an experiment collecting ratings on interest in math. Your participants make these ratings at the start of the semester and then again at the end of the semester. Each of these participants has two data points on for each rating. These pairs of data points are non-independent since they come from the same person and thus are related in ways beyond the experimental procedure (i.e. two points from one participant are more likely to be more similar to each other than two data points from two different participants). 

Non-independence can exist beyond repeated measures at the participant level to any items occurring within “units”, including students in classrooms, family members, etc. Mixed linear models treat these units as factors and include their effects in the model. 
        	
#### Why/when should I use mixed linear models?
Using regular linear regression when data is non-independent can lead to inflated Type 1 error rates, less statistical power, and potentially inaccurate effects. A mixed linear model should be used anytime there is a non-independent relationship in the data.
 
## Recommended path for learning:
Start with watching a few of the videos from the multi-part series to get an idea of what linear mixed effects models are and when you would use them. Learners then may want to read through one of the online tutorials and carry out the exercises in R or Python  Learners with experience coding in R might go to the first online tutorial. Learners with little experience in R/python might first go to the second tutorial, which provides some more general R instruction, or visit the pages on these coding languages. 

### Videos

A [multi-part series](https://www.youtube.com/watch?v=9iKgS0HeeOg&list=PLbyRmcun-giuz5hW11nD64zeiJZSDV4aD&index=1) reviewing what mixed models are, their benefits, and a few examples. Videos 1-3, 11, and 16 are good places to start if not wanting to go through the entire series. 1-3 provide short backgrounds/high level overviews. 11 describes repeated measures models, which are very common in psychology/cognitive science research. 16 gives a short overview of what these models mean and how to interpret them.

A high level [video](https://www.youtube.com/watch?v=Vfr3d1NIppU) overview of mixed models (mostly framed in terms of hierarchical models). The first half of the video describes when/why someone would use these models. The second half starts to touch into the equations/math for these models. 

### Online tutorials

[Website/post](https://ourcodingclub.github.io/tutorials/mixed-models/) providing a walkthrough style tutorial of basic linear mixed effects models in R. Includes code and the output, with descriptions of why/how to go about running these models. 

A [Github repo](https://github.com/singmann/mixed_model_workshop_2day) with a 3-part workshop aimed at providing tutorials and exercises to learn how to do mixed models in R. The first part is a general intro to R. The second part is about statistical modeling (generally) in R. Then part 3 is mixed models in R. 
 
A similar [tutorial](https://jbhender.github.io/Stats506/F18/GP/Group16.html) demonstrating mixed models in both R and Python.

### Papers 
This [paper](https://psycnet.apa.org/record/2017-52405-001) provides guidelines for how to create linear mixed effects models, including steps on how to decide what random effects to include and how to address convergence issues with a large number of parameters.

### Additional resources 
A very short [cheat sheet](https://rstudio-pubs-static.s3.amazonaws.com/63556_e35cc7e2dfb54a5bb551f3fa4b3ec4ae.html) of using the lme4 package in R to analyze mixed models. 

Jake Westfall, a former quantitative psychologist that now works in data science/analytics in industry, has curated a [list](http://jakewestfall.org/blog/index.php/2015/06/20/reading-list-introduction-to-linear-mixed-models-for-cognitive-scientists/) of 13 helpful readings on mixed linear models.


{% include links.html %}
