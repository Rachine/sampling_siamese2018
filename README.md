# Sampling strategies in Siamese Networks for unsupervised speech representation learning

### Introduction

Recent studies have investigated siamese network architectures for learning invariant speech representations using same-different side information at the word level. Here we investigate systematically an often ignored component of siamese networks: the sampling procedure (how pairs of same vs. different tokens are selected). We show that sampling strategies taking into account Zipf's Law, the distribution of speakers and the proportions of same and different pairs of words significantly impact the performance of the network. In particular, we show that word frequency compression improves learning across a large range of variations in number of training pairs. This effect does not apply to the same extent to the fully unsupervised setting, where the pairs of same-different words are obtained by spoken term discovery. We apply these results to pairs of words discovered using an unsupervised algorithm and show an improvement on state-of-the-art in unsupervised representation learning using siamese networks.


### License

Our code is released under the GNU GENERAL PUBLIC LICENSE  (refer to the LICENSE file for details).

### Cite our [paper](https://arxiv.org/abs/1804.11297)

If you find this code useful in your research, please, consider citing our paper:
```
 @inproceedings{riad18sampling,
    author      = "Rachid Riad and Corentin Dancette and Julien Karadayi and Neil Zeghidour and Thomas Schatz and Emmanuel Dupoux",
    title       = "Sampling strategies in Siamese Networks for unsupervised speech representation learning",
    booktitle   = "Proc. Interspeech 2018",
    year        = "2018"
}
```
### Contents

  1. [Requirements](#requirements)
  2. [Method](#method)
  3. [Evaluation](#evaluation)
  4. [Features](#features)

### Requirements

To run the code, you need python3 and pytorch installed and install the  [ABnet3](https://github.com/bootphon/abnet3) package and its dependencies.

### Method

This repo contains the yaml files for the method described in the paper. For instance, to replicate the 100%-buckeye variations of sampling function which is in the figure 1 of the paper:

```Bash
python Path_to_abnet3/abnet3/gridsearch.py Path_to_sampling_siamese2018/exp_yaml/prop_sampling_functions_buckeye_100.yaml
```

### Evaluation

Evaluation tools can be found on the [challenge website](http://sapience.dec.ens.fr/bootphon/2015/page_4.html).

For the **weakly-supervised** part, the evaluation is with the sample set of speakers. So features have to be generated for these two extra speakers of the buckeye.

For the **unsupervised** part, the evaluation is the usual track 1 evaluation of the challenge.

### Datasets

Datasets with the raw .wav files can be found on the [challenge website](http://sapience.dec.ens.fr/bootphon/2015/page_4.html).


### Features

In order to generate the features, in the **FeaturesGenerator** of the yaml exp file:
- fill the good path for the dir of .wav files
- fill the good path for vad file
- fill the output path
- change the parameter run from **never** to **once**

If you want to run this code on new data, you will need to process the data with the 'features.py' of **ABnet3**.
If you need more details on this don't hesitate to email the first author of the paper.

We also provide the top down words used in the paper for the weakly and unsupervised settings in the folder **data**.

### References

.. [1] Riad, R., Dancette, C., Karadayi, J., Zeghidour, N., Schatz, T., Dupoux, E.
       *Sampling strategies in Siamese Networks for unsupervised speech representation learning.*
       In Nineteenth Annual Conference of the International Speech Communication Association

.. [2] Thiolliere, R., Dunbar, E., Synnaeve, G., Versteegh, M., & Dupoux, E.
       *A hybrid dynamic time warping-deep neural network architecture for unsupervised acoustic modeling.*
       In Sixteenth Annual Conference of the International Speech Communication Association

.. [3] Zeghidour, N., Synnaeve, G., Usunier, N. & Dupoux, E.
       *Joint Learning of Speaker and Phonetic Similarities with Siamese Networks.*
       In: INTERSPEECH-2016, (pp 1295-1299)
