# ANN Classification Problem: Digit Recognition
<p align="center">
    <img src="https://github.com/CharlesDeLabra/Housing-Number-recognition-with-ANN/blob/main/images/number.png?raw=true" alt="Logo" width=72 height=72>
  <h3 align="center">Artificial Neural Networks: Street View Housing Number Digit Recognition</h3>
  <p align="center">
    This project solved a classification problem of Digit recognition to classify the housing number of a house. It was trained Artificial Neural Networks for solving the problem.
    <br>
  </p>
</p>

## Table of contents

- [Context](#context)
- [Problem Statement](#problem-statement)
- [Code](#code)
- [Status](#status)
- [Analysis](#analysis)
- [Conclusions](#conclusions)
- [Recomendations](#recomendations)

## Context

One of the most interesting tasks in deep learning is to recognize objects in natural scenes. The ability to process visual information using machine learning algorithms can be very useful as demonstrated in various applications.

The SVHN dataset contains over 600,000 labeled digits cropped from street level photos. It is one of the most popular image recognition datasets. It has been used in neural networks created by Google to improve map quality by automatically transcribing the address numbers from a patch of pixels. The transcribed number with a known street address helps pinpoint the location of the building it represents.

## Problem Statement

There is a huge dataset of housing numbers and it is needed to train a model that allow the system to classify the digits in order to recognize which digits is on each images. Since the digits are stored in images, it is needed to use NN so it will be check if ANN solves the problem.

## Code

The program was written on Jupyter Notebooks in Python Language. You can access to the code [here](https://github.com/CharlesDeLabra/Housing-Number-recognition-with-ANN/blob/main/ANN_Digits.ipynb)

## Status

The code is finished and have been evaluated, the goal was partially completed since the model was good enough to predict 70% of the digits but it fails in some digits compared to other ones.

## Analysis

The first steps was importing the data and after that it was necessary to see the images, so it was printed the first 10 images in order to visualize out dataset:

<br>
<p align="center">
    <img src="https://github.com/CharlesDeLabra/Housing-Number-recognition-with-ANN/blob/main/images/data.png?raw=true" alt="Data" width=911 height=100> 
</p>
<br>

After that it was needed to preprocess the data, so the next steps were followed:

- Print the first image in the train image and figure out the shape of the images
- Reshape the train and the test dataset to flatten them. Figure out the required shape
- Normalise the train and the test dataset by dividing by 255
- Print the new shapes of the train and the test set
- One-hot encode the target variable

After completing these steps it were created two model, the first one stucture was the next one: 

- First hidden layer with 64 nodes and relu activation and the input shape which is used above
- Second hidden layer with 32 nodes and relu activation
- Output layer with softmax activation and number of nodes equal to the number of classes -Compile the model with the categorical_crossentropy loss, adam optimizer (learning_rate = 0.001), and accuracy metric. Do not fit the model here, just return the compiled model.

After creating and training the previous model the results were the next ones:

<br>
<p align="center">
    <img src="https://github.com/CharlesDeLabra/Housing-Number-recognition-with-ANN/blob/main/images/data2.png?raw=true" alt="Data2" width=630 height=626> 
</p>
<br>

The results were not acceptable since the accuracy was almost near 60% so the second model was created:

- First hidden layer with 256 nodes and relu activation
- Second hidden layer with 128 nodes and relu activation
- Dropout layer with rate equal to 0.2
- Third hidden layer with 64 nodes and relu activation
- Fourth hidden layer with 64 nodes and relu activation
- Fifth hidden layer with 32 nodes and relu activation
- BatchNormalization layer
- Output layer with softmax activation and number of nodes equal to the number of classes -Compile the model with the categorical_crossentropy loss, adam optimizer (learning_rate = 0.0005), and accuracy metric. Do not fit the model here, just return the compiled model.

After creating and training the model, the results were the next ones: 

<br>
<p align="center">
    <img src="https://github.com/CharlesDeLabra/Housing-Number-recognition-with-ANN/blob/main/images/data3.png?raw=true" alt="Data3" width=630 height=626> 
</p>
<br>

These results were better than the previous since it were almost of 70% and this model was choosen for making our classification. The results of the classification were the next one:

<br>
<p align="center">
    <img src="https://github.com/CharlesDeLabra/Housing-Number-recognition-with-ANN/blob/main/images/data4.png?raw=true" alt="Data4" width=637 height=941> 
</p>
<br>

Using this final model lead to the next parts which are conclusions and recommendations.

## Conclusions

- 0,4 and 7 have the best result with 80% or more on the F1 score
- All of the classes have more than 70% on F1 results
- 3 and 8 have the lowest score, which means that other number are confuse with these ones.
- The model confused 5 with 3, 4 with 6, 7 with 2 and 8 with 6
- We need to export the model since the results were the better ones, it is needed to check the trade between computational resources and acuraccy.

## Recomendations

- It is needed to obtain more data about luxury cars
- Use the model for luxury cars only as a guide since the results could be better
- Since model of non-luxury cars had more than 90% of R-squared it is good to predict prices 
- Use Lasso model for luxury cars and Random Forest for non-luxury cars
