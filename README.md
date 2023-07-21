# Image Colorization using GANs

This repository is an implementation of the pix2pix paper _Image-to-Image Translation with Conditional Adversarial Networks_ authored by Phillip Isola, Jun-YanZhu, Tinghui Zhou, and Alexei A.Efros. The project generates colored images from black and white images by using a generator discriminator architecture.

Find the code for the project : `image-colorization-using-gan.ipynb` file.

Link of paper followed: https://arxiv.org/abs/1611.07004

Try out the deployed model here : https://huggingface.co/spaces/SMD00/Image_Colorization_Streamlit

## Implementation

A GAN model comprises of 2 sub-models:

>The generator learns to generate plausible data. The generated instances become negative training examples for the discriminator.

>The discriminator learns to distinguish the generator's fake data from real data. The discriminator penalizes the generator for producing implausible results.

We simultaneously train two models: a generative model G that captures the data distribution, and a discriminative model D that estimates the probability that a sample came from the training data rather than G. The training procedure for G is to maximize the probability of D making a mistake. This framework corresponds to a minimax two-player game. In the space of arbitrary functions G and D, a unique solution exists, with G recovering the training data distribution and D equal to 1/2 everywhere.

<img src="images/UNet architecture.png" width="500" alt="Demo Image">
Generator Discriminator Approach

## Clone the repository

```
git clone https://github.com/SahilDanayak/Image-Colorisation-using-GAN.git
pip install requirements.txt
```

## Result

<img src="https://github.com/SahilDanayak/Image-Colorisation-using-GAN/blob/main/images/image-colorization-demo-img.png" width="500" alt="Demo Image">

## Citation

```
@inproceedings{isola2017image,
  title={Image-to-image translation with conditional adversarial networks},
  author={Isola, Phillip and Zhu, Jun-Yan and Zhou, Tinghui and Efros, Alexei A},
  booktitle={Proceedings of the IEEE conference on computer vision and pattern recognition},
  pages={1125--1134},
  year={2017}
}
```
