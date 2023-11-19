# Adaptive Deep Learning Model for Artistic Style Transfer

Building a deep learning model to implement Fast Neural Style Transfer by using an encoder-decoder architecture with VGG19 feature extraction backbone for optimizing perceptual loss

## Introduction

Introduced by Gatys et. al, Neural Style Transfer is an optimization technique for transforming any photo or video into the artistic style of any renowned painting. This technique can allow us to produce a large variety of images from a single training session. However this technique is quite slow, suffering from long inference times. To tackle this issue, a novel approach, called Fast Style Transfer, has been proposed, which is significantly faster than the optimization-based technique for Neural Style Transfer introduced by Gatys et al. 

The process involves training a feedforward network that applies artistic styles to images, utilizing the loss function outlined in Gatys et al's paper. The feedforward network, functioning as a residual autoencoder, takes a content image as input and generates a stylized output. Additionally, the model incorporates instance normalization instead of batch normalization, as suggested in the paper titled *Instance Normalization: The Missing Ingredient for Fast Stylization*. Training is carried out using perceptual loss, as defined in the paper *Perceptual Losses for Real-Time Style Transfer and Super-Resolution*. The VGG19 model is employed to calculate perceptual loss, with further details provided in the associated paper.

## Requirements



## Usage

## References
