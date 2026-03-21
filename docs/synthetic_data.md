---
title: Synthetic Data Generation
nav_order: 3
---

# Synthetic Data Generation

## Overview

Synthetic data was generated to address limitations of small sample size and class imbalance.

## Methods Used

- CTGAN
- TVAE

## Generation Strategy

- Dataset expansion: 10x and 30x
- Class balancing: 50/50 (positive/negative)

## Evaluation Approach

Synthetic datasets were evaluated by training models on synthetic data and testing on real data.

## Key Findings

- CTGAN outperformed TVAE
- 30x generation produced better results than 10x
- Synthetic data preserved relevant feature distributions

## Statistical Validation

- Jensen-Shannon Distance (JSD)
- Total Variation Distance (TVD)
- Chi-square tests

Results indicated strong similarity between real and synthetic datasets.

## Conclusion

Synthetic data is a viable alternative to traditional imbalance techniques and can improve model performance in small epidemiological datasets.