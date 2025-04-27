#Topic:Phishing Website Detection using an Ensemble Machine Learning Approch.

# Aim
The project aims to build a phishing website detection system by combining Convolutional Neural Network (CNN), Multi-Layer Perceptron (MLP), and Support Vector Machine (SVM) models into a weighted soft voting ensemble. The goal is to improve phishing detection accuracy and reduce false positives compared to using standalone models.

#Data Used
Dataset: Phishing Site URLs Dataset-https://www.kaggle.com/datasets/taruntiwarihp/phishing-site-urls
Source: Kaggle (over 549,000 URLs labeled as "phishing" or "legitimate")

#Features:
Raw URLs (for CNN input)
Engineered features like URL length, entropy, subdomain count, special character counts, HTTPS presence, etc. (for MLP and SVM)

#Input Format
Input: A URL string (e.g., https://example.com/login)
Format: Plain text string.

#Output Format
Output:
Predicted label: "phishing" or "legitimate"
Evaluation metrics: Accuracy, Precision, Recall, F1-Score.
Model comparison: CNN vs. MLP vs. SVM vs. Ensemble.

#Repository Structure
Data preprocessing/: Scripts for cleaning and feature engineering
Model Development CNN/MLP/SVM/: Building individual models
TUNED CNN/MLP/SVM/: CNN/MLP/SVM models with optimized hyperparameters
TUNED ENSEMBLE MODEL/: Weighted soft voting ensemble integration
ensemble model development/: Scripts for final ensemble assembly
FINAL RESULT VALUATION/: Model evaluation results and confusion matrices
requirements.txt: Python library requirements

#Code Structure
Data analysis
Data preprocessing
cnn_model.py – Builds and trains the CNN model.
mlp_model.py – Builds and trains the MLP model.
svm_model.py – Builds and trains the SVM model.
ensemble_model.py – Combines predictions using weighted soft voting (CNN: 0.6, MLP: 0.3, SVM: 0.1).
live_prediction.py – Takes a URL as input and outputs ensemble prediction.

#How It Works
Step 1: Preprocess and extract features from the dataset.
Step 2: Train CNN, MLP, and SVM models individually.
Step 3: Combine predictions using weighted soft voting to form the ensemble model.
Step 4: compare the models accuracy.
step 5: Test the ensemble model.
