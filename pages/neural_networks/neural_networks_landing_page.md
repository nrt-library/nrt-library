---
title: Neural Networks
tags:
  - getting_started
keywords: "topic" # new keywords requiere to create a new tag file
last_updated: "August 7, 2020"
summary: "Neural networks refer to a broad class of algorithms that used to represent learning in supervised as well as unsupervised contexts"
published: true
sidebar: neural_networks_sidebar #name of yml sidebar file withouth extension
permalink: neural_networks_landing_page.html
folder: neural_networks
---

## What are neural networks?

At the most abstract level, neural networks (a.k.a. *Deep Learning*) are **an approach to the study and simulation of intelligent systems**. 

In the context of **machine learning**, neural networks are a class of models that search for solutions to problems in an *iterative* and *distributed* fashion, and with as little human intervention as possible. The core principle is that solutions can be found by exposing complex arrangements of simple processing units to data related to the problem at hand. Such units are the so-called neurons, which are connected in sequences of layers. This type of system is flexible and powerful and can be used to tackle supervised, unsupervised, semi-supervised, and reinforcement learning tasks. 

For **cognitive science**, neural networks have a similar meaning that for machine learning. Here, neural networks refer to **an approach to the study of cognition and behavior** that propose that **intelligence emerges from the collective action of billions of connected and interactive processing units**, i.e., neurons and synapses. Such an approach is sometimes called **connectionism**. The principle guiding neural networks models of cognition is that knowledge and mental activity are better represented as d**istributed patterns of neural activation**. For instance, memory, language, and reasoning would be an emergent property from a complex dynamical system which is the human brain. The neural network approach contrast with symbolic and modular approaches to the study of the mind and behavior. 

