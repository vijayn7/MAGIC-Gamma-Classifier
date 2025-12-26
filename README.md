# MAGIC Gamma Ray Classifier 🔭

![Python](https://img.shields.io/badge/Python-3.9+-blue)
![ML](https://img.shields.io/badge/Machine%20Learning-Supervised-green)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)
![Dataset](https://img.shields.io/badge/Dataset-UCI-orange)

## Overview
A machine learning project that classifies gamma ray events detected by the MAGIC telescope using real experimental data. This project demonstrates a full ML pipeline from raw data to evaluation.

## Problem Statement
Atmospheric Cherenkov telescopes capture both gamma ray and hadronic background events. The challenge is to accurately identify gamma initiated showers using image based features.

## Dataset
- Source: :contentReference[oaicite:1]{index=1}
- Samples: 19k+
- Features: 10 continuous variables
- Labels: Gamma vs Hadron

Let the dataset be defined as:

X ∈ ℝⁿˣᵈ,  y ∈ {0,1}ⁿ

where:
- n is the number of events
- d = 10 features per event
- y = 1 denotes gamma events
- y = 0 denotes hadronic background

## Pipeline
1. Data loading and cleaning
2. Exploratory data analysis
3. Feature scaling
4. Class imbalance correction
5. Model training
6. Evaluation

## Methodology

### Preprocessing
Feature scaling is applied using standardization:

z = (x − μ) / σ

This ensures features have zero mean and unit variance, improving convergence and model stability.

Class imbalance is addressed using random oversampling, increasing the representation of gamma events in the training set.

### Model Training
The dataset is split into training and test sets. A supervised classifier is trained on the resampled and standardized data.


## Visualizations
Feature distributions were visualized to compare gamma and hadron events, revealing separability in several dimensions such as size, concentration, and distance.

<!-- Optional: insert saved histogram images here -->

## Tech Stack
- Python
- NumPy
- Pandas
- Matplotlib
- Scikit learn
- Imbalanced learn

## Why This Project Matters
- Uses real physics data
- Addresses class imbalance explicitly
- Demonstrates end to end ML workflow
- Suitable for research and industry applications


## Discussion
Results demonstrate the importance of preprocessing and class balancing in astrophysical classification tasks. Without correction, models tend to favor the majority hadronic class.

## Conclusion
This project shows that classical machine learning techniques can effectively classify gamma ray events using engineered features. Future work may extend this approach using ensemble methods or deep learning architectures.