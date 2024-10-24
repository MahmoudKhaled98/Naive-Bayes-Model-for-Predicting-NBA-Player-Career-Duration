# Naive Bayes Model for Predicting NBA Player Career Duration

## Project Overview
This project focuses on building a Naive Bayes model to predict whether an NBA player will have a career lasting five years or more. The analysis will help management and coaches in the NBA make informed decisions on player retention and recruitment by identifying players likely to have long-term success in the league. The dataset consists of 1,341 observations, each representing a player's rookie-year statistics, which are used to predict their career longevity.

## Table of Contents
- [Introduction](#introduction)
- [Step 1: Imports](#step-1-imports)
- [Step 2: Data Preparation](#step-1-data-preparation)
- [Step 3: Model Building](#step-2-model-building)
- [Step 4: Results and Evaluation](#step-3-results-and-evaluation)
- [Conclusion](#conclusion)
- [How to Run](#how-to-run)
- [References](#references)

## Introduction
In this project, I will build a **Naive Bayes model** to predict whether an NBA player will have a career lasting five years or more. The analysis will help management and coaches in the NBA make informed decisions on player retention and recruitment by identifying players likely to have long-term success in the league. The dataset consists of 1,341 observations, each representing a player's rookie-year statistics, which are used to predict their career longevity.

## Step 1: Imports


### Import Packages
To begin, I imported the necessary libraries for data manipulation, and model building:
- `pandas` for data handling
- `sklearn` for splitting the data and model training (`train_test_split`, `naive_bayes`, and `sklearn.metrics` for evaluation)

### Load the Dataset

In the project phase of feature engineering, I outputted features for the NBA player dataset along with the target variable `target_5yrs`. Data was imported as a DataFrame called `extracted_data`.

## Step 2: Data Preparation
- **Isolating Target and Features**: The target variable `target_5yrs` was separated from the predictor variables. The predictor variables are all continuous numeric values.
- **Train-Test Split**: The data was split into a training set `75%` of data and a test set `25%`. This allows the model to be evaluated on unseen data.
  - Training data: `1,005 rows`
  - Test data: `335 rows`

## Step 3: Model Building
- **Gaussian Naive Bayes**: Since the predictor variables are continuous, a Gaussian Naive Bayes model was chosen. The model assumes that the features follow a normal distribution, which may not always hold perfectly but still provides reliable results.
- The model was trained using the training data and tested on the reserved test data.

## Step 4: Results and Evaluation

- **Model Performance Metrics**:
  - **Accuracy**: The model achieved an accuracy score of `69%`, meaning that `69%` of all predictions were correct.
  - **Precision**: The precision score was `84%`, indicating that the model is quite good at identifying players who will play longer than five years. This reflects the model's ability to reduce false positives.
  - **Recall**: The recall score was `59%`, showing that the model had weaker performance in identifying players who will not have long careers (true negatives). It struggles more with false negatives, i.e., predicting that a player will last five years when they actually won’t.
  - **F1 Score**: The F1 score was `69%`, balancing precision and recall to give a more comprehensive evaluation of the model's performance.

- **Confusion Matrix Analysis**:
  - The confusion matrix showed a higher concentration of **true positives** (correctly predicted long-term players) than false positives (incorrectly predicting a long career).
  - **True negatives** and **false negatives** were closer in number, which explains the relatively lower recall score.

## Conclusion

- **Key Insights**:
  - **Accuracy**: `69%` of the model's predictions were correct, providing a reasonable indication of its overall performance.
  - **Precision**: The model's ability to accurately identify players likely to play more than five years `84%` is a strong point, suggesting it can help identify key players for long-term success.
  - **Recall**: The model has a weaker ability to correctly identify players who will not last five years, reflected by the recall score of `59%`.
  - **F1 Score**: At `69%`, the F1 score shows that the model strikes a reasonable balance between precision and recall, providing a more reliable measure of its effectiveness than accuracy alone.

- **Summary for Stakeholders**:
  - **Actionable Insights**: Management and coaches can use these results to make data-driven decisions about which players to retain and develop. The model provides useful predictions about players likely to last more than five years in the NBA.
  - **Future Improvements**: To improve recall and better identify players who will not succeed, additional features or different model architectures could be explored.
  - **Strategic Focus**: Given the model's strength in identifying potential long-term players, this tool can be integrated into recruitment strategies to identify and prioritize players with long-term potential.

## How to Run


1. **Clone the repository**:

    ```bash
    git clone <https://github.com/MahmoudKhaled98/Naive-Bayes-Model-for-Predicting-NBA-Player-Career-Duration.git>
    ```

2. **Install the required dependencies**:

    ```bash
    pip install -r requirements.txt
    ```

3. **Run the Jupyter notebook**:

    ```bash
    jupyter notebook
    
## References
- [Pandas Documentation](https://pandas.pydata.org/)

- [Scikit-learn Documentation](https://scikit-learn.org/stable/)

