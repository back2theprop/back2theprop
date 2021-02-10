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

The autoencoder is a fantastic tool to have in your Machine Learning toolkit. While the regular autoencoder is a relatively simple model, it teaches you some of the fundamental concepts of the last decade in deep learning, which gives you a foot in the door for more advanced models such as Latent variable models and generative adversarial networks, and hence making them more accessible.

### Origins of the Autoencoder

Interestingly, when trying to trace back the origins of the autoencoder, it seems that there is no obvious consensus about the origin. A cursory google search does not immediately reveal to us a clear pointer towards a distinct source. However, we are met with a Stack Exchange thread that is also discussing the exact issue. One of the answers points towards an article by Schmidhuber called "Deep learning in neural networks: an overview" which states that: 'Perhaps the first work to study potential benefits of UL-based pre-training was published in 1987. It proposed unsupervised AE hierarchies (Ballard, 1987), closely related to certain post-2000 feedforward Deep Learners based on UL'. The study that he is citing here is called 'Modular learning in neural networks' and does indeed describe an architecture that we know today as the autoencoder.

The paper explains 'Activation from the input is propagated to the internal units and then back to the output, where it can be interpreted as a virtual copy. That is, it is the input as reconstructed from the internal representation. Since the input is known, this can be used to generate an error signal, just as in the feedforward case, that is then sent backwards around the network to the input weights. This architecture was first proposed by Hinton and Rumelhart'.

This idea of auto-association was introduced a year earlier (1986) by Hinton and Rumelhart in their paper 'Learning internal representations by error propagation', as stated. Which is in concordance with other sources that also state this as being the first paper to introduce the autoencoding concept. Hinton's paper explores the effect of hidden units when one trains a model to copy the input the output via means of error propagation. In comparison to earlier models that attempted this without any hidden units and ran into a number of issues, such as the incapability of solving specific problems like the XOR problem. Which is one of the first points that the paper addresses, Minsky and Papert proved earlier that neural networks were incapable of solving linearly inseparable problems, however when adding a hidden unit, Hinton shows that they can indeed solve the XOR problem.

The second, unapproved, answer to the same question points to an earlier paper released in 1986 named 'Learning internal representations by error propagation' by Rumelhart, Hinton and Williams. Which is in concordance with more recent works that also cite this work as being the first work to introduce autoencoders.

### Learning internal representations by Error Propagation

{% include figure.html image="https://i.imgur.com/H2jZ5xJ.png" alt="Image with just alt text" %}

It is worth it to spend some reading the paper as it explains with an incredible clarity the concept of a neural network with a hidden representation.

### Towards modern applications of Autoencoders
A noteworthy article is 'Reducing the Dimensionality of Data with Neural Networks' by Hinton, which is maybe the first study to apply auto-encoders in the context of images.

