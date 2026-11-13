# Hydraulic Valve Predictive Maintenance

## Project Overview

This project explores predictive maintenance techniques on hydraulic systems using machine learning.

The objective is to predict whether a hydraulic valve is operating under optimal conditions (100%) or degraded using pressure and flow measurements collected during production cycles.

## Dataset

Source:

- UCI Machine Learning Repository
- Condition Monitoring of Hydraulic Systems Dataset

Sensors used:

- PS2: Pressure sensor (100 Hz)
- FS1: Flow sensor (10 Hz)

Each row corresponds to one operating cycle.

## Methodology

### Data preprocessing

- Exploratory Data Analysis
- Correlation analysis
- Feature Engineering
- Feature Selection

### Feature Engineering

Raw measurements were summarized into statistical indicators:

- Mean
- Standard deviation
- Minimum
- Maximum
- Median

This reduced each cycle from 6600 sensor measurements to a compact set of interpretable features.

### Models Evaluated

- Logistic Regression
- K-Nearest Neighbors
- Decision Tree
- Gaussian Naive Bayes
- Support Vector Machine
- Random Forest

### Hyperparameter Optimization

GridSearchCV with 5-fold Cross Validation was used for:

- Random Forest
- SVM RBF

## Results

| Model | Accuracy |
|---------|---------|
| Random Forest Optimized | 95.1% |
| SVM RBF Optimized | 90.7% |
| Random Forest | 85.9% |
| Decision Tree | 84.4% |
| SVM RBF | 82.9% |

The optimized Random Forest provided the best overall performance.

## Key Findings

- Flow variability and average flow are the most informative features.
- Non-linear models significantly outperform linear approaches.
- Hyperparameter optimization greatly improves model performance.
- Random Forest achieved the best bias-variance trade-off.

## Author

Léo Carlier-Barnoux

Machine Learning & Big Data Engineering Student
EFREI Paris