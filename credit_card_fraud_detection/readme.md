## Credit Card Fraud Detection
- **This project implements a credit card fraud detection system using machine learning techniques. It preprocesses the dataset, applies various classifiers, and uses techniques for handling imbalanced datasets.

## Table of Contents
1. Installation
2. Data Description
3. Project Structure
4. Steps
5. Results
6. Model Persistence
7. License

# 1. Installation
To run this project, you'll need to install the following Python packages:

bash
Copy code
-** pip install pandas scikit-learn seaborn matplotlib imbalanced-learn
You can also upgrade specific packages if needed:

bash
Copy code
pip install --upgrade scikit-learn imbalanced-learn
Data Description
The dataset used in this project is a credit card transaction dataset. The key features are:

Time: Time in seconds from the first transaction
V1, V2, ..., V28: 28 anonymized features generated from PCA
Amount: Transaction amount
Class: Target variable (1 for fraudulent transactions, 0 for legitimate transactions)
Dataset Information
Shape: The dataset has [number_of_rows] rows and [number_of_columns] columns.
Missing Values: The dataset has been checked for missing values and duplicates.
Project Structure
bash
Copy code
.
├── creditcard.csv             # Dataset file
├── credit_card_model.pkl      # Serialized model file
└── credit_card_detection.py    # Python script for detection
# Steps
Data Loading: Load the dataset using pandas.
# Data Preprocessing:
Standardize the 'Amount' feature.
Drop the 'Time' feature.
Check for and remove duplicates.
Class Distribution Visualization: Use Seaborn to visualize the count of classes.
Train-Test Split: Split the dataset into training and testing sets.
# Model Training:
Implement Logistic Regression and Decision Tree Classifier.
Evaluate models using accuracy, precision, recall, and F1-score.
# Handling Imbalanced Data:
Undersampling: Sample the majority class.
Oversampling: Use SMOTE (Synthetic Minority Over-sampling Technique) to generate synthetic examples of the minority class.
Final Model Evaluation: Train the classifiers on the balanced dataset and evaluate their performance again.
# Results
The models are evaluated based on:

-** Accuracy
-** Precision
-** Recall
-** F1-score
-** The results will be printed in the console for each classifier during training.

# Model Persistence
-** The Decision Tree Classifier is saved as a pickle file (credit_card_model.pkl) for later use. You can load the model using the following code snippet:

python
Copy code
import joblib
model = joblib.load("credit_card_model.pkl")

# License
This project is licensed under the MIT License - see the LICENSE file for details.










