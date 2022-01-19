# Detecting Reproducible Fatal Collision Locations

This code implement the paper "Kim et al. (2022). Imputing Qualitative Attributes for Trip Chains Extracted from Smart Card Data Using a Conditional Generative Adversarial Network", Under-review at Transportation Research Part C: Emerging Technologies. 

## Overview

The proposed model aims to estimate the qualitative attributes of large-scale passively collected mobility data by mimicking the small-scale travel survey data using Conditional Generative Adversarial Networks (CGAN).

## Getting Started

### Dependencies

* Tensorflow 2.4.1, Keras 2.4.3
* Python 3.6.10

### Components

#### Dataset
* '01_Data' include the smart card and travel survey data, before and after the preprocessing
* Only pertubated samples of smart card and travel survey data are provided due to the permission

##### DataPreprocessing.ipynb
* Transforming the long-form smart card and travel survey data into ndarray form 

##### 2D-Transformer.ipynb
* Step-by-step implementation of 2D-Transformer
* It covers every components including data load, model structure, training, evaluation, and visualization
* Pre-trained generator using full dataset is in the 'Py_generator'

##### BERT_Embed.ipynb
* Step-by-step implementation of BERT to evaluate the fidelity and diversity
* Transforming the categorical outputs (qualitative attributes) into the numeric one for constructing manifold 
* Pre-trained BERT generator using full dataset is 'MLM_Embed_indiv.h5'

## Notice
* Full-paper of this code with detilaed explanation will be provided after peer-review proces

## Authors

[@Eui-Jin Kim](https://sites.google.com/view/euijinkim)


## License

This project is licensed under the MIT License - see the LICENSE.md file for details

## Acknowledgments

* [WGAN-GP](https://github.com/kongyanye/cwgan-gp)
* [Fidelity and Diversity](https://github.com/clovaai/generative-evaluation-prdc)
