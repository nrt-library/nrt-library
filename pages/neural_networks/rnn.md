---
title: Recurrent Neural Networks
tags:
keywords: "topic" # new keywords requiere to create a new tag file
last_updated: "August 13, 2020"
summary: "A type of neural networks designed to approach time-dependent and/or sequence-dependent problems"
published: true
sidebar: neural_networks_sidebar #name of yml sidebar file withouth extension
permalink: rnn.html
folder: neural_networks
---

## What are Recurrent Neural Networks (RNN)?

 Recurrent Neural Networks (RNNs) are a type of neural networks designed to approach **time-dependent** and/or **sequence-dependent** problems. RNN are "recurrent" in the sense that they can **revisit or reuse past states as inputs to predict the next or future states**. To put it plainly, they have **memory**. Indeed, memory is what allows us to incorporate our past thoughts and behaviors into our future thoughts and behaviors. 

 The first successful example of a RNN with backpropagation was introduced by [Jeffrey Elman](https://en.wikipedia.org/wiki/Jeffrey_Elman), the so-called Elman Network (Elman, 1990). Since the Elman network, outstanding progress has been made with RNN in both basic research and practical applications. RNNs today are used for tasks like machine translation, robotics, speech recognition, speech production, time series prediction, sequential decision making, modeling of brain activity, and many more. 
 
## Recommended Path for Learning

- [Understanding LSTM Networks](https://colah.github.io/posts/2015-08-Understanding-LSTMs/)
- **Modeling sequences: A brief overview - Lecture by Geoffrey Hinton (47 min)**   
<iframe width="560" height="315" src="https://www.youtube.com/embed/9T2X6WRUwFU" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

- [The Recurrent Neural Network in introduction to Neural Networks Models of Cognition - Interactive Book by Pablo Caceres](https://com-cog-book.github.io/com-cog-book/features/recurrent-net.html)

## Further Learning

## Video

- **Recurrent Neural Networks - MIT 6.S191**
<iframe width="560" height="315" src="https://www.youtube.com/embed/SEnXr6v2ifU" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

- [CS224n: Natural Language Processing with Deep Learning - Stanford / Winter 2020](http://web.stanford.edu/class/cs224n/index.html#schedule)
- [Bhiksha Raj's Deep Learning Lectures 13, 14, and 15 at Carnegie Mellon University](http://deeplearning.cs.cmu.edu/F20/index.html)

## Applied papers 

- [Botvinick, M., & Plaut, D. C. (2004). Doing without schema hierarchies: A recurrent connectionist approach to normal and impaired routine sequential action. Psychological Review, 111(2), 395](http://www.cnbc.cmu.edu/~plaut/papers/pdf/BotvinickPlaut04PR.seq-action.pdf).
- [Güçlü, U., & van Gerven, M. A. (2017). Modeling the dynamics of human brain activity with recurrent neural networks. Frontiers in Computational Neuroscience, 11, 7](https://www.frontiersin.org/articles/10.3389/fncom.2017.00007/full).
- [Munakata, Y., McClelland, J. L., Johnson, M. H., & Siegler, R. S. (1997). Rethinking infant knowledge: Toward an adaptive process account of successes and failures in object permanence tasks. Psychological Review, 104(4), 686](http://www.cs.memphis.edu/~tmccauly/munakataetal97.pdf).

## Online tutorials

- [NLP From Scratch: Classifying Names with a Character-Level RNN (Pytorch)](https://pytorch.org/tutorials/intermediate/char_rnn_classification_tutorial.html)
- [Recurrent Neural Networks (RNN) with Keras](https://www.tensorflow.org/guide/keras/rnn)
- [ML with Recurrent Neural Networks (NLP Zero to Hero - Part 4)](https://www.youtube.com/watch?v=OuYtk9Ymut4)

## Theory papers and book chapters

- [Elman, J. L. (1990). Finding Structure in Time. Cognitive Science, 14(2), 179–211](https://crl.ucsd.edu/~elman/Papers/fsit.pdf). 
- [Bengio, Y., Simard, P., & Frasconi, P. (1994). Learning long-term dependencies with gradient descent is difficult. IEEE Transactions on Neural Networks, 5(2), 157–166](https://ieeexplore.ieee.org/document/279181).
- [Sequence Modeling: Recurrent and Recursive Nets in Deep Learning by Goodfellow, Bengio, and Courville](https://www.deeplearningbook.org/contents/rnn.html).
- [Recurrent Neural Networks in Dive into Deep Learning by Zhang, Lipton, and Smola](https://d2l.ai/chapter_recurrent-neural-networks/index.html).

## Contributors

- [Pablo Caceres](mydoc_about.html#pablocaceres) 

{% include links.html %}