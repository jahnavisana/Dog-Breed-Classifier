

## Project Overview

The Dog breed classifier is the problem where in if an image of dog or human is supplied we have to identify the resembling breed. The idea is to build a pipeline that can process real world user supplied images and identify an estimate of the canine’s breed. This is a multi-class classification problem where we can use supervised machine learning to solve this problem. After completion of the model. I will build a web app where the user can input in the image format and the predictions will be outputted on his screen. I felt this project is very helpful in identifying a dog breed when the owner himself is confused and for people who are tempted to dogs and want to know dog breed to buy it if they have available picture of the dog.I will be using Convolution Neural Network to build this image classifier as they are specialized type of neural network for processing the grid data.



## The Scratch CNN
Most of the pre-trained models use (224,224) as size so I have used that size. I have applied random-sized crop and random horizontal flip for the train-dataset. I have done a resize of 256 and then centre cropped to 224 on the valid dataset. For the test dataset I have only done resizing. I have applied normalization to all the three i.e train, valid, test datasets. All the images are converted to tensors before passing it to the model.It had a very less accuracy of 18%

## Refined CNN

The first CNN created from scratch had just an accuracy of 18%.It met the benchmark provided but the model could be improved in a great way using the concept of transfer learning. So, I have resnet101 architecture which is already pre-trained on the dataset the architecture as mentioned was 101 layers deep. The last layer of the model was fed as the input to our model. We needed to add the fully connected layer to produce the 133 dimensional output. The model really did well. I trained it for 10 epochs and the accuracy was 76%.Around 643/836 images were classified right!
## Datasets
The datasets used for this project can be obtained from the following links:
https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dogImages.zip
https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/lfw.zip