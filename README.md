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
The second model utilizes the `h2o.randomForest` to classify the images and gives the following results:
- Deep Learning Accuracy: 55.69106 %
- Deep Learning Precision: 16.68697 %
- Deep Learning Recall: 33.52365 %
- Deep Learning AuC: 55.85439 %
## Support Vector Machine
The second model utilizes the `h2o.randomForest` to classify the images and gives the following results:
- Gaussian RBF Kernel Accuracy: 57.1169 %
- Gaussian RBF Kernel Precision: 38.28664 %
- Gaussian RBF Kernel Recall: 75.25938 %


