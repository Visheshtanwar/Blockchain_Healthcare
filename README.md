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
## 10. Machine Learning Experimental Results

### 10.1 Experimental Setup

Six machine learning algorithms were implemented and evaluated to investigate their performance in predicting blockchain adoption in healthcare systems.

The dataset was divided into training and testing subsets using an 80:20 split.

| Parameter | Value |
|---|---|
| Total Samples | 5,000 |
| Input Features | 6 |
| Training Samples | 4,000 |
| Testing Samples | 1,000 |
| Training Percentage | 80% |
| Testing Percentage | 20% |
| Number of Classes | 2 |
| Evaluation Strategy | Cross-validation and independent test evaluation |

**Evaluated Machine Learning Algorithms:**

1. Logistic Regression
2. Random Forest
3. XGBoost
4. Support Vector Machine (SVM)
5. K-Nearest Neighbors (KNN)
6. Gradient Boosting

### 10.2 Cross-Validation Results

The models were evaluated using cross-validation to assess their performance and consistency across different data partitions.

| Machine Learning Model | Accuracy (Mean ± Std.) | ROC-AUC (Mean ± Std.) |
|---|---:|---:|
| Logistic Regression | 99.55 ± 0.19% | 0.9996 ± 0.0004 |
| Random Forest | 99.18 ± 0.35% | 0.9990 ± 0.0009 |
| XGBoost | 99.30 ± 0.49% | 0.9991 ± 0.0008 |
| SVM | 99.35 ± 0.24% | 0.9994 ± 0.0006 |
| KNN | 99.00 ± 0.29% | 0.9965 ± 0.0021 |
| Gradient Boosting | 99.02 ± 0.52% | 0.9992 ± 0.0006 |

**Observation:** Logistic Regression achieved the highest mean cross-validation accuracy (99.55%) and ROC-AUC (0.9996), demonstrating strong classification performance during cross-validation.

### 10.3 Final Test Set Performance

All six models were subsequently evaluated on the independent test set containing 1,000 samples.

| Model | Accuracy (%) | Precision (%) | Recall (%) | F1-Score (%) | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | 98.70 | 98.70 | 98.70 | 98.70 | 0.9997 |
| Random Forest | 99.10 | 99.10 | 99.10 | 99.10 | 0.9997 |
| XGBoost | 98.70 | 98.71 | 98.70 | 98.70 | 0.9995 |
| SVM | 98.60 | 98.60 | 98.60 | 98.60 | 0.9995 |
| KNN | 98.70 | 98.70 | 98.70 | 98.70 | 0.9936 |
| Gradient Boosting | 99.00 | 99.01 | 99.00 | 99.00 | 0.9995 |

*Note: Precision, recall, and F1-score are macro-averaged values.*

### 10.4 Final Model Ranking

Models were ranked according to their ROC-AUC performance on the independent test set.

| Rank | Model | Test ROC-AUC |
|---:|---|---:|
| 1 | Logistic Regression | 0.999700 |
| 2 | Random Forest | 0.999652 |
| 3 | Gradient Boosting | 0.999520 |
| 4 | SVM | 0.999460 |
| 5 | XGBoost | 0.999456 |
| 6 | KNN | 0.993594 |

### 10.5 Key Findings

- **Logistic Regression:** Achieved the highest test ROC-AUC of 0.9997 and the highest cross-validation accuracy of 99.55%.
- **Random Forest:** Achieved the highest independent test accuracy of 99.10%, with a ROC-AUC of approximately 0.9997.
- **Gradient Boosting:** Delivered the second-highest test accuracy of 99.00%.
- **SVM:** Demonstrated consistent classification performance with 98.60% test accuracy.
- **XGBoost:** Achieved 98.70% test accuracy and a ROC-AUC of 0.9995.
- **KNN:** Achieved 98.70% test accuracy, although its ROC-AUC was comparatively lower at 0.9936.

### 10.6 Conclusion

The experimental findings demonstrate that all six evaluated machine learning algorithms achieved strong classification performance on the Blockchain Healthcare Dataset.

Random Forest obtained the highest test accuracy (99.10%), whereas Logistic Regression achieved the highest test ROC-AUC (0.9997) and cross-validation accuracy (99.55%).

These results provide a comparative baseline for machine learning-based blockchain adoption prediction in healthcare environments.

**Important:** The reported performance reflects prediction of the selected target variable (`blockchain`) and should not be interpreted as direct evidence that blockchain improves healthcare outcomes.

**Note:** The dataset contains observational records. Predictive associations should not be interpreted as evidence of causal effects of blockchain technology.
