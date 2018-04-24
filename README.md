# Fork of zsdonghao's DCGAN in TensorFlow

## Motivation
This fork was done primarily as an exploration of GAN and setting up an environment for Tensorflow with GPU.
The dataset used was a relatively small dataset (n=5000) of faces drawn by various artists found on the web.
Results shown in results folders are the results of generating images for 300 epochs, with zsdonghao's default batch size.
The folder labelled 'Run 1' used test images of size 128x128px to train the discriminator, with a generator producing images of size 64x64px.
The folder labelled 'Run 2' used test images of size 128x128px to train the discriminator, with a generator producing images of size 128x128px.

TensorFlow / TensorLayer implementation of [Deep Convolutional Generative Adversarial Networks](http://arxiv.org/abs/1511.06434) which is a stabilize Generative Adversarial Networks.

Looking for Text to Image Synthesis ? [click here](https://github.com/zsdonghao/text-to-image)

![alt tag](img/DCGAN.png)

* [Brandon Amos](http://bamos.github.io/) wrote an excellent [blog post](http://bamos.github.io/2016/08/09/deep-completion/) and [image completion code](https://github.com/bamos/dcgan-completion.tensorflow) based on this repo.
* *To avoid the fast convergence of D (discriminator) network, G (generator) network is updated twice for each D network update, which differs from original paper.*




## Prerequisites

- Python 2.7 or Python 3.3+
- [TensorFlow==1.0+](https://www.tensorflow.org/)
- [TensorLayer==1.4+](https://github.com/zsdonghao/tensorlayer)


## Usage

First, download images to `data/celebA`:

    $ python download.py celebA		[202599 face images]

Second, train the GAN:

    $ python main.py

## Result on celebA


<a href="http://tensorlayer.readthedocs.io">
<div align="center">
	<img src="img/result.png" width="90%" height="90%"/>
</div>
</a>