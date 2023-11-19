# Adaptive Deep Learning Model for Artistic Style Transfer

Building a deep learning model to implement Fast Neural Style Transfer by using an encoder-decoder architecture with VGG19 feature extraction backbone for optimizing perceptual loss

## Introduction

Introduced by Gatys et. al, Neural Style Transfer is an optimization technique for transforming any photo or video into the artistic style of any renowned painting. This technique can allow us to produce a large variety of images from a single training session. However this technique is quite slow, suffering from long inference times. To tackle this issue, a novel approach, called Fast Style Transfer, has been proposed, which is significantly faster than the optimization-based technique for Neural Style Transfer introduced by Gatys et al. 

The process involves training a feedforward network that applies artistic styles to images, utilizing the loss function outlined in Gatys et al's paper. The feedforward network, functioning as a residual autoencoder, takes a content image as input and generates a stylized output. Additionally, the model incorporates instance normalization instead of batch normalization, as suggested in the paper titled *Instance Normalization: The Missing Ingredient for Fast Stylization*. Training is carried out using perceptual loss, as defined in the paper *Perceptual Losses for Real-Time Style Transfer and Super-Resolution*. The VGG19 model is employed to calculate perceptual loss, with further details provided in the associated paper.

For example, using Neural Style Transfer the image of a dog painted in the style of Wassily Kandinsky's Composition 7 is generated, given below:

<img src="https://storage.googleapis.com/download.tensorflow.org/example_images/YellowLabradorLooking_new.jpg" width="500px"/>

[Picture of a Yellow Labrador](https://commons.wikimedia.org/wiki/File:YellowLabradorLooking_new.jpg)

<img src="https://storage.googleapis.com/download.tensorflow.org/example_images/Vassily_Kandinsky%2C_1913_-_Composition_7.jpg" width="500px"/>

[Wassily Kandinsky's Composition 7](https://commons.wikimedia.org/wiki/File:Vassily_Kandinsky,_1913_-_Composition_7.jpg)

<img src="https://tensorflow.org/tutorials/generative/images/stylized-image.png" style="width: 500px;"/>

Image Generated Using Neural Style Transfer

## Requirements

The following Python libraries are needed to ensure that the notebook runs smoothly

numpy==1.23.5 \
tensorflow==2.14.0 \
PIL==9.4.0 \ 
matplotlib==3.7.1 \
requests==2.31.0 \

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install requirements.txt.

```bash
pip install -r requirements.txt
```

Download the dataset from Google Drive link: [NeuralStyleTransfer](https://drive.google.com/file/d/15IF18bDscAVg8eAta6PGtKYmLEta-Ofd/view?usp=sharing)

## Usage

Clone the repository, download the dataset from the link given above, extract the dataset from the zip file into the same folder as the project, and run the Jupyter notebook attached with the project. A model checkpoint is provided in this repo for instant inference without training (nst_model_weights).

## Limitations

1) The approach by Gatys et. al, while being slower, can accomodate multiple style images. The encoder-decoder architecture is capable of accommodating only one style for one set of encoder-decoder weights.
2) Due to limited computational resources, artifacting is seen in the generated images. Training for more epochs may be a solution.
