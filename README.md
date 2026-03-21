# LVC Synthetic Data ML

![Python](https://img.shields.io/badge/Python-3.12-blue)
![ML](https://img.shields.io/badge/Machine%20Learning-Scikit--Learn-orange)
![Synthetic Data](https://img.shields.io/badge/Synthetic%20Data-CTGAN%20%7C%20TVAE-green)
![Status](https://img.shields.io/badge/Status-Research%20Project-yellow)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

Machine Learning, synthetic data generation, and explainable AI applied to **Canine Visceral Leishmaniasis (CVL)**.

---

## 📘 Full Documentation

👉 <a href="https://infopontes.github.io/lvc-synthetic-data-ml/" target="_blank"><b>Access full documentation (GitHub Pages)</b></a>

The complete documentation includes:

* methodology
* synthetic data generation
* experimental results
* threshold optimization
* explainability (SHAP and LIME)
* scientific references

---

## 📁 Repository Structure

```text
lvc-synthetic-data-ml/
│
├── data/
│   ├── raw/
│   └── synthetic/
│
├── docs/
│   ├── index.md
│   ├── methodology.md
│   ├── synthetic_data.md
│   ├── results.md
│   ├── threshold_analysis.md
│   ├── xai.md
│   ├── references.md
│   └── assets/
│
├── notebooks/
│   ├── 01_data_loading_and_split.ipynb
│   ├── 02_preprocessing_pipeline.ipynb
│   ├── 03_baseline_ml.ipynb
│   ├── 04_balancing_methods.ipynb
│   ├── 05_synthetic_data_generation.ipynb
│   ├── 06_synthetic_to_real_evaluation.ipynb
│   └── 07_xai_shap_lime.ipynb
│
├── results/
│   ├── images/
│   └── tables/
│
├── src/
├── requirements.txt
├── _config.yml
└── README.md
```

---

## 🚀 Getting Started

### Clone the repository

```bash
git clone git@github.com:infopontes/lvc-synthetic-data-ml.git
cd lvc-synthetic-data-ml
```

---

### Create a virtual environment

```bash
python3 -m venv venv
source venv/bin/activate
```

---

### Install dependencies

```bash
pip install -r requirements.txt
```

---

## ▶️ Run the project

```bash
jupyter lab
```

Run notebooks in order:

1. Data loading and preprocessing
2. Baseline models
3. Balancing techniques
4. Synthetic data generation
5. Synthetic → real evaluation
6. Threshold optimization
7. Explainability (XAI)

---

## 📊 Project Overview

This project investigates the use of **synthetic tabular data** to improve machine learning performance in:

* small datasets
* imbalanced datasets
* epidemiological screening scenarios

Key contributions:

* evaluation of CTGAN and TVAE
* comparison with imbalance techniques
* threshold optimization (recall-focused)
* explainability with SHAP and LIME

---

## 📩 Dataset Access

The dataset used in this project is not publicly available.

Requests can be sent to:

**[marcelo.rodrigues@ufpi.edu.br](mailto:marcelo.rodrigues@ufpi.edu.br)**

---

## 🔁 Reproducibility

* fixed random seeds
* stratified splits
* preprocessing pipelines
* saved results
* synthetic datasets

---

## 📜 License

MIT License
