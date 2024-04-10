# Petavue-AI Assignment

## Overview

The goal of this project is to predict flight delays using machine learning techniques. The dataset consists of flight information as well as weather data. We aim to merge these datasets, preprocess the data, train machine learning models, and evaluate their performance in predicting flight delays.

## Approach

1. **Data Preprocessing**:
    - We start by merging all the CSV files containing flight data into a single CSV file.
    - Next, we iterate through each row in the flight dataframe, fetch corresponding weather data, and store it in a list.
    - We extend our dataframe with the list containing weather information and save it as `merged_dataset.csv`.
    - Due to resource constraints, we sample a subset of the original dataset to prevent system freezing.
  
    - Merged_dataset link: https://drive.google.com/file/d/10cmyACVAX0hInfpoPMv8Khbe46ynhNjb/view?usp=sharing

2. **Feature Engineering**:
    - We drop unnecessary date columns as they are not relevant for prediction.
    - The dataset is then split into features (X) and target (y) variables.
    - Min-max scaling is applied to normalize the features.
    - One-hot encoding is used to encode categorical variables.

3. **Model Training and Evaluation**:
    - We train two machine learning models: XGBoost Classifier and Random Forest Classifier.
    - Evaluation is performed using the F1 score metric.
    - XGBoost Classifier achieves a F1 score of approximately 0.89, while Random Forest Classifier achieves around 0.65.

## Conclusion

- The XGBoost Classifier outperforms the Random Forest Classifier in predicting flight delays.
- Further optimization and fine-tuning of hyperparameters could potentially improve model performance.
