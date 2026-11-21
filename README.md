## Blockchain Healthcare Dataset

### 1. Dataset Overview

The **Blockchain Healthcare Dataset** is a structured dataset designed to support the application and evaluation of Machine Learning (ML) techniques in blockchain-enabled healthcare systems. It contains 5,000 records and 7 features representing blockchain adoption, trust, data integrity, transaction performance, fraud incidents, patient satisfaction, and stakeholder participation.

The dataset can be used to investigate relationships between blockchain implementation and important healthcare system performance indicators.

### 2. Dataset Specifications

| Property | Description |
|---|---|
| Dataset Name | Blockchain Healthcare |
| Total Records | 5,000 |
| Total Features | 7 |
| Missing Values | 0 |
| Data Format | Structured Tabular Data |
| Numerical Features | 7 |
| Categorical Features | 0 (blockchain is binary encoded) |
| Target Variable | Blockchain (binary classification, if selected) |

### 3. Feature Description

| Feature | Data Type | Description |
|---|---|---|
| `blockchain` | Integer | Indicates blockchain adoption (0 = No, 1 = Yes). |
| `trust_score` | Float | Represents the trust level within the healthcare system. |
| `data_integrity` | Float | Measures the integrity and reliability of healthcare data. |
| `transaction_time` | Float | Represents the time required to process transactions. |
| `fraud_incidents` | Integer | Number of reported fraud incidents. |
| `patient_satisfaction` | Float | Represents the patient satisfaction score. |
| `stakeholders` | Integer | Number of stakeholders participating in the healthcare system. |

### 4. Sample Dataset (First Five Records)

| Blockchain | Trust Score | Data Integrity | Transaction Time | Fraud Incidents | Patient Satisfaction | Stakeholders |
|---:|---:|---:|---:|---:|---:|---:|
| 0 | 44.03 | 69.27 | 4.09 | 5 | 4.32 | 69 |
| 1 | 56.10 | 91.74 | 3.95 | 1 | 5.77 | 90 |
| 1 | 75.88 | 85.06 | 3.27 | 4 | 7.64 | 37 |
| 1 | 89.13 | 89.26 | 5.70 | 2 | 6.88 | 62 |
| 0 | 55.38 | 69.00 | 16.57 | 6 | 4.12 | 22 |

### 5. Descriptive Statistical Analysis

The following table presents the descriptive statistics of the dataset.

| Statistic | Blockchain | Trust Score | Data Integrity | Transaction Time | Fraud Incidents | Patient Satisfaction | Stakeholders |
|---|---:|---:|---:|---:|---:|---:|---:|
| Mean | 0.50 | 64.82 | 80.01 | 7.54 | 3.98 | 6.48 | 52.13 |
| Std. Dev. | 0.50 | 17.98 | 11.11 | 3.21 | 2.24 | 1.82 | 27.71 |
| Minimum | 0 | 11.63 | 53.12 | -2.27 | 1 | 1.55 | 5 |
| 25% | 0 | 49.80 | 70.03 | 5.01 | 2 | 4.95 | 28 |
| Median | 0.50 | 64.70 | 79.93 | 7.54 | 5 | 6.47 | 52 |
| 75% | 1 | 79.84 | 90.04 | 10.03 | 6 | 8.00 | 76 |
| Maximum | 1 | 115.29 | 106.42 | 18.96 | 11 | 11.35 | 99 |

### 6. Data Quality and Preprocessing

Initial data inspection indicates:

- Total records: 5,000.
- Total features: 7.
- Missing values: None.
- Duplicate records: Not yet assessed.
- All features are stored in numerical format.
- The `blockchain` feature is binary encoded.

**Data quality consideration:** The `transaction_time` feature contains negative values, while some scores exceed their apparent conventional ranges. These observations should be investigated before model training to determine whether they represent valid measurements or synthetic data-generation artefacts.

### 7. Potential Machine Learning Applications

The dataset can support several ML research directions:

1. **Binary Classification:** Predict blockchain adoption using healthcare system indicators.
2. **Regression:** Predict patient satisfaction, trust scores, or transaction time.
3. **Fraud Analysis:** Investigate patterns associated with healthcare fraud incidents.
4. **Clustering:** Identify groups of healthcare systems based on trust, integrity, and operational performance.
5. **Feature Importance:** Examine which indicators are most strongly associated with blockchain adoption.
6. **Comparative Analysis:** Compare healthcare system indicators between blockchain and non-blockchain observations.

### 8. Machine Learning Algorithms

Potential algorithms for experimentation include:

- Logistic Regression
- Decision Tree
- Random Forest
- Support Vector Machine (SVM)
- K-Nearest Neighbors (KNN)
- XGBoost
- LightGBM
- Gradient Boosting
- Artificial Neural Networks (ANN)

### 9. Research Scope

This dataset provides an opportunity to explore how machine learning can be applied to blockchain-enabled healthcare environments. The analysis can focus on blockchain adoption, healthcare data integrity, trust, fraud-related indicators, transaction efficiency, and patient satisfaction.

**Note:** The dataset contains observational records. Predictive associations should not be interpreted as evidence of causal effects of blockchain technology.

## 11. Data Visualization and Experimental Analysis

### Feature Correlation Heatmap
![Correlation Heatmap](images/correlation_heatmap.png)

### Model Accuracy Comparison
![Model Accuracy](images/model_accuracy.png)

### ROC Curve Comparison
![ROC Curves](images/roc_curves.png)

### Confusion Matrix Analysis
![Confusion Matrices](images/confusion_matrices.png)

### Cross-Validation Performance
![Cross Validation](images/cross_validation.png)

### Feature Importance
![Feature Importance](images/feature_importance.png)
