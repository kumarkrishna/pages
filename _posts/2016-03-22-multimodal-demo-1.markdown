---
layout: post
categories: science
author: Kumar Krishna Agrawal
date: 2016-03-22 22:21:19
title: An image worth a thousand words
summary: Talking to machines
---

**Prologue:** Preparing for my [first talk](http://kumarkrishna.github.io/pages/science/reading-group-1.html) at the Machine Learning Reading Group, I decided on including a short web-demonstration. The motivation: making the session more interactive, and convince the audience that the models perform fairly well.(Largely inspired from the demonstrations at [CloudCV](https://cloudcv.org/vqa/) )

The broad topic for my talk was Multimodal Learning, image and text being the primary modalities. Though there were various interesting directions, which I would have loved to touch upon, I had to restrict myself to [Image Captioning](http://kumarkrishna.github.io/pages/science/reading-group-1.html), due to time constraints. 

Having previously [experimented](http://kumarkrishna.github.io/pages/programming/torch-review-1.html) with the [NeuralTalk2](https://github.com/karpathy/neuraltalk2) library, I already had a trained model, ready for deployment. Therefore to make things more exciting in the demo, I decided on including another task closely related to this; that of Visual Question Answering (VQA, for short). Following a couple of interesting blog posts [[1]](https://avisingh599.github.io/deeplearning/visual-qa/), [[2]](https://github.com/abhshkdz/neural-vqa), it did not take too much effort to train a new model for the same (thanks to our amazing clusters!).

While going through the implementations, what I found especially intersting was the similarity in the approach to solve apparently different looking problems. First, let us consider the architecture for training an `image description generator`. A ConvNet for extracting image representations, followed by a RNN in the supervised learning setting to, generate the descriptions. 

<figure style="text-align:center">
<img src="/images/image_caption.png"
     title="Generating Image captions."
     style="width:auto; height:350px; border:solid 1px #ccc"/>
<figcaption>
    Connecting ConvNets and RNN to generate image descriptions.
    <br>
    (Image source: Andrej Karpathy's lecture slides)
</figcaption>
</figure>

To understand how the model learns, we can consider the output node at each time step of the RNN as a softmax classifier on a `1000-word dictionary`, which is unfolded simultaneously for each example.
Similarly, consider the architecture for training a `visual question answering` model. A ConvNet (preferrably VGG) for extracting image representations, followed by a RNN in the supervised learing setting to, generate the desired answers.

<figure style="text-align:center">
<img src="/images/visual_qa.png"
     title="Visual Question Answering : Alternative Turing test?"
     style="width:auto; height:350px; border:solid 1px #ccc"/>
<figcaption>
    Using ConvNets and LSTM based RNN for VQA.
    <br>
    (Image source: Zemel etal.)
</figcaption>
</figure>

As you must have noticed, the training algorithm for both the approaches is almost the same. Instead of having classifiers at each time-step, we now have a single softmax classifier at the last output node. 
Therefore the next question that we ask is, *Where is the difference between the models?*

Both the architectures fit into the general framework of `many-to-many` sequential models, based on Recurrent Neural Networks. Besides the slight differences in the training, the primary difference comes in the testing phase.

<figure style="text-align:center">
<img src="/images/many_to_many.png"
     title="How RNNs work"
     style="width:auto; height:350px; border:solid 1px #ccc"/>
<figcaption>
    A unified view for image-to-text models.
    <br>
    (Image source: Andrej Karpathy's lecture slides)
</figcaption>
</figure>

An interesting direction which I would like to experiment on, is whether a single model can be trained to handle both the tasks (following some fine-tuning maybe?). Another observation, which I found pretty intriguing was the 'understanding' of abstract ideas, the model achieves. While discussing the `VQA` system with my roommate, we stuck upon the question: 
<br>
*Does the model have `trained` answers for questions starting with `What`, `Where` etc. given the fact we have a restricted dictionary to choose the answer from?*. 

What we ended up testing the system for, was something though intuitive for humans, should be fairly difficult for a machine. Consider the following image :

<figure style="text-align:center">
<img src="/images/sleep_dog.jpg"
     title="Sleeping dog"
     style="width:auto; height:350px; border:solid 1px #ccc"/>
<figcaption>
    Is the dog sleeping?
</figcaption>
</figure>

#### The questions which followed : 
    Query:  Is the dog sleeping?
    Model:  Yes
    Query:  Is the dog awake?
    Model:  No

Though we haven't it more rigourously, we did note similar responses for certain other examples. What does this tell about the model? **That it not only detects the eyes, notices that they are closed, and that this corresponds to the act of sleeping, which in turn is the opposite of being awake**. Phew! Amazing, isn't it?
<br>

Well, probably not. Maybe the model does not make such hierarchichal decisions, like a human would. Or maybe it does? The only way to know more about it, is to carry out more careful experiments to understand what the system is learning. Nevertheless, we can surely say, these models literally hold to the saying : 
<br>
*An image is worth a thousand words.*

(P.S : A short video of the demo can be found [here](https://www.youtube.com/watch?v=NFqMGprSjcU)).


