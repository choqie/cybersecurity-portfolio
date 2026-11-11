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

Actual numerical results and model comparisons will be documented using the dissertation's recorded outputs.

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
**Final dissertation grade:** 68%.

This project documents the implementation and methodology developed during my academic research.

## 9. Disclaimer

This project is presented for academic and professional portfolio purposes. It does not disclose confidential organisational information.
