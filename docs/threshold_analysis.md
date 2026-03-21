---
title: Threshold Optimization
nav_order: 5
---

# Threshold Optimization

## Motivation

The default classification threshold (0.5) is not optimal for medical screening applications.

## Approach

Threshold values from 0.10 to 0.85 were evaluated.

## Key Result

Optimal threshold:

- **0.35**

## Performance Impact

| Metric | Before | After |
|---|---:|---:|
| Recall | ~0.49 | ~0.93 |
| False Negatives | 21 | 3 |

## Interpretation

Lowering the threshold:

- increases sensitivity
- reduces missed cases
- increases false positives

## Clinical Relevance

In epidemiological screening:

- false negatives are more critical than false positives
- higher recall is desirable

## Conclusion

Threshold tuning is a critical step to adapt machine learning models to real-world clinical applications.