# 📝 Handling Missing Data – Titanic Dataset  
**Course:** INFO 7390 – Art and Science of Data  
**Name:** Siddi Kommuri  
**Date:** October 2025  

---

## 📌 Project Overview
This repository contains my submission for **Assignment 1: Writing a Chapter for "Understanding Data"**.  
The focus of this project is on **handling missing data** using different imputation strategies and evaluating their impact on downstream model performance.

The Titanic dataset was chosen as the real-world dataset for this assignment. Missing values were analyzed and handled using:
- **Median Imputation**
- **KNN Imputation**
- **Regression Imputation**

The effect of each strategy was evaluated using a Logistic Regression model, and their performances were compared visually.

---

## 📊 Dataset
**Source:** [Datasciencedojo Titanic Dataset](https://raw.githubusercontent.com/datasciencedojo/datasets/master/titanic.csv)  

The dataset contains information about Titanic passengers, including demographic details, ticket class, and survival status. Several columns, especially `Age`, `Cabin`, and `Embarked`, contain missing values — making this dataset ideal for studying imputation techniques.

---

## 🧪 Methodology

1. **Exploratory Data Analysis**  
   - Inspected missing value patterns using `.isnull()` and a heatmap.

2. **Preprocessing**  
   - Encoded categorical columns (`Sex`, `Embarked`) using `LabelEncoder` to prepare for imputation.

3. **Imputation Strategies**  
   - **Median Imputation:** Replaced missing numerical values with column medians.  
   - **KNN Imputation:** Used `KNNImputer` to fill missing values based on feature similarity.  
   - **Regression Imputation:** Trained a linear regression model to predict missing `Age` values.

4. **Model Training**  
   - Trained a Logistic Regression model on each imputed dataset to predict survival.

5. **Evaluation**  
   - Compared accuracy scores and plotted a bar chart to visualize performance differences.

---

## 📈 Results
| Imputation Method  | Accuracy |
|--------------------|----------|
| Median             | ~0.77    |
| KNN                | ~0.78    |
| Regression         | ~0.78    |

> **Observation:** KNN and Regression imputations performed slightly better than Median imputation, likely because they leverage more information from other features.

---

## 🧠 Key Learnings
- Handling missing data is not just about filling gaps — the choice of method **directly affects model accuracy**.  
- KNN and Regression methods, though more computationally involved, can preserve data relationships better than simple statistical imputation.  
- Data preprocessing (encoding, dropping irrelevant columns) is critical for imputation methods to work properly.

---

## 📂 Repository Structure

