---
date: 2019-03-18
categories:
  - Technical Deep Dive
tags:
  - deep-learning
  - tensorflow
  - tutorial
---

# Neural Network with TensorFlow: How to Stop Training Using Callback?

A practical tutorial on using callbacks to control training in TensorFlow — stopping early when the desired accuracy is reached.

<!-- more -->

Often, when training a very deep neural network, we want to stop training once the model reaches a target accuracy or when the loss stops improving. TensorFlow provides a clean mechanism for this via **callbacks**.

This tutorial walks through how to implement custom callbacks to gain fine-grained control over your training loop.

[:material-arrow-right: Read the full tutorial](https://medium.com/@supratim.haldar/neural-network-with-tensorflow-how-to-stop-training-using-callback-5c8d575c18a9){target="_blank" .md-button .md-button--primary}
