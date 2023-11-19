# CS50 AI Shopping Prediction Project

<img src="https://i.imgur.com/qhnttAC.jpg">

## Overview
This project is part of the CS50 Introduction to Artificial Intelligence with Python course. It involves developing a machine learning model to predict whether online shopping customers will complete a purchase. The model is built using a k-nearest neighbors (k-NN) classifier and is trained on a dataset containing about 12,000 user sessions from a shopping website.

## Features
- **Data Processing**: Converts raw shopping data from CSV files into structured evidence and labels for machine learning.
- **Machine Learning Model**: Implements a k-NN classifier (with k=1) to predict customer purchasing behavior.
- **Performance Metrics**: Calculates sensitivity (true positive rate) and specificity (true negative rate) to evaluate model performance.

## Technologies Used
- Python 3.10
- scikit-learn (for machine learning algorithms)
- NumPy (optional, for advanced data handling)

## Installation
To set up the project environment, follow these steps:
1. Ensure Python 3.10 is installed on your machine.
2. Install the required Python packages:
   ```bash
   pip install scikit-learn
   ```
3. Clone this repository or download the source code.

## Usage
To run the prediction model:
1. Place the `shopping.csv` data file in the same directory as the script.
2. Execute the script via the command line:
   ```bash
   python shopping.py shopping.csv
   ```
3. The output will display the model's performance metrics.

## Functions Overview
- `load_data(filename)`: Reads data from a CSV file and processes it into formatted evidence and labels.
- `train_model(evidence, labels)`: Trains a k-nearest neighbor model using the provided training data.
- `evaluate(labels, predictions)`: Calculates and returns the sensitivity and specificity based on the model's predictions.

## Data
The `shopping.csv` file contains user session data with the following columns:
- Administrative, Informational, ProductRelated (integer)
- Administrative_Duration, Informational_Duration, ProductRelated_Duration, BounceRates, ExitRates, PageValues, SpecialDay (float)
- Month (categorical, converted to integer)
- OperatingSystems, Browser, Region, TrafficType, VisitorType (integer)
- Weekend (boolean, converted to integer)
- Revenue (boolean, converted to integer for labels)

## Results
The model's performance is evaluated based on its accuracy in predicting whether users completed a purchase. It outputs the following metrics:

Correct: **4068**
Incorrect: **864**
True Positive Rate: **40.05%**
True Negative Rate: **90.20%**
