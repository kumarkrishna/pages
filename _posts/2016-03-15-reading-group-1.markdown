---
layout: post
categories: science
author: Kumar Krishna Agrawal
date: 2016-03-15 21:19:42
title: Image Captioning&colon; The first talk
summary: Every picture tells a story
---

The Machine Learning Reading Group is a weekly paper presentation session, to engage in discussions on 
less explored direction in theoretical computer science, with a focus on Deep Learning. The audience demography ranging from professors to undergraduate students; anyone with a knack for Learning theory.

<figure style="text-align:center">
<img src="/images/first_page.png"
     title="Cover page of my presentation delivered in a Reading Group session, IIT Kharagpur."
     style="width:auto; height:350px; border:solid 1px #ccc"/>
<figcaption>
    Introductory slide from the presentation.
</figcaption>
</figure>

With a couple of introductory talks on the theoretical foundations of Machine Learning, this week I had the opportunity to talk on an [interesting paper](http://cs.stanford.edu/people/karpathy/deepimagesent/) out of the Stanford AI Lab, I had recently come across; on *Multimodal Learning*. While the problem at hand; of describing images using sentences, rather than just labels; the approach taken in the paper was quite intuitive and simple. Much like putting together *Lego blocks together* to construct something compelling, as the lead author of the paper [Andrej Karpathy](http://cs.stanford.edu/people/karpathy/), would like to put it. 

In this case, the building *blocks* were Convolutional and Recurrent Neural Networks, with the focus on designing an architecture to bring the paraigms together. With ConvNets for learning image representations, and Recurrent Nets for sequence modelling, their approach looked like an obvious choice for such a problem. While much of the analysis was emperical and the results pretty convincing, the paper opens intersting directions of exploring in future work. Meanwhile, the source code for running the experiments are also made publically available at [NeuralTalk2](https://www.youtube.com/watch?v=NFqMGprSjcU) and are quite fun to play around with.

<figure style="text-align:center">
<img src="/images/rg_result.png"
     title="Interesting results from data-driven models"
    style="width:auto; height:350px; border:solid 1px #ccc"/>
<figcaption>
    After all the captions are pretty convincing.
</figcaption>
</figure>

The talk inspired some interesting discussions on the structure of using convolutions on images, 
hierarchical feature learning and sequence modelling using LSTMs. An important takeaway for me, among many others, was the importance of open discussions in channeling clarity of thoughts. That there is a fine line between understanding something, and then communcating it effectively to others, became more prominent to me during the session. 

Putting it all together, it was a pretty amazing experience, and first of probably
many more to follow.

My presentation for the talk can be found
[here](/talk/captions.pdf).
A video for the demo is available on [Youtube](https://www.youtube.com/watch?v=NFqMGprSjcU).


