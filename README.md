# Credit Risk Prediction - Machine Learning Project

## Project Overview

This project analyzes the German Credit dataset to build machine learning models that predict credit risk for loan applicants.

The goal is to classify applicants into:

- Low Risk
- High Risk

Two machine learning models were implemented:

- Logistic Regression
- Random Forest

## Dataset

German Credit Dataset  
https://archive.ics.uci.edu/dataset/144/statlog+german+credit+data

The dataset contains financial information about loan applicants including credit amount, employment status, savings, and age.

## Project Structure


credit-risk-project
│
├── data
│ └── german.data-numeric
│
├── notebooks
│ └── credit_risk_analysis.ipynb
│
├── src
│ └── preprocessing.py
│
├── report
│ └── Project1_Report.pdf
│
├── README.md
└── requirements.txt


## Installation

Clone the repository:


git clone https://github.com/yourusername/credit-risk-project.git


Navigate to the project folder:


cd credit-risk-project


Create virtual environment:


python -m venv venv


Activate environment:

Mac/Linux:


source venv/bin/activate


Install dependencies:


pip install -r requirements.txt


## Running the Project

Open the notebook:


notebooks/credit_risk_analysis.ipynb


Run all cells to reproduce the analysis and model training.

## Models Implemented

- Logistic Regression
- Random Forest

## Evaluation Metrics

- Accuracy
- Confusion Matrix
- ROC Curve
- Cross Validation

## Author

Rafaela Hollanda  
MS Computer Science – Pace University