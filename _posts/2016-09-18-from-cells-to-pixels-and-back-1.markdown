---
layout: post
categories: vision science
author: Kumar Krishna Agrawal
date: 2016-09-18 02:23:41
title: From Cells to Pixels and Back - 1
summary: Looking != Seeing
---

In his 1967 expository, **Eye Movements and Vision** <sup>\[\*\]</sup> , psychologist Alfred Yarbus, observes :
>"In man under natural conditions the retinal image is never stationary relative to the retina, and if a strictly stationary and unchanging retinal image is created artificially, the eye ceases to see."

Among the primary proponents of importance of [saccadic movements](https://en.wikipedia.org/wiki/Saccade) and their connection to vision, Yarbus laid foundation of extensive research in the role of **motion** and **attention** in human visual systems.

Illustrating this, consider the following pair of images (glance from left to right) :

<figure style="text-align:center">
<img src="/images/see_not_see.png"
     title="Interest drives attention"
     style="width:auto; height:540px; border:solid 1px #ccc"/>
<figcaption>
    ( Tracking changes in regions of focused attention (b) is substantially simpler than in marginalised attention (a).)
</figcaption>
<small><i>Rensink, O'Regan & Clark</i> <sup>[1]</sup></small>
</figure>

Think about the differences you immediately observed in these set of images.  
Was the movement of helicopter (b), more apparent than shift of the railings (a)?

This is one of the questions **Rensink et al** explore in their fascinating article <sup>\[1\]</sup>. Observing a scene, one might advocate the amazing abilities of the visual system to detect significant changes in the view. That proposition holds merit, largely attributed to relative motion of objects within the scene <sup>[2]</sup>. However, what happens when this transient signal is somehow suppressed? How difficult would it observing changes in a scene then be?

Quite difficult, it seems.

In an experimental setting, a natural way of suppressing these transient signal, would be inserting _blank images_ between two consecutive frames of images.
Try visualizing the left image in Fig. 1(a), followed by a blank gray frame, followed by the right image (Fig. 2). Through a series of such cleverly designed methods, _Rensink et al_ illustrate how **attention** controls our ability to observe these differences.

Even though the visual system _looks_ at the whole scene, it's ability to attend is rather restricted <sup>[3]</sup>. This in turn implies that, any point of time, there would be several sections of the image to which the perception system is essentially blind, and thereby unable to track the changes.

<figure style="text-align:center">
<img src="/images/experiment_see.png"
     title="Capturing attention"
     style="width:auto; height:350px; border:solid 1px #ccc"/>
<figcaption>
    ( Suppresing relative motion in consecutive frames. )
</figcaption>
<small><i>Rensink, O'Regan & Clark</i> <sup>[1]</sup></small>
</figure>

The authors draw several interesting observations, some intriguing ones being :
<ul>
<li> In absence of relative motion, the perception of change is only noted in regions of focused attention.  </li>
<li> Verbal cues could act as surrogates to these transient signal, drastically improving performance. This provides evidence that information about the whole image is indeed available for processing. </li>
<li> These regions of focused attention are probably entered into a _"relatively stable store"_, while the rest are simply overwritten. In subsequent frames, this prevents any further comparison in the unattended regions, making tracking difficult. </li>
<li> Distributing attention all over the image is prohibitive, and is compensated by rapid-switching of these regions of interest (dominated by low-level transients). Only under volitional (voluntary high-level) control does this dynamic shift break down, causing unwarranted issues in tracking. </li>
</ul>

<figure style="text-align:center">
<img src="/images/show_attend_tell.png"
     title="Show, attend and tell"
     style="width:auto; height:500px"/>
<figcaption>
    (Image captioning with Neural Networks. Regions attended to while generating the underlined words.)
</figcaption>
<small><i>Xu et al</i> <sup>[5]</sup></small>
</figure>

Attention mechanisms in the human visual system have a rich and fascinating literature, which if revisited, could potentially provide several insights on improving similar approaches for artificial visual systems. To someone inherently interested in Artificial Neural Networks, parallels to the success in [**Attention and Memory Networks**](http://distill.pub/2016/augmented-rnns/) are immediately noticeable <sup>[4],[5],[6]</sup>. In such architectures, soft-attention aims at distributing attention all over the image and is easier to train through standard back-propagation. On the other hand, while hard-attention tries to achieve focused attention and is substantially harder to train, the results are quantifiably more appealing.

Takeaway from all of this?  
_Looking is definitely a necessary, however not a sufficient condition for **seeing**_.

#### References
<small><sup>\[\*\]</sup> : Yarbus, Alfred L. Eye movements during perception of complex objects. Springer US, 1967.  
<sup>\[1\]</sup> : Rensink, Ronald A., J. Kevin O'Regan, and James J. Clark. "To see or not to see: The need for attention to perceive changes in scenes." Psychological science 8.5 (1997): 368-373.  
<sup>\[2\]</sup> : Posner, Michael I. "Orienting of attention." Quarterly journal of experimental psychology 32.1 (1980): 3-25.  
<sup>\[3\]</sup> : Wolfe, Jeremy M., Kyle R. Cave, and Susan L. Franzel. "Guided search: an alternative to the feature integration model for visual search." Journal of Experimental Psychology: Human perception and performance 15.3 (1989): 419.  
<sup>\[4\]</sup> : Mnih, Volodymyr, Nicolas Heess, and Alex Graves. "Recurrent models of visual attention." Advances in Neural Information Processing Systems. 2014.  
<sup>\[5\]</sup> : Xu, Kelvin, et al. "Show, attend and tell: Neural image caption generation with visual attention." arXiv preprint arXiv:1502.03044 2.3 (2015): 5.  
<sup>\[6\]</sup> : Weston, Jason, Sumit Chopra, and Antoine Bordes. "Memory networks." arXiv preprint arXiv:1410.3916 (2014).  </small>

