# Building a Predictive Model for Physical Activity Classification Using R and GBM

This project demonstrates how to build a predictive model to classify physical activity quality based on accelerometer data collected during weight-lifting exercises. The dataset contains various sensor readings and labels for different classes of movements.

---

## Overview

The primary goal of this project is to predict the quality of weight-lifting exercises. This is achieved by:
- Preprocessing the data to handle missing values and irrelevant columns.
- Visualizing data distributions for better understanding.
- Building a predictive model using **Gradient Boosting Machine (GBM)**.
- Evaluating the model on a validation dataset.
- Making predictions on a test dataset.

---

## Dataset

The data for this project is sourced from accelerometers placed on participants performing different movements. The datasets are:
- `pml-training.csv`: Used for training and validating the model.
- `pml-testing.csv`: Used for generating predictions.

---

## Methodology

### **1. Data Cleaning**
- Removed columns with mostly missing values (`NA`) and metadata like timestamps and usernames.
- Ensured the target variable (`classe`) is a factor.

### **2. Exploratory Data Analysis (EDA)**
- Visualized class distributions using `ggplot2`.
- Analyzed variable importance to identify key features influencing predictions.

### **3. Model Building**
- Split the data into **70% training** and **30% validation** sets.
- Trained a **GBM** model with 5-fold cross-validation to optimize hyperparameters.

### **4. Evaluation**
- Evaluated model performance using:
  - Accuracy
  - Kappa statistic
  - Confusion matrix

### **5. Predictions**
- Used the trained model to predict the classes of the test dataset.
- Saved predictions in a `predictions.csv` file for submission.

---

## Results

### **Model Performance on Validation Data**
- **Accuracy**: 99.76%
- **Kappa**: 0.997

The confusion matrix and other statistics show that the model performs exceptionally well in classifying movements into their respective categories.

### **Feature Importance**
![image](https://github.com/user-attachments/assets/835d68c0-3b21-44b3-9004-c049302e9f06)

## Usage

### Prerequisites
- Install **R** and **RStudio**.
- Required R libraries:
  ```R
  install.packages(c("caret", "ggplot2", "gbm"))
