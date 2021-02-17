# Computer Vision Hands on

# Technical Requirement: 
You need to install OpenCV for all of the computer vision work you will be carrying out, using pip install opencv-python. OpenCV is a library of built-in programming functions for computer vision work.

# 1. Foundational concepts of computer vision
We'll go through fundamental things(mentioned below) before going into advanced:
 Image hashing,
 Image filtering,
 Various methods of feature extraction and image retrieval...

# 1.1 Detecting edges using image hashing and filtering
Image hashing is a method used to find similarity between images. Hashing involves modifying an input image to a fixed size of binary vector through transformation. 
There are different algorithms for image hashing using different transformations:

Perpetual hash (phash): A cosine transformation
Difference hash (dhash): The difference between adjacent pixels
After a hash transformation, images can be compared quickly with the Hamming distance. The Python code for applying a hash transformation is shown in the code. A hamming distance of 0 shows an identical image (duplicate), whereas a larger hamming distance shows that the images are different from each other. The Following code snippet imports Python packages, such as PIL, imagehash, and distance. imagehash is a Python package that supports various types...

# 1.2 Extracting features from an image
Once we know how to detect edges, the next task is to detect features. Many edges combine to form features. Feature extraction is the process of recognizing visual patterns in an image and extracting any discriminating local features that match with the image of an unknown object. Before performing feature extraction, it is important to understand the image histogram. An image histogram is the distribution of the color intensity of the image. 

An image feature matches with the test image if the histograms are similar. 
Importing required libraries and reading image

import numpy as np
import cv2
import matplotlib.pyplot as plt
%matplotlib inline
import matplotlib.pyplot as plt
from PIL import Image
image = Image.open('../car.png')
plt.imshow(image)
image_arr = np.asarray(image) # convert image
