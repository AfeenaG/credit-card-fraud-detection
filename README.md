# Fraud Detection Using Machine Learning & Streaming
## Project Overview
This project focuses on building a scalable fraud detection system using machine learning and real-time data processing. The solution leverages historical transaction data to train predictive models capable of identifying fraudulent behavior, and then applies these models to streaming data to simulate real-time fraud detection.

The system is designed using a big data architecture, integrating distributed processing and streaming technologies to handle high-volume transaction data efficiently. The end-to-end pipeline includes data ingestion, model training, real-time prediction, and storage of results for further analysis.

## Business Problem

Financial fraud is a major challenge for organizations, leading to significant monetary losses and reputational damage. Traditional rule-based systems are often insufficient because:

- Fraud patterns evolve rapidly

- High false positives impact customer experience

The goal of this project is to:

- Accurately detect fraudulent transactions in real time

- Minimize false positives while maintaining high recall

- Provide a scalable solution that can handle continuous streams of transaction data

By implementing a machine learning-based approach, the system can learn hidden patterns and adapt better to new fraud behaviors compared to traditional methods.

# Project Structure

```text
toronto-traffic-injury-risk-analysis
│
├── README.md
├── data
│   └── CreditFraud.csv
├── Notebooks
│   ├── FraudDetection.ipynb
│
├── outputs
└── report
    └──<UNDER CONSTRUCTION>.pdf
```
## Dataset
The data set used was an open dataset "Credit Card Fraud Detection" https://www.kaggle.com/datasets/kartik2112/fraud-detection?select=fraudTest.csv

## Analytical Approach
The data contained a series of numerical, categorical data that needed to be transformed. Since the aim of this project is a binary classification, three models were analysed: SVM, Logistical regression, random forest.

# Data Processing

Data cleaning and preprocessing performed using distributed data frameworks

Feature scaling applied where necessary

Handling of class imbalance (fraud cases are rare) using appropriate techniques

3.3 Model Development

Multiple machine learning models were trained and evaluated, including:

- Logistic Regression

- Random Forest

- Support Vector Machine (SVM)

Performance was measured using:

- AUC (Area Under the Curve)

- Precision and Recall

The best-performing model (Random Forest) achieved the highest AUC and was selected for deployment.

3.4 Real-Time Streaming Pipeline

To simulate real-time fraud detection:

- Historical data (fraudTest.csv) was fed into different model
- Trained model was determined
- The same dataset was streamed into the trained model
- Predictions are generated in "real time"

## Key components:

- Streaming engine processes incoming data

- Model inference layer applies fraud prediction

- Output includes predicted is_fraud label

## Data Storage

Results are stored in a NoSQL database (e.g., MongoDB)

- Each processed transaction includes:

- Original transaction data

- Predicted fraud label


## System Architecture

The system follows a pipeline architecture:

Data Source → Streaming Engine → ML Model → Prediction Output → Database

This design ensures scalability, flexibility, and real-time processing capability.

## Key Results

Random Forest model achieved the highest predictive performance

High AUC indicates strong ability to distinguish fraud vs. non-fraud

Real-time simulation demonstrates feasibility of production deployment

## Future Improvements

Incorporate deep learning models for improved accuracy

Use real-time data sources instead of simulated streams

Implement alerting/notification system for detected fraud

Enhance feature engineering with domain-specific insights

# Technologies Used

- Python

- Apache Spark (PySpark)

- Machine Learning (Scikit-learn)

- Streaming (Spark Structured Streaming)

- MongoDB