## Brief history

 In 1943, Warren McCulloch and Walter Pitts published "*A logical calculus of the ideas immanent in nervous activity*", introducing what is considered the first computational model of an artificial neuron. The next well-known neural network model was the "*Perceptron*", introduced by Frank Rosenblatt in 1958. One of the main differences between the McCulloch-Pitts' and Rosenblatt's architectures was that Rosenblatt's model incorporated a **learning algorithm**, that allowed the network to adjust its parameters to make better predictions over time. The learning part was of crucial importance for later developments in the field because it enabled the possibility of creating artificial systems capable of **discovering solutions** instead of forcing humans to figure out the solution beforehand, to just then building the solution into the system. 

 The research on neural networks stall after that in 1969, **Marvin Minsky** and **Seymour Papert** famously demonstrated that Rosenblatt's perceptron wasn't able to learn simple patterns like the *exclusive-or (XOR) rule*, which had a devastating effect on the academic interest on artificial neural networks. Nonetheless, several researchers continued to pursue this line of thinking. In particular, a group of researchers led by **David Rumelhart** and **James McClelland**, the so-called "*Parallel Distributed Processing Research Group*" (PDP research group), would work together exploring the implications of neural network models for the understanding of human intelligence. Their work would be crystallized in a two volumes book titled "**Parallel Distributed Processing: Explorations in the Microstructure of Cognition**". The PDP research group work would help to revitalize the interest in neural network models of cognition in the 80s. In particular, the introduction of today's well-known "**backpropagation** algorithm" by **Rumelhart**, **Hinton**, and **Williams**, would be the key to overcome Minsky and Papert's criticism. 

 Fast forward to the present, neural networks have become one of the most active areas of research in the machine learning and cognitive science community under the rubric of **Deep Learning**. Recent achievements like the [DeepMind's AlphaGo](https://deepmind.com/research/case-studies/alphago-the-story-so-far) that beat the at the time best Go player in the world, the 9-dan Lee Sedol, and OpenAI's 175 billion parameter language model [GPT-3](https://www.technologyreview.com/2020/07/20/1005454/openai-machine-learning-language-generator-gpt-3-nlp/), have made headlines around the globe and captured the attention of public and private section alike. In the image below you can find a timeline summarizing the evolution of neural networks from their inception until today:

 ![neural-net](images/roadmap.svg)


## Basic elements of a neural network

The basic components of neural networks are **units** (neurons), **connections** (synapses), and **layers**. The image below illustrates one of the simplest neural networks: **the multilayer perceptron**. This example consists of two input units, three hidden units, and one output unit. All neurons are said to be **fully-connected** when every neuron is connected to every other neuron in a forward fashion. 

![neural-net](images/forward-pass.svg)

Some authors would say this network has two layers while others three, depending on whether you count the input layers as a layer. In general, networks have three types of layers: *input*, *hidden*, and *output*. Input layers that take input data for training, hidden layers where the learning actually happens, and output layers to get the results from training. 

## Recommended Path for Learning

- [Chapter 1: "Introduction" in *Deep Learning* by Goodfellow, Bengio, and Courville](https://www.deeplearningbook.org/contents/intro.html)

- **But what is a Neural Network? - Deep learning, chapter 1**
<iframe width="560" height="315" src="https://www.youtube.com/embed/aircAruvnKk" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

- [Chapter 1: "The Appeal of Parallel Distributed Processing" in *Parallel distributed processing: Explorations in the microstructure of cognition*. Volume I. by McClelland, Rumelhart, and Hinton](https://stanford.edu/~jlmcc/papers/PDP/Chapter1.pdf)

## Video courses

- **Neural Networks for Machine Learning by Geoffrey Hinton**

<iframe width="560" height="315" src="https://www.youtube.com/embed/OVwEeSsSCHE" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

- **MIT Introduction to Deep Learning | 6.S191**

<iframe width="560" height="315" src="https://www.youtube.com/embed/njKP3FqW3Sk" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

- **Neural Networks series by 3Blue1Brown**

<iframe width="560" height="315" src="https://www.youtube.com/embed/aircAruvnKk" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Applied papers 

- [Elman, J. L. (1990). Finding structure in time. Cognitive science, 14(2), 179-211.](https://onlinelibrary.wiley.com/doi/pdf/10.1207/s15516709cog1402_1)
- [LeCun, Y., Bottou, L., Bengio, Y., & Haffner, P. (1998). Gradient-based learning applied to document recognition. Proceedings of the IEEE, 86(11), 2278-2324.](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=726791&casa_token=6wyLjmRwb9UAAAAA:asALm4lyfFI5oFQKOiT0WIVoAyASMHhwY3oVG8zdMJiEYqKLXENTpTIofgE-Ir5WZpyW3xUksGao&tag=1)
- [Silver, D., Schrittwieser, J., Simonyan, K., Antonoglou, I., Huang, A., Guez, A., ... & Chen, Y. (2017). Mastering the game of go without human knowledge. nature, 550(7676), 354-359.](https://www.nature.com/articles/nature24270.)

## Online tutorials and books

- [Dive into Deep Learning Book](https://d2l.ai/)
- [Deep Learning Book](https://www.deeplearningbook.org/)
- [Introduction to Neural Networks Models of Cognition - Interactive Book](https://com-cog-book.github.io/com-cog-book/intro.html)

## Theory papers 

- [Thomas, M. S., & McClelland, J. L. (2008). Connectionist models of cognition. The Cambridge handbook of computational psychology, 23-58.](https://neuro.bstu.by/my/Tmp/2010-S-abeno/Papers-3/Is-AI-intelligent/McClelland/ThomasMcCIPCambEncy.pdf)

- [LeCun, Y., Bengio, Y., & Hinton, G. (2015). Deep learning. nature, 521(7553), 436-444.](https://www.nature.com/articles/nature14539)

- [McClelland, J. L., Botvinick, M. M., Noelle, D. C., Plaut, D. C., Rogers, T. T., Seidenberg, M. S., & Smith, L. B. (2010). Letting structure emerge: connectionist and dynamical systems approaches to cognition. Trends in cognitive sciences, 14(8), 348-356.](https://www.sciencedirect.com/science/article/pii/S1364661310001245?casa_token=vK6Y7A7C1ToAAAAA:-AedyDeRnQ426tbn6PCNmdSayEXrou0Hk5I-pO26wpkbQGRgmqew7BJZDm8xGv2zvdMoHmmxhHQw)

## Contributors

- [Pablo Caceres](mydoc_about.html#pablocaceres) 

{% include links.html %}