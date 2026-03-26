# Image Classification with TensorFlow

This project implements a binary image classifier using TensorFlow and Keras to distinguish between happy and sad faces.

## Overview
The model is a Convolutional Neural Network (CNN) trained on a dataset of facial expressions to classify images as either "Happy" or "Sad". The project demonstrates a complete machine learning pipeline including data preprocessing, model building, training, evaluation, and prediction.

## Features
- Image preprocessing and scaling
- CNN architecture with Conv2D, MaxPooling, and Dense layers
- Model training with TensorBoard logging
- Performance evaluation using precision, recall, and accuracy metrics
- Model persistence for later use

## Dataset Structure
The dataset should be organized as follows:
data/
├── Happy/
│ ├── image1.jpg
│ ├── image2.jpg
│ └── ...
└── Sad/
├── image1.jpg
├── image2.jpg
└── ...

text

## Model Architecture
The model consists of:
- 3 Convolutional layers with ReLU activation and MaxPooling
- Flatten layer
- Dense layer with 256 units (ReLU)
- Output layer with sigmoid activation for binary classification

**Total parameters:** 3,696,625

## Installation
Install the required dependencies:

## Usage
1. Data Preparation
The notebook includes code to clean the dataset by removing corrupted images using OpenCV and imghdr.

2. Load and Scale Data
Images are loaded using image_dataset_from_directory and pixel values are scaled to the [0,1] range.

3. Split Data
The dataset is split into:

70% for training

20% for validation

10% for testing

4. Build the Model
A Sequential CNN model is constructed with convolutional, pooling, flatten, and dense layers, compiled with the Adam optimizer and binary crossentropy loss.

5. Train the Model
The model is trained for 20 epochs with TensorBoard logging for monitoring.

6. Evaluate Performance
Performance is evaluated using precision, recall, and binary accuracy metrics on the test set.

7. Make Predictions
New images can be classified by resizing them to 256x256 pixels and passing them through the trained model.

8. Save the Model
The trained model is saved in H5 format for later use.

Results
Metric	Score
Precision	1.0
Recall	1.0
Accuracy	1.0
These metrics indicate perfect classification performance on the test set.

## Visualization
The notebook includes visualization of:

Sample images from the dataset

Training loss curves

Training accuracy curves

File Structure
text
project/
├── data/                   # Dataset directory
│   ├── Happy/             # Happy face images
│   └── Sad/               # Sad face images
├── models/                 # Saved models
│   └── imageclassifier.h5 # Trained model
└── README.md              # This file
## Requirements
TensorFlow 2.x

OpenCV

Matplotlib

NumPy
