# Objective
Find defects in the rope.

## Thoughts
Finding defects in rope can be done with various methods with varying degree of complexity. Here, I have tried with 3 methods. 
It is expected that the rate of prediction should be as high as 200 frames/sec. 

## Method tried 

### Deep learning complex nueral network
In this method, we used trasfer learning on resnet model.
Fast.ai library was used for trasfer learning.
First, dense layer of the resnet is remove and is trained with the ROPE dataset.
Then all layers are trained with varying learning rate. 
Archieved an accuracy of 99.8% on the validation dataset. 
Achieved predictions/sec = 128 images on P40. 


### SVM + HOG
### Gabor Filter 

