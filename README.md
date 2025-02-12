We are given a dataset containing 1305 images which belong to different
classes. For each image we are given a mask containing its segmented
version, a transformed and simplified image where `interesting' regions are
emphasized. Masks could be then used to train a model for inferring the
image class.

The following inputs are available:
1. input image, a 256 * 256 * 3 tensor. The last dimension denotes the
number of input channels (RGB). Each pixel is a value in [0, 255];

2. image mask, a 256 * 256 * 1 tensor. Each pixel can take only 6 possible
values, the integers from 0 to 5, representing the different emphasized
areas within all input images. Indeed, given an input image, it is
possible that its mask contains just a subset of all possible mask values.

Design a deep neural network able to output a segmented mask from a given
input image.
