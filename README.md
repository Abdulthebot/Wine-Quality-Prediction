# Wine Quality Prediction using Machine Learning

A comprehensive data science project to classify red wine quality based on its physicochemical properties. This repository demonstrates a full machine learning workflow, including data exploration, preprocessing, model comparison, and interpretation of results.

![Correlation Heatmap](https://i.imgur.com/gK2BwV7.png)
*(To make this work, take a screenshot of the correlation heatmap from your notebook, upload it to a site like Imgur, and paste the link here.)*

## Core Task
The goal is to build an efficient classifier to distinguish between 'good' (quality score >= 7) and 'poor' quality red wines.

## The Process
1.  **Exploratory Data Analysis (EDA):** A deep dive into the dataset to uncover correlations and patterns. Key insights revealed that `alcohol` and `sulphates` are positively correlated with quality, while `volatile acidity` is negatively correlated.
2.  **Preprocessing:** The target variable was binarized into two categories (good/poor), and features were scaled using `StandardScaler`.
3.  **Model Comparison:** Three classification models were implemented and evaluated:
    * Logistic Regression
    * Support Vector Machine (SVM)
    * [cite_start]Random Forest Classifier [cite: 34]
4.  **Results:** The Random Forest model achieved the highest accuracy and F1-score, making it the most effective classifier for this task.

## Key Findings & Actionable Insights
The most influential factors in determining wine quality were identified using the Random Forest model's feature importance scores.
- **Top Predictors:** `alcohol`, `sulphates`, `volatile acidity`, `total sulfur dioxide`.
- **Business Value:** These insights can help wineries focus on specific chemical attributes during production to consistently achieve higher-quality products.

## How to Run
1.  Clone this repository.
2.  Install the required libraries: `pip install -r requirements.txt`.
3.  Download the dataset from [Kaggle](https://www.kaggle.com/datasets/uciml/red-wine-quality-cortez-et-al-2009) and place `winequality-red.csv` in the root directory.
4.  Run the `wine_quality_analysis.ipynb` Jupyter Notebook.

## Architect's Notes
This project emphasizes the importance of a structured workflow. While the final model is important, the true value lies in the insights generated during EDA and feature analysis. The decision to binarize the 'quality' score transformed a complex regression problem into a clear, actionable classification task, which is often more useful in a business context.
