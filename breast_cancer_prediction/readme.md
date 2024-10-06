# Breast Cancer Prediction Using Decision Trees

## Introduction

This project aims to predict breast cancer using the Decision Tree algorithm. Breast cancer prediction is a critical task in healthcare, and machine learning can help automate the process and make it more accurate. In this project, we use a dataset of breast cancer features to train a Decision Tree classifier to predict whether a breast tumor is malignant or benign.

## Dataset

The dataset used in this project is the Breast Cancer Wisconsin (Diagnostic) Data Set, which is available in the Scikit-Learn library. This dataset contains features such as mean radius, mean texture, mean smoothness, and more. The target variable indicates whether the tumor is malignant (1) or benign (0).

## Project Structure

The project structure is organized as follows:

- `breast_cancer_decision_tree.ipynb`: Jupyter Notebook containing the code for data preprocessing, model training, and evaluation.

## Data Preprocessing

Data preprocessing is a crucial step in preparing the dataset for training. It involves:

- Loading and exploring the dataset.
- Handling missing values if any.
- Encoding categorical features.
- Splitting the data into training and testing sets.

## Model Training

In this project, we use the Decision Tree classifier provided by Scikit-Learn. The model is trained using the training data.

## Model Evaluation

The trained model is evaluated using various metrics such as accuracy, precision, recall, and F1-score. Additionally, a confusion matrix is generated to visualize the model's performance.

## Dependencies

The following Python libraries and tools are used in this project:

- Scikit-Learn
- Pandas
- Matplotlib
- Jupyter Notebook


