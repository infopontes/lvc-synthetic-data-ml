# LVC Synthetic Data ML

**Author:** Marcelo Pontes Rodrigues
**Program:** Graduate Program in Technologies Applied to Regional Animal Health – UFPI

---

## 📌 Project Overview

This project implements a complete Data Science workflow applied to **Canine Visceral Leishmaniasis (CVL)** using:

* Machine Learning
* Synthetic Data Generation (CTGAN, TVAE)
* Class Imbalance Handling
* Threshold Optimization
* Explainable Artificial Intelligence (XAI)

---

## 🎯 Objective

To evaluate whether **synthetic tabular data** can improve model performance in:

* Small datasets
* Imbalanced datasets
* Epidemiological screening scenarios

---

## 🐶 Dataset

The dataset contains clinical records of dogs investigated for CVL.

### Target Variable

* `diagnosis`: positivo / negativo

### Features

* Clinical signs (alopecia, lesions, mucosa color, etc.)
* Animal characteristics (sex, breed)

---

## ⚠️ Problem

* Small dataset (456 samples)
* Class imbalance (~30% positive)
* High cost of false negatives (missed infected animals)

---

## 🔬 Methodology

### 1. Data Splitting

* Train/Test: 70/30
* Stratified
* Seeds: `[41, 42, 46]`

---

### 2. Baseline Models

* Logistic Regression
* SVM
* KNN
* Random Forest
* Gradient Boosting
* MLP

Metrics:

* Accuracy
* Precision
* Recall
* F1-score

---

### 3. Imbalance Handling

* RandomOverSampler
* SMOTE / ADASYN
* Class weights

---

### 4. Synthetic Data Generation

Using SDV:

* **CTGAN**
* **TVAE**

Scenarios:

* 10x dataset
* 30x dataset
* Balanced classes (50/50)

---

### 5. Synthetic → Real Evaluation

* Training: synthetic data
* Testing: real holdout data

This evaluates real-world generalization.

---

### 6. Threshold Optimization

After selecting the best model, threshold tuning was applied:

* Default threshold: `0.5`
* Optimized threshold: `0.35`

Goal:

* Maximize recall
* Minimize false negatives

---

## 📊 Key Results

### Baseline

* Recall ≈ 0.26 ❌

### Balanced Data

* Recall ≈ 0.50 ✔

### Synthetic Data (CTGAN 30x + KNN)

* Recall ≈ 0.51 ✔

---

## 🔥 Threshold Optimization Results

* Recall increased to **0.93**
* False negatives reduced from **21 → 3**

### Interpretation

* Significant improvement in sensitivity
* Model becomes suitable for screening

---

## 📉 Model Limitations

* Low ROC AUC (~0.52)
* High false positive rate

However:

> The model is not intended for final diagnosis, but for epidemiological screening.

---

## 📊 Evaluation Metrics

### ROC Curve

* Evaluates global discrimination
* Shows limited separability

### Precision-Recall Curve

* More suitable for imbalanced data
* Shows that recall can increase without major precision loss

---

## 🔬 Statistical Validation of Synthetic Data

* Jensen-Shannon Distance (JSD)
* Total Variation Distance (TVD)
* Chi-square test

Results confirm strong similarity between real and synthetic distributions.

---

## 📁 Project Structure

```
lvc-synthetic-data-ml/
│
├── data/
│   ├── raw/
│   └── synthetic/
│
├── notebooks/
│   ├── 01_baseline.ipynb
│   ├── 02_balancing.ipynb
│   ├── 05_synthetic_data_generation.ipynb
│   ├── 06_synthetic_to_real_evaluation.ipynb
│
├── results/
│   └── tables/
│
├── requirements.txt
└── README.md
```

---

## ⚙️ Installation

```bash
git clone git@github.com:infopontes/lvc-synthetic-data-ml.git
cd lvc-synthetic-data-ml

python3 -m venv venv
source venv/bin/activate

pip install -r requirements.txt
```

---

## ▶️ Running

```bash
jupyter lab
```

---

## 🔁 Reproducibility

* Fixed seeds
* Stratified splits
* Controlled preprocessing
* Saved results

---

## 📌 Final Conclusion

This study demonstrates that:

* Synthetic data can improve recall in small datasets
* CTGAN outperforms TVAE in this context
* Threshold tuning dramatically improves clinical usefulness
* The model is effective for **screening**, not diagnosis

---

## 📜 License

MIT License


## 📘 Full Documentation

👉 https://infopontes.github.io/lvc-synthetic-data-ml/