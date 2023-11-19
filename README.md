# Adaptive Deep Learning Model for Artistic Style Transfer

Building a deep learning model to implement Fast Neural Style Transfer by using an encoder-decoder architecture with VGG19 feature extraction backbone for optimizing perceptual loss

## Introduction

Neural Style Transfer can be applied to transform any photo or video into the artistic style of renowned paintings. This method can allow a single training session to produce a large variety of images. The approach followed here, called Fast Style Transfer, is significantly faster than the optimization-based technique for Neural Style Transfer, introduced by Gatys et al. 

The process involves training a feedforward network that applies artistic styles to images, utilizing the loss function outlined in Gatys et al's paper. The feedforward network, functioning as a residual autoencoder, takes a content image as input and generates a stylized output. Additionally, the model incorporates instance normalization instead of batch normalization, as suggested in the paper titled "Instance Normalization: The Missing Ingredient for Fast Stylization." Training is carried out using perceptual loss, as defined in the paper "Perceptual Losses for Real-Time Style Transfer and Super-Resolution." The Vgg19 model is employed to calculate perceptual loss, with further details provided in the associated paper.

## Requirements



## Usage

## References
