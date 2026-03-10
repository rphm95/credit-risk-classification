# Project 1 – Credit Risk Prediction Using Machine Learning

**Author:** Rafaela Hollanda
**Program:** MS Computer Science – Pace University
**Course:** Introduction to Deep Learning
**Project:** Project 1 – Credit Risk Analysis

---

# 1. Dataset Explanation

## Dataset Description

This project uses the **German Credit dataset**, a well-known dataset used in financial risk modeling and machine learning research. The dataset contains financial and demographic information about individuals who applied for credit. The goal of the dataset is to determine whether a loan applicant represents a **good credit risk or a bad credit risk**.

Credit risk prediction is a critical task for financial institutions. Banks must evaluate loan applications and determine the likelihood that a borrower will repay their loan. Machine learning models can assist in this process by identifying patterns in historical credit data.

The dataset used in this project is the **German Credit Data**, which has been widely used for classification problems related to credit risk.

## Dataset Size

The dataset contains:

* **1000 rows** representing individual loan applicants
* **25 columns** representing financial attributes and the target variable

Each row corresponds to one loan application and contains numerical information describing the applicant's financial situation.

## Important Features

Several variables in the dataset help describe the financial profile of each applicant. Some of the most relevant variables include:

| Feature          | Description                                   |
| ---------------- | --------------------------------------------- |
| duration         | Length of the loan in months                  |
| credit_amount    | Total amount of credit requested              |
| savings          | Amount of savings held by the applicant       |
| employment       | Duration of current employment                |
| installment_rate | Installment payment as a percentage of income |
| residence_since  | Length of time living at current residence    |
| age              | Age of the applicant                          |
| existing_credits | Number of existing credit accounts            |

These features help determine the financial stability of a borrower and are important indicators used in credit risk assessment.

## Target Variable

The target variable in this dataset is:

**risk**

In the original dataset the values are defined as:

* **1 = Good credit**
* **2 = Bad credit**

For the purposes of machine learning modeling in this project, the target variable was transformed into a binary format:

* **0 = Low Risk (good credit)**
* **1 = High Risk (bad credit)**

This transformation allows the dataset to be treated as a **binary classification problem**, where the goal is to predict whether an applicant is likely to represent a high credit risk.

---

# 2. Data Cleaning

Data cleaning is an important step in any machine learning project because it ensures that the dataset is accurate and suitable for analysis.

Several checks were performed during the data cleaning stage.

## Checking for Missing Values

The dataset was first examined for missing values using built-in data inspection functions. After reviewing the dataset, it was determined that **no missing values were present**. This means all observations contained valid data for each feature.

Because no missing values were detected, no imputation or data replacement was required.

## Duplicate Records

The dataset was also checked for duplicate rows. Duplicate records can negatively impact model training because they may bias the model toward repeated observations.

Any duplicate rows found were removed from the dataset to ensure that each record represented a unique loan application.

## Data Format

The dataset used in this project was already converted into a **numeric format**, which made it compatible with machine learning algorithms. Since the features were already encoded numerically, no additional categorical encoding was necessary.

## Outlier Inspection

Basic statistical summaries and visual inspection were used to detect potential outliers in the data. Although some values appeared larger than others, no extreme anomalies were identified that required removal.

Overall, the dataset required minimal cleaning and was ready for analysis after these checks.

---

# 3. Problem Statement

Financial institutions must evaluate loan applications to determine whether an applicant is likely to repay their loan or default. Incorrect lending decisions can lead to significant financial losses for banks.

The objective of this project is to develop a **machine learning model capable of predicting credit risk** based on historical financial data.

From a data analyst's perspective, the goal is to analyze the dataset and identify patterns that indicate whether a borrower represents a high or low credit risk. By training classification models on historical credit data, it is possible to automate part of the loan evaluation process.

Accurate credit risk prediction can help financial institutions:

* Reduce the probability of loan defaults
* Improve decision making in loan approvals
* Identify high-risk applicants more efficiently

The main goal of this project is therefore to build and compare machine learning models that can effectively classify loan applicants into **low risk or high risk categories**.

---

# 4. Preprocessing and Exploratory Data Analysis (EDA)

