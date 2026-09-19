# Simple Linear Regression - Height and Weight Prediction

## Project Overview

This project demonstrates **Simple Linear Regression** using a Height and Weight dataset.

The goal is to build a machine learning model that learns the relationship between a person's **height** and **weight**, and then predicts the weight based on a given height.

## Objective

The main objective is:

> Predict a person's weight based on their height using Simple Linear Regression.

* **Input (X):** Height in centimeters
* **Output (y):** Weight in kilograms

##  Dataset

The dataset is stored in:

```text
height_weight.csv
```

It contains two columns:

| Column | Description                       |
| ------ | --------------------------------- |
| Height | Height of a person in centimeters |
| Weight | Weight of a person in kilograms   |

## Algorithm Used

### Simple Linear Regression

Simple Linear Regression is a supervised machine learning algorithm used to find the relationship between one independent variable and one dependent variable.

The model learns a straight-line relationship between Height and Weight.

The general equation is:

```text
y = mx + c
```

Where:

* `y` = predicted weight
* `x` = height
* `m` = slope
* `c` = intercept

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* Google Colab
* GitHub

##  Project Workflow

```text
Dataset
   ↓
Load CSV using Pandas
   ↓
Explore the Dataset
   ↓
Separate X and y
   ↓
Visualize the Data
   ↓
Split the Dataset
   ↓
Train Linear Regression Model
   ↓
Make Predictions
   ↓
Evaluate the Model
```

##  Implementation

The dataset is loaded using Pandas:

```python
import pandas as pd

data = pd.read_csv("height_weight.csv")
```

The input and output variables are separated:

```python
X = data[["Height"]]
y = data["Weight"]
```

The Linear Regression model is created and trained:

```python
from sklearn.linear_model import LinearRegression

model = LinearRegression()
model.fit(X, y)
```

The model can then be used to predict weight for a new height:

```python
model.predict([[170]])
```
