---
title: Results
nav_order: 4
---

# Results

## Performance Comparison

| Scenario | Recall |
|---|---:|
| Baseline | ~0.26 |
| Balanced Data | ~0.50 |
| Synthetic Data | ~0.51 |
| Threshold Optimization | ~0.93 |

## Key Observations

- Synthetic data matched traditional balancing methods
- CTGAN provided the best generalization
- KNN performed best in synthetic scenarios

## Model Behavior

- Improved detection of positive cases
- Increased false positives as an expected trade-off
- Suitable for screening, not diagnosis

## ROC Analysis

- AUC ≈ 0.52
- Indicates limited global separability

## Precision-Recall Analysis

- Recall can be increased significantly with minimal precision loss
- More informative than ROC in imbalanced settings

## Conclusion

The model demonstrates strong performance for epidemiological screening, particularly when combined with threshold optimization.