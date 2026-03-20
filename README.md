# LVC Synthetic Data ML

This repository contains a complete Data Science workflow for epidemiological studies of Canine Visceral Leishmaniasis (LVC), including machine learning, synthetic tabular data generation, and explainable artificial intelligence.

## Project goals

- Evaluate traditional machine learning models on clinical canine data
- Investigate class imbalance handling strategies
- Generate synthetic tabular data using CTGAN and TVAE
- Compare real, balanced, and synthetic data scenarios
- Assess generalization through Synthetic-to-Real evaluation
- Apply SHAP and LIME for model interpretability

## Experimental design

- Stratified train/test split with multiple random seeds: 41, 42, 46
- Internal validation through cross-validation
- Comparison across:
  - Real data
  - Oversampling-based balancing
  - Cost-sensitive learning
  - Synthetic data (10x and 30x)

## Models evaluated

- Logistic Regression
- Support Vector Machine
- K-Nearest Neighbors
- Random Forest
- Gradient Boosting
- Multi-layer Perceptron

## Synthetic data generation

Synthetic datasets are generated with the SDV ecosystem using:

- CTGAN
- TVAE

## Explainability

The project uses:

- SHAP for global and model-based explanations
- LIME for local explanations

## Reproducibility

This repository is intended to support reproducibility for reviewers and readers.  
All experiments should be run with fixed seeds, explicit preprocessing pipelines, and documented evaluation procedures.

## Suggested structure

data/  
notebooks/  
src/  
results/

## Author

**Marcelo Pontes Rodrigues**  
Graduate Program in Applied Technologies to Animals of Regional Interest  
Federal University of Piauí (UFPI), Brazil  

📧 Email: marcelo.rodrigues@ufpi.edu.br
🔗 GitHub: https://github.com/infopontes

## License

MIT License