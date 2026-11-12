# Protocol-Specific Intrusion Detection System for Electric Vehicle Charging Infrastructure Using Machine Learning and Hybrid Online Learning

## 1. Project Overview

This project was developed as part of my MSc Cybersecurity dissertation at Anglia Ruskin University.

It investigates machine-learning approaches for detecting malicious activity in Electric Vehicle (EV) charging infrastructure using the CICEVE 2024 dataset.

The research combines offline machine-learning models with online learning algorithms and concept-drift detection to investigate how an intrusion detection system can respond to changing network behaviour.

## 2. Research Objectives

- Develop a machine-learning-based intrusion detection approach.
- Investigate protocol-specific attack detection.
- Address class imbalance in the dataset.
- Compare offline and online learning models.
- Investigate concept-drift detection.
- Evaluate a hybrid offline-online learning approach.

## 3. Dataset

**Dataset:** CICEVE 2024

**Application:** Electric Vehicle charging infrastructure security.

The dataset was processed through feature selection, preprocessing and class grouping before model development.

## 4. Technologies and Libraries

- Python
- Pandas
- NumPy
- Scikit-learn
- Imbalanced-learn
- River
- Matplotlib
- TQDM

## 5. Implementation Methodology

### Phase 1: Dataset Preparation

- Dataset loading and exploration.
- Attack class grouping.
- Feature selection.
- Data preprocessing.
- Class balancing using SMOTEENN.

### Phase 2: Offline Baseline Models

**Multi-Layer Perceptron (MLP)**

- Neural network with hidden layers of 128, 64 and 32 neurons.
- Training over 200 epochs.
- Classification performance evaluation.

**Gradient Boosting**

- Offline ensemble classification.
- Prediction and performance evaluation.
- Confusion matrix analysis.

### Phase 3: Online Models with Drift Detection

**Adaptive Random Forest (ARF) + ADWIN**

- Online learning.
- Adaptive classification.
- Prediction-error monitoring.
- Concept-drift detection using ADWIN.

**Streaming Random Patches (SRP) + ADWIN**

- Online ensemble learning.
- Streaming data evaluation.
- Prediction-error monitoring.
- Concept-drift detection using ADWIN.

### Phase 4: Hybrid Model

**Gradient Boosting (Offline) + Adaptive Random Forest (Online)**

The hybrid approach combines the predictions of an offline Gradient Boosting model and an online Adaptive Random Forest model.

The implementation uses:

- Offline Gradient Boosting weight: 60%.
- Online Adaptive Random Forest weight: 40%.
- ADWIN for monitoring prediction errors and detecting concept drift.

## 6. Model Evaluation

The implementation evaluates model performance using:

- Accuracy
- Precision
- Recall
- F1-score
- Macro averages
- Weighted averages
- Confusion matrices
- Online performance tracking
- Concept-drift monitoring
  

### 6.1 Offline Baseline Model: Multi-Layer Perceptron (MLP)

The MLP model was evaluated on 254,977 records from the CICEVE 2024 dataset.

**Performance Results:**

| Metric | Result |
|---|---:|
| Accuracy | 96% |
| Macro Precision | 90.25% |
| Macro Recall | 89.83% |
| Macro F1-score | 90.00% |
| Weighted Precision | 95.89% |
| Weighted Recall | 95.91% |
| Weighted F1-score | 95.88% 

### 6.2 Offline Baseline Model: Gradient Boosting

Gradient Boosting was evaluated as an additional offline baseline model using the CICEVE 2024 dataset, containing 254,977 records.

**Performance Results:**

| Metric | Result |
|---|---:|
| Accuracy | 100% (rounded) |
| Macro Precision | 99.87% |
| Macro Recall | 99.91% |
| Macro F1-score | 99.89% |
| Weighted Precision | 99.95% |
| Weighted Recall | 99.95% |
| Weighted F1-score | 99.95% |
### 6.3 Online Learning Model: Adaptive Random Forest (ARF) with ADWIN

The Adaptive Random Forest (ARF) model was implemented using online learning, with ADWIN (Adaptive Windowing) monitoring prediction errors and detecting concept drift. The model was evaluated on 254,977 records from the CICEVE 2024 dataset.

**Performance Results:**

| Metric | Result |
|---|---:|
| Accuracy | 98% (rounded) |
| Macro Precision | 96.88% |
| Macro Recall | 95.02% |
| Macro F1-score | 95.63% |
| Weighted Precision | 98.42% |
| Weighted Recall | 98.25% |
| Weighted F1-score | 98.21% |

**Concept Drift Detection:**

ADWIN detected 2 concept drift events during online evaluation.

- Drift Event 1: Instance 181056; estimated error 0.0174.
- Drift Event 2: Instance 190784; estimated error 0.0192.

### 6.4 Hybrid Offline-Online Model: Weighted Fusion

A hybrid model was developed by combining the offline Gradient Boosting model with the online Adaptive Random Forest model.

The fusion mechanism used the following weights:

- Offline Gradient Boosting model: 60%.
- Online Adaptive Random Forest model: 40%.

The hybrid model was evaluated on 254,977 records from the CICEVE 2024 dataset.

**Performance Results:**

| Metric | Result |
|---|---:|
| Accuracy | 100% (rounded) |
| Macro Precision | 99.91% |
| Macro Recall | 99.93% |
| Macro F1-score | 99.92% |
| Weighted Precision | 99.96% |
| Weighted Recall | 99.96% |
| Weighted F1-score | 99.96% |

**Concept Drift Detection:**

- Total drift events detected: 0.

## 7. Key Cybersecurity Concepts

- Intrusion Detection Systems (IDS)
- Electric Vehicle charging infrastructure security
- Protocol-specific attack detection
- Offline machine learning
- Online machine learning
- Ensemble learning
- Concept drift
- Adaptive classification
- Hybrid intrusion detection

## 8. Project Status

**Status:** MSc dissertation completed.  


This project documents the implementation and methodology developed during my academic research.

## 9. Disclaimer

This project is presented for academic and professional portfolio purposes. It does not disclose confidential organisational information.
