# A Comparative Study of Classification and Regression Models for Intelligent Beam Selection in 5G Systems

**Prepared by Robin Wang**

---

## Executive Summary

Modern 5G wireless networks rely on directional beamforming to achieve high data rates, particularly in millimeter-wave (mmWave) systems. However, selecting the optimal beam typically requires exhaustive beam sweeping, which increases latency, signaling overhead, and reduces spectral efficiency.

This capstone project develops and compares supervised machine learning models for predicting the optimal beam index and corresponding beam quality using Channel State Information (CSI). By replacing exhaustive beam search with intelligent prediction, the system demonstrates how AI can improve wireless efficiency and reduce beam training overhead.

The study evaluates multiple classification and regression algorithms, including linear models, tree-based models, ensemble methods, and neural networks, to determine the most effective approach for intelligent beam selection.

---

## Problem Statement

In 5G mmWave systems, maintaining a reliable connection requires accurate beam alignment between base stations and users. Traditional beam selection methods rely on repeated beam sweeping, which:

- Increases latency
- Consumes network resources
- Reduces spectral efficiency
- Limits scalability in dynamic environments

This project investigates whether supervised machine learning models can predict:

1. The optimal beam index (classification problem)
2. The maximum achievable beam gain / SNR (regression problem)

The objective is to compare model performance and identify the most effective approach for AI-driven beam selection.

---

## Model Objectives

### Task 1 – Classification

Predict the **optimal beam index** from a predefined beam codebook.

- Type: Supervised Learning
- Category: Multi-class Classification
- Output: Integer beam index

---

### Task 2 – Regression

Predict the **maximum achievable beam gain / SNR**.

- Type: Supervised Learning
- Category: Regression
- Output: Continuous numerical value

---

## Data Sources

Primary dataset:

**DeepMIMO – O1_60 Scenario**  
https://www.deepmimo.net/

The dataset provides:

- Massive MIMO CSI matrices
- User positions
- Ray-tracing-based propagation environment

### Dataset Construction

For each user sample:

1. Extract CSI matrix  
2. Apply beamforming codebook  
3. Compute beam gain  
4. Define:
   - Classification label → Best beam index
   - Regression label → Maximum beam gain (SNR)

---

## Data Visualization

Exploratory analysis includes:

- Beam index distribution
- SNR histogram
- Correlation heatmap
- PCA visualization (2D projection)

These visualizations confirm learnability and feature separability in the dataset.

---

## Data Preprocessing

- Removed invalid or extremely low-SNR samples
- Verified no missing values
- Standardized numerical features
- Applied PCA for dimensionality reduction
- Encoded beam indices
- Split dataset into:
  - 80% Training
  - 20% Testing
  - Stratified sampling for classification

---

## Machine Learning Models

### Classification Models

| Model | Purpose |
|--------|---------|
| Logistic Regression | Linear baseline |
| K-Nearest Neighbors | Distance-based comparison |
| Decision Tree | Nonlinear modeling |
| Random Forest | Ensemble method |
| Gradient Boosting | High-performance ensemble |
| Neural Network (MLP) | Deep learning benchmark |

---

### Regression Models

| Model | Purpose |
|--------|---------|
| Linear Regression | Baseline |
| Ridge / Lasso | Regularization |
| Decision Tree Regressor | Nonlinear modeling |
| Random Forest Regressor | Ensemble |
| Gradient Boosting Regressor | High performance |
| Neural Network Regressor | Deep learning comparison |

---

## Model Evaluation

### Classification Metrics

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

### Regression Metrics

- Mean Absolute Error (MAE)
- Root Mean Square Error (RMSE)
- R² Score

### Model Selection Criteria

Models were compared based on:

- Highest classification accuracy
- Lowest regression RMSE
- Cross-validation stability
- Interpretability

---

## Key Findings

- Ensemble models (Random Forest and Gradient Boosting) significantly outperformed linear baselines.
- Neural networks provided competitive performance but required higher computational cost.
- Intelligent beam prediction can reduce beam sweeping overhead while maintaining high signal quality.

This demonstrates the strong potential of AI-driven beam management in future 5G/6G systems.

---

## Future Work

- Cross-scenario generalization testing (e.g., indoor vs urban)
- Robustness under noise and interference
- Real-time deployment simulation
- Feature importance analysis for interpretability

---

## Why This Matters

Wireless networks are evolving toward higher frequencies and more dynamic use cases. Without intelligent beam prediction:

- Users experience increased latency
- Networks waste resources
- Scalability becomes limited

This project shows that machine learning can help build faster, smarter, and more efficient wireless systems.

---

## Contact

Robin Wang  
robin.888.wang@gmail.com
