# Day and Night Image Classifier


The day/night image dataset consists of 200 RGB color images in two categories: day and night. There are equal numbers of each example: 100 day images and 100 night images.

We'd like to build a classifier that can accurately label these images as day or night, and that relies on finding distinguishing features between the two types of images!

Note: All images come from the AMOS dataset (Archive of Many Outdoor Scenes).

## Import resources
Before you get started on the project code, import the libraries and resources that you'll need.

```python
import cv2
import helpers
import numpy as np
import matplotlib.pyplot as plt
```

## Training and Testing data
From 200 images of day/night we will separate them for training and testing.

* 60% of them will be used for training images, for creating a classifier.
* 40% of them will be used for testing images, for calculating the accuracy of our classifier.

We set two variables to store the path of directory of training and testing images separately.

```python
training_file = 'day_night_images/training/'
testing_file = 'day_night_images/test/'
```




