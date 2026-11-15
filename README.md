# Bank Marketing – Machine Learning Classification

**Data Analytics & Machine Learning (DAML)**  
CentraleSupélec – Université Paris-Saclay  
October 2026

## 1. Project Overview

This academic group project focuses on predicting whether bank customers will subscribe to a term deposit using machine learning techniques.

The objective is to identify potential subscribers before a marketing call and evaluate how different machine learning models perform under different data-splitting strategies.

## 2. Dataset

**UCI Bank Marketing Dataset**

- Dataset: `bank-full.csv`
- Number of observations: 45,211
- Task: Binary classification
- Target variable: Term deposit subscription (yes/no)

The call duration variable was excluded to avoid using information unavailable before the call.

**Dataset source:** https://archive.ics.uci.edu/dataset/222/bank+marketing

## 3. Data Preprocessing

The preprocessing steps include:

- Data quality assessment and cleaning
- Handling categorical variables
- Feature engineering
- One-hot encoding
- Numerical standardization
- Prevention of data leakage

## 4. Data Splitting

Two evaluation strategies were investigated:

**Chronological Split**
- Training: 70%
- Validation: 15%
- Testing: 15%
- Preserves the original chronological ordering

**Stratified Random Split**
- Training: 70%
- Validation: 15%
- Testing: 15%
- Maintains approximately the same target-class proportions across subsets

The two strategies were compared to investigate the impact of temporal distribution changes on model performance.

## 5. Machine Learning Models

Six classification models were evaluated:

1. Logistic Regression (L1/L2 regularization)
2. k-Nearest Neighbors (kNN)
3. Decision Tree
4. Random Forest
5. AdaBoost
6. Support Vector Machine (SVM)

## 6. Results

The evaluation revealed substantial differences between chronological and stratified random splitting.

| Model | Chronological ROC-AUC | Stratified ROC-AUC |
|---|---:|---:|
| Logistic Regression | 0.630 | 0.769 |
| Random Forest | 0.593 | 0.786 |
| Decision Tree | 0.583 | 0.767 |
| AdaBoost | 0.568 | 0.773 |
| SVM | 0.567 | 0.770 |
| kNN | 0.554 | 0.761 |

The chronological evaluation was particularly challenging because of a substantial shift in the positive-class proportion between training and testing data.

## 7. My Contributions

My main responsibilities in this group project included:

- Data preparation and cleaning
- Feature preprocessing
- Implementing the train, validation, and test data splits
- Preparing datasets for machine learning experiments

## 8. Project Files

The complete project is available in:

**[DAML_Groupe5.zip](DAML_Groupe5.zip)**

The archive contains the project implementation and supporting documentation.

To reproduce the experiments:

1. Download and extract the archive.
2. Obtain `bank-full.csv` from the UCI Machine Learning Repository.
3. Open the relevant project notebook in Google Colab.
4. Upload the dataset when prompted.
5. Execute the notebook cells in order.

The notebooks implement different data-splitting strategies.

## 9. Academic Context

This work was completed as a group mini-project for the Data Analytics & Machine Learning course at CentraleSupélec, Université Paris-Saclay.

**Project type:** Academic group project  
**Year:** 2026  
**Repository visibility:** Private
