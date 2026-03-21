# Methodology

The workflow consists of:

1. Data preprocessing
2. Baseline model evaluation
3. Imbalance handling
4. Synthetic data generation (CTGAN, TVAE)
5. Synthetic → real evaluation
6. Threshold tuning
7. Explainability (SHAP, LIME)

## Key Decision

The best pipeline was:

- Generator: CTGAN
- Scenario: 30x
- Model: KNN