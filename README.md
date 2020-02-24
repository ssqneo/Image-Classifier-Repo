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
-Naive Bayes Accuracy: 0.5893246
-Naive Bayes Precision: 0.2196508
-Naive Bayes Recall: 0.4412724
-Naive Bayes AuC: 0.6167882
## Random Forest Model
The second model utilizes the `h2o.randomForest` to classify the images and gives the following results:
-Random Forest Accuracy: 0.6937173
-Random Forest Precision: 0.1075924
-Random Forest Recall: 0.2161501
-Random Forest AuC: 0.6485541
## Deep Learning Model
The second model utilizes the `h2o.randomForest` to classify the images and gives the following results:
-Deep Learning Accuracy: 0.3266219
-Deep Learning Precision: 0.0592773
-Deep Learning Recall: 0.1190865
-Deep Learning AuC: 0.4180248
## Support Vector Machine
The second model utilizes the `h2o.randomForest` to classify the images and gives the following results:
-Gaussian RBF Kernel Accuracy: 0.571169
-Gaussian RBF Kernel Precision: 0.3828664
-Gaussian RBF Kernel Recall: 0.7525938


