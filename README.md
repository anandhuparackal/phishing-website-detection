# Phishing Website Detection 

This repository contains the complete implementation of a phishing website detection system developed using three machine learning models — Convolutional Neural Network (CNN), Multi-Layer Perceptron (MLP), and Support Vector Machine (SVM). The project culminates in a **weighted soft voting ensemble** model that improves performance by combining all three classifiers.


## Project Overview
Phishing websites trick users into revealing sensitive information. This project uses machine learning to automatically detect such websites. It compares individual models and demonstrates how an ensemble approach boosts accuracy and reduces false positives.


## Dataset
- **Source**: [Kaggle - Phishing Site URLs Dataset](https://www.kaggle.com/datasets/taruntiwarihp/phishing-site-urls)
- **Entries**: 549,346
- **Labels**: "Good" = 1, "Bad" = 0



## Models Used

- **CNN**: Character-level model with 1D convolution trained on padded URL tokens.
- **MLP**: Feature-based model using URL length, special characters, entropy, etc.
- **SVM**: RBF kernel with tuned hyperparameters.
- **Ensemble**: Weighted soft voting strategy (CNN: 0.6, MLP: 0.3, SVM: 0.1).


## Performance Summary

| Model    | Accuracy | Phishing F1 | Legitimate F1 |
|----------|----------|-------------|----------------|
| CNN      | 96.25%   | 93%         | 97%            |
| MLP      | 84.88%   | 69%         | 90%            |
| SVM      | 72.57%   | 68%         | 76%            |
| Ensemble | 96.16%   | 93%         | 97%            |


## Real-Time Testing
A set of URLs was tested using the final ensemble model. These tests confirmed the model’s ability to correctly identify both phishing and legitimate sites. Screenshots and results are available in the appendix of the project report.
