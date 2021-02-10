---
title: Origins of the Autoencoder
categories:
- Unsupervised Learning
excerpt: |
  Autoencoders are your bread and butter when it comes to dimensionality reduction and feature extraction. This blog post explains in detail their inner workings.
feature_text: |
  ## The Autoencoder
  The autoencoder is an unsupervised learning model that utilizes an encoder and a decoder to learn a latent representation of data.
feature_image: "https://picsum.photos/2560/600?image=733"
image: "https://picsum.photos/2560/600?image=733"
---

The autoencoder is a fantastic and vesatile tool to have in your Machine Learning toolkit. While the regular autoencoder is a relatively simple model, it teaches you some of the fundamental concepts of the last decade in deep learning, which gives you a foot in the door for more advanced models such as Latent variable models and generative adversarial networks, and hence making them more accessible.

### Origins of the Autoencoder

Interestingly, when trying to trace back the origins of the autoencoder, it seems that there is no obvious consensus about it's origin. A cursory google search does not immediately reveal to us a clear pointer towards a distinct source. However, we are met with a Stack Exchange thread that is also discussing the same issue. One of the answers points towards an article by Schmidhuber called "Deep learning in neural networks: an overview" which recounts a history of neural networks and states that: 'Perhaps the first work to study potential benefits of UL-based pre-training was published in 1987. It proposed unsupervised AE hierarchies (Ballard, 1987), closely related to certain post-2000 feedforward Deep Learners based on UL'. The study that he is citing here is called 'Modular learning in neural networks' and does indeed describe an architecture that we know today as the autoencoder.

The paper by Ballard explains: 'Activation from the input is propagated to the internal units and then back to the output, where it can be interpreted as a virtual copy. That is, it is the input as reconstructed from the internal representation. Since the input is known, this can be used to generate an error signal, just as in the feedforward case, that is then sent backwards around the network to the input weights. This architecture was first proposed by Hinton and Rumelhart'. Which leads us deeper down the rabbit hole.


### Learning internal representations by Error Propagation

{% include figure.html image="https://i.imgur.com/H2jZ5xJ.png" alt="Image with just alt text" %}

This idea of auto-association was introduced a year earlier (1986) by Hinton and Rumelhart in their paper 'Learning internal representations by error propagation', as stated. Which is in concordance with other sources that also state this as being the first paper to introduce the autoencoding concept (see Autoencoders: an overview). Hinton's paper explores the effect of hidden units when one trains a model to copy the input the output via means of error propagation. In comparison to earlier models that attempted this without any hidden units and ran into a number of issues, such as the incapability of solving specific problems like the XOR problem. Which is one of the first points that the paper addresses, Minsky and Papert proved earlier that neural networks were incapable of solving linearly inseparable problems, however when adding a hidden unit, Hinton shows that they can indeed solve the XOR problem.

### Dimensionality reduction
Exploring the usefulness of autoencoding structures for dimensionality reduction began with a paper called 'Neural Networks and Principal Component Analysis:
Learning from Examples Without Local Minima ' by Baldi and Hornik. They state that 'Auto-association, which is also called auto-encoding or identity mapping (see Ackley, Hinton, & Sejnowski; 1985; Ellman & Zipser, 1988) is a simple trick intended to avoid the need for having a teacher, that is, for knowing the target values Yt, by setting Xt = Yt. In this mode, the network will tend to learn the identity map which in itself is not too exciting. However, if this is done using one narrow layer of hidden units, one expects the network to find efficient ways of compressing the information contained in the input patterns'
Fast forward a couple of years to 1993, the paper 'Non-linear Dimensionality Reduction' by DeMers and Cottrell discusses the usage of multi-layer encoder-decoder architectures for the sake of dimensionality reduction. The paper raises the point that an autoencoder with one hidden layer will essentially extract the principal components of the data, and proceed to show that adding an additional layer between the input, the hidden layer and the output allows the autoencoder to learn non-linear representations of the data. Both papers significantly contributed to our understanding of autoencoders today and how we actually use them today, mainly for dimensionality reduction. I wonder however why there's a quite long gap of time between the two papers.

### Towards modern applications of Autoencoders
Fast forward another decade, a noteworthy article is 'Reducing the Dimensionality of Data with Neural Networks' again by Hinton, which may be the first study to apply auto-encoders in the context of images. 


### Conclusion
There is something quite exciting about exploring older papers. Older papers feel a lot less standardized in comparision to current papers, and the writing style is less leaden. I recommend trying it yourself, picking some method that you are familiar with and trying to trace back it's origins to see how it eveolved over the years with ideas from different people in different places.
