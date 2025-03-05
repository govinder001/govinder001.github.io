---
layout: post
author: Govinder Pal Singh
title: "Applied Data Science Project Documentation"
categories: ITD214
---
## Project Background
This project involves a dataset of mental health-related statements from sources like Reddit and Twitter. It includes data on mental health conditions such as depression, anxiety, stress, and suicidal thoughts. Each statement is labeled with one of seven mental health statuses: Normal, Depression, Suicidal, Anxiety, Stress, Bipolar, or Personality Disorder. This dataset is useful for creating mental health chatbots, analyzing trends in mental health, and developing machine learning models to predict mental health conditions based on text data.



## Work Accomplished
### Data Preparation
The dataset was downloaded from Kaggle and loaded for analysis.
Basic cleaning was done by checking for missing data and removing it.
A new feature, "statement length," was added to count the number of words in each statement.
The text data was cleaned by removing URLs, social media handles, and extra spaces, and transforming the text to lowercase.
Stopwords (common words like "and," "the," etc.) were removed to focus on important words.
Words were reduced to their root forms (e.g., "running" to "run") using a technique called stemming.
To balance the dataset (since some mental health conditions are more common than others), oversampling was used to make the data more equal.

### Modelling
Two machine learning models were tested:
Logistic Regression: A simpler model used as a baseline.
XGBoost: A more complex model that is better at handling difficult cases and is faster because it uses GPU acceleration.
The mental health status labels were converted into numbers using a method called encoding.
The text was split into individual words (tokenized), and different techniques were used to turn the text into numbers that the models can understand, such as Count Vectorization and TF-IDF.

### Evaluation
Overall Accuracy - Both models (Logistic Regression and XGBoost) achieved an accuracy of 76%.
Class-wise Performance:
XGBoost generally performed better, especially at detecting more cases (called recall).
For some conditions like Depression and Anxiety, Logistic Regression had higher precision (fewer false positives), but XGBoost was better overall at catching more cases.
Findings
XGBoost tends to perform better in identifying cases of mental health issues, especially in terms of recall (detecting as many cases as possible).
Logistic Regression was better for precision in a few areas, such as Depression and Anxiety, where it's important to avoid false positives.


## Recommendation and Analysis
Model Selection for Deployment
Since XGBoost performs better at identifying mental health issues overall, it should be the main model used in real-world applications.
However, combining Logistic Regression and XGBoost could be explored to improve precision in some areas.
Improving Model Performance
To reduce missed cases (false negatives), techniques like adjusting decision thresholds or cost-sensitive learning could be used.
Adding more data or using techniques like text augmentation could improve the model's accuracy further.
Fine-tuning XGBoost's settings through optimization could improve its performance.




## AI Ethics
It is important to make sure the dataset doesn’t contain biased or sensitive information that could lead to ethical concerns.
Fairness and transparency should be prioritized in developing models to avoid reinforcing stereotypes.
If using AI for mental health analysis, clear disclaimers should be provided, and the limitations of the models should be emphasized.
AI should not be relied on too heavily in sensitive situations, as human context and understanding are crucial in mental health discussions.


## Source Codes and Datasets
(_Upload your model files and dataset into a GitHub repo and add the link here. _)
https://github.com/govinder001/ITD214-Mental-Health
