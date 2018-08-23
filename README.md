# Sampling strategies in Siamese Networks for unsupervised speech representation learning

### Introduction

Recent studies have investigated siamese network architectures for learning invariant speech representations using same-different side information at the word level. Here we investigate systematically an often ignored component of siamese networks: the sampling procedure (how pairs of same vs. different tokens are selected). We show that sampling strategies taking into account Zipf's Law, the distribution of speakers and the proportions of same and different pairs of words significantly impact the performance of the network. In particular, we show that word frequency compression improves learning across a large range of variations in number of training pairs. This effect does not apply to the same extent to the fully unsupervised setting, where the pairs of same-different words are obtained by spoken term discovery. We apply these results to pairs of words discovered using an unsupervised algorithm and show an improvement on state-of-the-art in unsupervised representation learning using siamese networks.


### License

Our code is released under the GNU GENERAL PUBLIC LICENSE  (refer to the LICENSE file for details).

### Cite

If you find this code useful in your research, please, consider citing our paper:

> @InProceedings{Riad18sampling,
>    author      = "Rachid Riad and Corentin Dancette and Julien Karadayi and Neil Zeghidour and Thomas Schatz and Emmanuel Dupoux",
>    title       = "Sampling strategies in Siamese Networks for unsupervised speech representation learning",
>    booktitle   = "Proc. Interspeech 2018",
>    year        = "2018"
>}

### Contents

  1. [Requirements](#requirements)
  2. [Method](#method)
  3. [Evaluation](#evaluation)
  4. [Features](#features)

### Requirements

To run the code, you need python3 installed and install the [ABnet3](https://github.com/bootphon/abnet3)
In order to obtain the features used here, other dependencies are needed.
For that, see the corresponding [section](#features).

### Method

This repo contains the yaml files for the method described in the paper.

### Evaluation

### Datasets

Datasets with the raw .wav files can be found on the [challenge website](http://sapience.dec.ens.fr/bootphon/2015/page_4.html).



### Features

We provide the features files for t
If you want to run this code on new data, you will need to process the data as follows.
If you need more details on this don't hesitate to email the first author of the paper.

#### **Filterbanks**