Before building machine learning models, the dataset underwent several preprocessing steps and exploratory data analysis techniques.

## Target Variable Transformation

The target variable originally used values of 1 and 2 to represent credit risk categories. In order to apply binary classification models, the variable was converted so that:

* **0 represents low credit risk**
* **1 represents high credit risk**

This transformation simplifies interpretation of model predictions.

## Feature and Target Separation

The dataset was separated into two components:

* **Features (X)** – all explanatory variables used to predict credit risk
* **Target variable (y)** – the risk column

This step prepares the dataset for machine learning model training.

## Exploratory Data Analysis

Exploratory Data Analysis was performed to better understand the dataset and identify potential patterns.

Several visualizations were created:

### Class Distribution

A class distribution plot was generated to analyze how many applicants fall into each risk category. This helps determine whether the dataset is balanced or imbalanced.

Understanding class balance is important because heavily imbalanced datasets can cause models to favor the majority class.

### Correlation Heatmap

A correlation heatmap was created to visualize relationships between the variables in the dataset. This helps identify whether certain financial attributes are strongly related to each other or to the target variable.

Understanding correlations can provide insights into which variables may have the strongest influence on credit risk.

### Age Distribution by Risk

A boxplot comparing age and risk categories was also created. This visualization helps examine whether certain age groups show different risk patterns.

Exploratory analysis like this helps build intuition about the dataset before training predictive models.

---

# 5. Models Used

Two machine learning models were implemented in this project:

* **Logistic Regression**
* **Random Forest Classifier**

These models were chosen because they represent two different approaches to classification.

## Logistic Regression

Logistic Regression is one of the most common algorithms used for binary classification problems. It estimates the probability that an observation belongs to a specific class based on the input variables.

Logistic Regression serves as a strong baseline model because it is simple, interpretable, and efficient.

## Random Forest

Random Forest is an **ensemble learning algorithm** that combines multiple decision trees. Each tree makes a prediction, and the final result is determined by aggregating those predictions.

Random Forest models are often able to capture complex relationships in data that simpler models may miss.

## Train-Test Split

To evaluate the models properly, the dataset was divided into:

* **80% training data**
* **20% testing data**

The training dataset was used to train the models, while the testing dataset was used to evaluate how well the models perform on unseen data.

---

# 6. Model Comparison

The performance of the models was evaluated using several metrics.

## Accuracy

Accuracy measures the proportion of correct predictions made by the model. It is calculated as the number of correct predictions divided by the total number of predictions.

Both Logistic Regression and Random Forest models were evaluated using accuracy scores.

## Confusion Matrix

A confusion matrix was used to evaluate the types of classification errors made by the model.

The confusion matrix shows:

* True Positives
* True Negatives
* False Positives
* False Negatives

This provides deeper insight into how the model performs when identifying high-risk borrowers.

## Classification Report

The classification report provides additional metrics including:

* Precision
* Recall
* F1-Score

These metrics provide a more detailed evaluation of model performance beyond simple accuracy.

## ROC Curve

A Receiver Operating Characteristic (ROC) curve was generated to visualize how well the model distinguishes between high-risk and low-risk applicants.

The Area Under the Curve (AUC) value measures the overall quality of the model's predictions. Higher AUC values indicate better model performance.

## Cross Validation

Cross-validation was also performed to evaluate the reliability of the model.

In cross-validation, the dataset is divided into multiple subsets, and the model is trained and tested multiple times using different splits of the data. This helps ensure that the model's performance is consistent and not dependent on a single train-test split.

---

# 7. Conclusion

The results of the model evaluation showed that the **Random Forest model performed better than Logistic Regression** for this dataset.

Random Forest achieved higher predictive accuracy and demonstrated a stronger ability to capture relationships between financial variables and credit risk.

Additionally, the ROC curve and cross-validation results indicated that the model maintained consistent performance across different training and testing splits.

The results suggest that ensemble learning methods such as Random Forest are well suited for credit risk prediction tasks.

Machine learning models like the ones developed in this project can support financial institutions in making more informed lending decisions, reducing financial risk, and improving the efficiency of credit approval processes.

Overall, this project demonstrates how data analysis and machine learning techniques can be applied to real-world financial problems such as credit risk assessment.
