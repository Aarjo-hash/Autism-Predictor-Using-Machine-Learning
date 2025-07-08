# Autism Prediction Using Machine Learning

## Introduction

Autism Spectrum Disorder (ASD) is a developmental condition that affects communication, behavior, and social interaction. Diagnosing it early can make a big difference in outcomes, but it’s not always easy. In this project, I’ve built a machine learning-based prediction system that aims to help detect Autism using available data and ML techniques.

## Background

Autism was first formally described back in the 1940s by Dr. Leo Kanner and, separately, Dr. Hans Asperger. Over time, our understanding of it has evolved a lot — it’s now seen as a spectrum, where individuals can have very different strengths and challenges. Some may need lifelong support; others live independently. That wide range is what makes early detection so important.

## Why It Matters

The effects of Autism aren’t limited to the individual — families, education systems, and society are impacted too. Communication barriers, sensory overload, and social difficulties can make day-to-day life harder. Autism often appears alongside conditions like anxiety, epilepsy, or intellectual disabilities, so timely support matters.

There’s no “cure” for Autism, but it can be managed. With the right support, therapy, and education, individuals can improve key life skills. The goal here isn’t to label anyone — it’s to provide tools that can help spot early signs and get help sooner.

## About This Project

The idea is simple: build a machine learning model that can predict the likelihood of someone having Autism based on key features in a dataset. This kind of tool could eventually support healthcare workers, researchers, or even screening apps.

## Dataset

The dataset includes behavioral scores and personal factors that might relate to Autism. I cleaned the data, handled missing values, normalized features, and split it into training and testing sets to prepare it for modeling.

## Approach

Here’s how I went about it:

1. **Data Preprocessing** – cleaned up the dataset and made it model-ready.
2. **Feature Engineering** – selected and created the most relevant features.
3. **Modeling** – tested a few algorithms like Logistic Regression, Support Vector Machines (SVM), and XGBoost.
4. **Training & Validation** – split the dataset to evaluate performance fairly.
5. **Evaluation** – used metrics like accuracy to judge how well the model predicts.

## Steps Followed in This Project

Below is a high-level summary of what I did inside the notebook:

1. **Imported Required Libraries**  
   Brought in all necessary libraries like pandas, numpy, seaborn, sklearn, xgboost, and imblearn.

2. **Loaded the Dataset**  
   Read the dataset from CSV and displayed the first few rows for inspection.

3. **Initial Data Analysis**  
   - Checked shape, data types, and missing/null values.
   - Explored the distribution of classes (autistic vs non-autistic).

4. **Data Cleaning**  
   - Replaced "yes"/"no" with 1/0, and "?" or "others" with "Others".
   - Dropped irrelevant columns like `ID`, `age_desc`, etc.
   - Filtered out extreme outliers (e.g., result < -5).

5. **Feature Engineering**  
   - Created a new column `sum_score` which is the total of A1 to A10 scores.
   - Created another column `ind` combining `austim`, `used_app_before`, and `jaundice`.

6. **Exploratory Data Analysis (EDA)**  
   - Used countplots and pie charts to visualize distributions and class balance.
   - Used distribution plots and box plots to understand float features and detect outliers.

7. **Feature Transformation**  
   - Applied log transformation on `age` to reduce skew.
   - Label encoded the categorical (`object`) columns.

8. **Train-Test Split**  
   - Split the data into training and validation sets (80-20 split).
   - Addressed class imbalance using `RandomOverSampler`.

9. **Model Training**  
   - Trained multiple models: Logistic Regression, Support Vector Machine (SVM), and XGBoost.
   - Evaluated their performance using accuracy score and classification reports.

10. **Results and Conclusion**  
    - Best model achieved an accuracy between **80%–85%**.
    - Concluded that ML can assist in early autism detection, but further validation is needed.



## Results

The models performed well, with accuracy scores ranging between **80–85%**. That’s promising for something like this — it shows that machine learning can pick up on meaningful patterns when it comes to early signs of Autism.

## Conclusion

This project shows how machine learning can be a useful aid in the early detection of Autism. It’s not a replacement for professional diagnosis — but it could be a helpful tool in the process. There’s still more to be done to improve accuracy and reliability, especially in real-world use cases.

## Future Improvements

- Adding more diverse and larger datasets
- Including genetic, environmental, or medical history features
- Trying advanced models like deep learning
- Working with professionals in healthcare to validate predictions in clinical settings

