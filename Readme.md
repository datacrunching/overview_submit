# Objective
Find defects in the rope.

## Thoughts of methods 

The main task for the classification is to indentify the features of the image that represent the defect. The features can then be passed as an input to classifier. 

### SVM: 
Simplest method is to just use image as an input. Define a hyperplane than separates the images into two class SVM (such as using oneclasssvm)

### Traditional Feature extractors + classifer. 
This is a standard method in image classification. We can use HOG, SIFT or GABOR feature extractor. Use the features as input to classifier. Examples of classiers include SVM, MAP etc. SIFT is faster compared to GABOR (based on google search). 

### Deep learning based approches.
Given the large number of training images. This approach will possibly give best results. 


## Dataset 
Generated images from the look clean (no blurr,shadows). The orientation of the rope is changing. 
On every anamoly image, there is a black blob. This needs to be identified. 


## Which methos to implement? 
Finding defects in rope can be done with various methods with varying degree of complexity. Below, I tried with the method that gives maximum accurnacy. 

## Method tried 

### Deep learning complex nueral network
In this method, we used trasfer learning on resnet model. Additional images is generated by flipping,rotating, additing brightness using existing images. 

Fast.ai library was used for trasfer learning.
First, dense layer of the resnet is remove and is trained with the ROPE dataset.
Then all layers are trained with varying learning rate. 
Archieved an accuracy of 99.8% on the validation dataset. 
Achieved predictions/sec = 128 images on P40. 


//TODO 

### SVM + HOG
### Gabor Filter 

