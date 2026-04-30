# NYC 311 Complaint Classification

This project analyzes NYC 311 service request data and builds machine learning models to classify complaint types from complaint descriptions.

## Project Overview

The goal of this project is to predict the `Complaint Type` based on the text in the `Descriptor` column. The notebook also includes exploratory data analysis, text preprocessing, n-gram analysis, model comparison, cross-validation, sentiment analysis, and priority mapping.

## Dataset

The dataset used is `NYC311data.csv`.

Main columns used:

- `Complaint Type`
- `Descriptor`
- `Borough`
- `Agency Name`

Only rows with valid `Descriptor` and `Complaint Type` values are used. For efficient processing, the notebook loads the first 10,000 rows.

## Features

- Data loading and cleaning
- Missing value analysis
- Complaint type distribution
- Borough-wise complaint analysis
- Text length analysis
- Word cloud visualization
- Unigram, bigram, and trigram frequency distributions
- TF-IDF feature extraction
- Train-test split
- 5-fold cross-validation
- Model comparison
- Sentiment analysis using TextBlob
- Priority mapping
- Final complaint prediction function

## Models Used

The notebook compares three classification models:

1. Logistic Regression
2. Naive Bayes
3. Linear SVM

The best model is selected based on cross-validation accuracy.

## Evaluation Metrics

Models are evaluated using:

- Accuracy
- Macro F1-score
- Weighted F1-score
- Classification report
- Confusion matrix
- Cross-validation mean accuracy
- Cross-validation standard deviation

## Workflow

1. Import required libraries
2. Load NYC 311 dataset
3. Inspect dataset structure and missing values
4. Clean data and select relevant columns
5. Perform EDA
6. Preprocess complaint text
7. Generate word cloud
8. Analyze n-gram frequencies
9. Convert text using TF-IDF
10. Split data into train and test sets
11. Perform cross-validation
12. Train and evaluate all models
13. Select the best model
14. Add sentiment and priority labels
15. Predict complaint type for new text

## Example Prediction

```python
predict_complaint('Street light not working for 3 days')
