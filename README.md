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
