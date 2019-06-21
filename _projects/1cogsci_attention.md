---
name: Visual Attention in Object Classification
tools: [Deep Learning, Tensorflow, Image Processing, Attention Mechanism, CNN, LSTM, Eye-tracking]
image: https://i.imgur.com/8eVb5cF.png
description: The project aims to compare human visual attention with CNN attention. School project for Cognitive Science 3 Fall 2018, at University of Copenhagen.
---

# Visual Attention in Object Classification. The Relationship between Attention in Humans and Deep Networks

The project aims to compare human visual attention with CNN attention. 

School project for Cognitive Science 3 Fall 2018, at University of Copenhagen.

Abstract:


>This work explores different attention mechanisms in an object recognition setting with the POET dataset. We introduce a novel approach to constructing heatmaps visualizing human attention, formalize object recognition as a sequential task, and employ an evaluation scheme that proves to distinguish between computational attention mechanisms in relation to human attention. Finally, we use sequential fixations to guide a machine learning model and draw conclusions about the foundational reasons for human effective attention range as a function of eccentricity from the fixation.

Full paper available [here](https://github.com/cristianmtr/visual-attention-cnn-and-eye-tracking/blob/master/paper.pdf)

## Details

We use the [POET](http://calvin.inf.ed.ac.uk/datasets/poet-dataset/) dataset. This provides eye-tracking annotations for ~6000 images categorized into 10 classes. 

We divided the main problem statement into smaller experiments:

1. _CAM (Class Activation Map) Attention_: CNN with global average pooling layer with localization abilities. This exposes the underlying focus of the CNN on an image. In this case we compare human fixations with CNN class activations. Based on the work by [Zhou et al](http://cnnlocalization.csail.mit.edu/Zhou_Learning_Deep_Features_CVPR_2016_paper.pdf).
2. _CNN with Soft Attention_: Based on [Show, Attend and Tell](https://arxiv.org/pdf/1502.03044.pdf), we build a CNN with an attention mechanism layer that learns to focus on specific parts of the image. We compare the attention derived by this model with the attention from the _CAM Attention_.
3. _Patch-based LSTM_: We extract the surrounding area around each fixation in the image, pass them each through a _ResNet50_ pre-trained on ImageNet, and then through a dense layer to predict the 10 classes. This is compared with a baseline _ResNet50_ that predicts on the entire image. In this case, our aim is to contrast how human-guided attention can help computer vision.

In the figure below we can see one of the main results in our paper, a comparison of the different attention heat maps:

![figure](https://i.imgur.com/8eVb5cF.png)

## My contribution

I contributed to the main idea of the project and helped structure the approach.

I extracted, pre-processed and visualized the POET dataset.

I performed experiment (3) from the above list. 

I produced visualizations of the results.


<p class="text-center">
{% include button.html link="https://github.com/cristianmtr/visual-attention-cnn-and-eye-tracking" text="Learn More" %}
</p>
