# CIFAR-10-Image-Classification
Image classification with transformations on CIFAR 10 dataset

## Steps

First defined some PyTorch transformations. 
1) Flip
2) Rotate 90 degrees

Used the pretrained Resnet18 model (from torchvision) to extract features and use them as inputs in a new multi-class logistic regression model. 
Here, I have only optimized parameters of the final layer. 

Labels are shown for the predictions for both the transformed models. 
Correct prediction has one label whereas incorrect prediction has all 5 labels showing that it is incorrectly predicted.

### FINE TUNING:
In fine tuning, the weights of the pre-trained CNN model are preserved on some of layers and tuned in the others. 
I adjusted the learning parameters and observed the results. 
We can tweak the num_epochs to train for longer, batch_size to adjust the size of each minibatch, 
gamma to play with the speed of convergence (learning rate), or step_size to move towards the minima.

### PERFORMANCE

###### AFTER FINE TUNING PERFORMANCE IMPROVED SIGNIFICANTLY
Accuracy of Model with image random Flip: 92.3% 
Accuracy of Model with image random Rotation: 92.4% 


###### WITHOUT Fine Tuning 
Accuracy random Flip: 79.5%
Accuracy random Rotation: 66.5%

### You can download the code and run in jupyter notebook.
