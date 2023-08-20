
# Emotion Detection Using Deep Learning

A deep learning model that accurately identifies human faces and their emotions in images and videos.


## Context
Affective computing is a field of Machine Learning and Computer Science that studies the recognition and the processing of human affects. Multimodal Emotion Recognition is a relatively new discipline that aims to include text inputs, as well as sound and video. This field has been rising with the development of social network that gave researchers access to a vast amount of data.
## Introduction

This project aims to classify the emotion on a person's face into one of seven categories, using deep convolutional neural networks. The model is trained on the FER-2013 dataset which was published on International Conference on Machine Learning (ICML). This dataset consists of 35887 grayscale, 48x48 sized face images with seven emotions - angry, disgusted, fearful, happy, neutral, sad and surprised.
## Dependencies

* Python3
* OpenCV
* Tensorflow


## Algorithm

* First, the haar cascade method is used to detect faces in each frame of the webcam feed.

* The region of image containing the face is resized to 48x48 and is passed as input to the CNN.

* The network outputs a list of softmax scores for the seven classes of emotions.

* The emotion with maximum score is displayed on the screen.
## Data Sources

We are using the popular FER2013 Kaggle Challenge data set. The data consists of 48x48 pixel grayscale images of faces. The faces have been automatically registered so that the face is more or less centered and occupies about the same amount of space in each image. The data set remains quite challenging to use, since there are empty pictures, or wrongly classified images.
[The Original FER2013 dataset in Kaggle](https://www.kaggle.com/datasets/deadskull7/fer2013)
## Model

![CNN](https://lh3.googleusercontent.com/yrHzday2CwSYLkXf9yKSoH-BpjqnnAuyiMvPAS5yS3-lFnl5jwkR6FoT_v2Vbi14s414fJSORuGLRQbHyYp6dtHDItRcSQnRWcd1JRGbZC5VlGTvH80gFZrHw8qg2Tx7ca2HYKFc)

Convolutional Neural Networks (CNNs) are a type of deep learning model designed for image and pattern recognition. They work by learning hierarchical features through layers of convolutional and pooling operations. In the initial layers, the network identifies simple features like edges, gradually combining them to detect complex patterns and objects in deeper layers. CNNs use weight-sharing and feature maps to reduce the number of parameters, making them efficient. The final layers often include fully connected layers for classification. Training involves adjusting these weights through backpropagation to minimize the difference between predicted and actual outputs, enabling accurate image analysis and classification.

![CNN2](https://github.com/maelfabien/Multimodal-Emotion-Recognition/blob/master/00-Presentation/Images/video_pipeline2.png?raw=true)

When it comes to applying CNNs in real life application, being able to explain the results is a great challenge. We can indeed plot class activation maps, which display the pixels that have been activated by the last convolution layer. We notice how the pixels are being activated differently depending on the emotion being labeled. The happiness seems to depend on the pixels linked to the eyes and mouth, whereas the sadness or the anger seem for example to be more related to the eyebrows.

![CNN3](https://github.com/maelfabien/Multimodal-Emotion-Recognition/raw/master/00-Presentation/Images/light.png)
## Working

* We initially clone the haar cascade classifier and then use the functions and the data associated with it in our OpenCV function defined.

* Then we import the required dependencies necessary for the project to function ranging from numpy, matplotlib to tensorflow

* Then we build the model using the Sequential Model extracted from the tensorflow keras models library. We select the Convolutional Neural Network which has a pooling of 2D structure and also we use the image processing library to analyze and process the image for emotion detection/recognition

* Then we develop the model and set the parameters and configurations according to the need of the user.

* Finally we come to the opencv section to capture image and detect the emotion where we create a function with unloading the haas cascade classifier model into the created model and create a specific dictionary for certain emotions. and then we perform the necessary processing to detect each frame and dimensions of the image to detect the emotion. and then these cropped and splitted out frames will be returned as an output along with the value of the emotion of the person in the image.


## Screenshots

![App Screenshot](Emo_Det
/Screenshot 2023-08-20 200651.png
)

![App Screenshot](Emo_Det
/Screenshot 2023-08-20 200651.png
)




