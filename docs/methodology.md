---
title: Methodology
nav_order: 2
---

# Methodology

## Overview

The project follows a structured machine learning workflow designed for epidemiological applications with small and imbalanced datasets.

## Workflow Steps

1. Data preprocessing
2. Baseline model evaluation
3. Class imbalance handling
4. Synthetic data generation
5. Synthetic → real evaluation
6. Threshold optimization
7. Explainable AI (XAI)

## Data Splitting

- Train/Test split: 70/30
- Stratified sampling
- Multiple seeds: 41, 42, 46

## Baseline Models

- Logistic Regression
- Support Vector Machine (SVM)
- K-Nearest Neighbors (KNN)
- Random Forest
- Gradient Boosting
- Multi-layer Perceptron (MLP)

## Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1-score

## Imbalance Handling Techniques

- Random OverSampling
- SMOTE / ADASYN
- Class weighting

## Model Selection

The best-performing pipeline was selected based on recall performance under standard threshold conditions (0.5).

Selected configuration:

- Generator: CTGAN
- Scenario: 30x
- Model: KNN

> Recall was prioritized because false negatives represent undetected infected animals.