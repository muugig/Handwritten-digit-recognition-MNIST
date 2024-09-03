# Handwritten-digit-recognition-MNIST
Handwritten Digit Recognition using Convolutional Neural Networks in Python with Keras

## MNIST dataset:

MNIST is a collection of handwritten digits from 0-9.
Image of size 28 X 28



## Code Requirements
python 3.x with following modules installed

1. numpy
2. seaborn
3. tensorflow
4. keras
5. opencv2

## Description
This is a 5 layers Sequential Convolutional Neural Network for digits recognition trained on MNIST dataset. I choosed to build it with keras API (Tensorflow backend) which is very intuitive.

It achieved 98.51% of accuracy with this CNN trained on a GPU, which took me about a minute. If you dont have a GPU powered machine it might take a little longer, you can try reducing the epochs (steps) to reduce computation.

## Execution


To run the code type,

`python digit_recogniser.py`


## Update

### For running on GPU enabled devices:

Please uncomment the following line from **digit_recogniser.py** (line no. 70) file:
```
tfback._get_available_gpus = _get_available_gpus
```

**Note: If you are using the tensorflow 2.1, then you may get an error "AttributeError: module'tensorflow_core._api.v2.config' has no attribute 'experimental_list_devices'"**

As the experimental_list_devices is deprecated in tf 2.1. A simple snippet is injected into the code to make the code work.
And the code is taken from here : https://github.com/keras-team/keras/issues/13684#issuecomment-595054461
