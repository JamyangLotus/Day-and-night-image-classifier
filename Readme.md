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

We set two variables to store the directory path for training images and test images.

```python
training_file = 'day_night_images/training/'
testing_file = 'day_night_images/test/'
```
## Load training images from path:'day_night_images/training/'

```python
IMAGE_LIST = helpers.load_dataset(training_file)
STANDARDIZE_IMAGE_LIST = helpers.standardize_list(IMAGE_LIST)
```
## Feature Extraction

Create a feature that represents the brightness in an image. We'll be extracting the average brightness using HSV colorspace. Specifically, we'll use the V channel (a measure of brightness), add up the pixel values in the V channel, then divide that sum by the area of the image to get the average Value of the image

### Function for calculating the average brightness of an image

```python
def avg_brightness(image):
  hsv = cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
  sum_brightness = np.sum(hsv[:,:,:]
  area = 600*1100
  
  avg = sum_brightness/area
  
  return avg
```




