---
layout: post
categories: programming
author: Kumar Krishna Agrawal
date: 2015-07-03  18:12:54
title: CAFFE &colon; Deep Network Espresso
summary: Brewing neural networks layer by layer
---

**Prologue** : The [Winter School](http://ws2014.cs.cmu.edu/) was a great learning experience, both academically and otherwise. While I made some really crazy friends and interacted with amazing mentors, the 10-day camp opened new frontiers of exploration. With a slightly unorthodox project choice already, my team of nerds ( a.k.a Complex Numbers, duh?! ), was interested in exploring different approaches for detecting objects in images, using Deep Neural Architectures. Much of the idea was inspired by our discussions with [Pulkit](www.eecs.berkeley.edu/~pulkitag/), our wonderful mentor at the WS.

So, the long story short, with others busy sifting through papers trying to get their head around the theory of Neural Networks, I decided to take up on the implementation front of things. And this was the (*Eureka?*) moment, when I was introduced to [CAFFE](http://caffe.berkeleyvision.org/), a Deep Learning framework developed and maintained by the BVLC team at UC Berkeley.

Though the initial sleepless nights were spent experimenting with the framework, I enjoyed every bit of it. The framework, at that point of time, was in fairly early stages of development. Combing through the documentation, and finally to have a [model](http://caffe.berkeleyvision.org/gathered/examples/mnist.html) running was one of the most thrilling experiences of my stay there. Gradually, with some modifications to the source, we were finally able to have a naive implementation of our regularizer running.

What I loved most about using CAFFE, was the simplistic `proto` interface for defining architectures and experimenting with them. Also, the maintainers have been really great at maintaining a [*Model Zoo*](http://caffe.berkeleyvision.org/model_zoo.html) of already trained models, which others can use for their own benchmarking or initializations as need be. Now that I have my spring break coming up, I am excited to read up more on this, and contribute to the development of the awesome framework as well!

**Update** : We recently won the Microsoft Machine Learning Challenge on multi-label object detection, organized by IISc Bangalore! Thank you CAFFE-dev team!

