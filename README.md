# Image-Classifier-Repo

- Team Syed and Zimin
- CIS-544-11
- 2/24/2020

# About: 

The goal of this project was to build a image classifier in R using Naive Bayes, Random Forest, Deep Learning and Support Vector Machine. The model classifies an image based on the feature and learns with the label provided such as in our case that the picture is of a cat or a dog.

# Requirement:
The script is written in R, the required packages are as follows: `naiveBayes` `randomForest` `deeplearning` `kernlab` `h2o` `tidyverse` `caTools` `rvest` `imager`.

# Labeling image:
For labeling the images we used `imager` which is an image processing package in R. The following link was really helpful in understanding how image processing work and helped us get familiar with the syntax of the package https://dahtah.github.io/imager/imager.html
The imager uses edge detection for an image and converts it into a 4 dimensional array. The four dimensions are labelled x,y,z,c which are width, height, depth and spectrum respectively. The first two are the usual spatial dimensions, the third one corresponds to depth, and the fourth one is colour. In case of a grayscale image the two extra dimensions are obviously pointless since it will be defined by just x and y. The object will still be officially 4 dimensional, with two trailing flat dimensions. Pixels are stored in the following manner: the scanning of the image begins at the upper-left corner, along the x axis. Once it hits the end of the scanline, it moves to the next line. Once it hits the end of the screen, it moves to the next frame (increasing z) and repeats the process. If an image has several colour channels, then once we’re done with the first colour channel we move to the next one. All in all the different dimensions are represented in the x,y,z,c order. In R the object is represented as a 4D array.

<a href="https://ibb.co/K92NDWm"><img src="https://i.ibb.co/nD73BjR/image.png" alt="image" border="0"></a>
<a href="https://ibb.co/g6jyJC1"><img src="https://i.ibb.co/yVf0qJT/image.png" alt="image" border="0"></a>

# Data Split
The data was split using a split ratio of 0.75 and the `set.seed()` utilized was 12345. The naiveBayes, randomForest and Deep Learning models were used with h2o package which is a scalable machine learning platform. It utilizes in-memory compression which makes it very robust. 

# Models: 
## Naive Bayes Model
The first model utilizes the `h2o.naiveBayes` to classify the images and gives the following results:
- Naive Bayes Accuracy: 58.93246 %
- Naive Bayes Precision: 21.96508 %
- Naive Bayes Recall: 44.12724 %
- Naive Bayes AuC: 61.67882 %
## Random Forest Model
The second model utilizes the `h2o.randomForest` to classify the images and gives the following results:
- Random Forest Accuracy: 86.79245 %
- Random Forest Precision: 1.867641 %
- Random Forest Recall: 3.752039 %
- Random Forest AuC: 65.09849 %
## Deep Learning Model
The third model utilizes the `h2o.deeplearning` to classify the images and gives the following results:
- Deep Learning Accuracy: 55.69106 %
- Deep Learning Precision: 16.68697 %
- Deep Learning Recall: 33.52365 %
- Deep Learning AuC: 55.85439 %
## Support Vector Machine
The fourth model utilizes the `ksvm` to classify the images and gives the following results:
- Gaussian RBF Kernel Accuracy: 57.1169 %
- Gaussian RBF Kernel Precision: 38.28664 %
- Gaussian RBF Kernel Recall: 75.25938 %


