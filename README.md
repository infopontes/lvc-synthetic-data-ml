# LVC Synthetic Data ML

**Author:** Marcelo Pontes Rodrigues
**Program:** Graduate Program in Technologies Applied to Regional Animal Health – UFPI

📧 Email: marcelo.rodrigues@ufpi.edu.br
🔗 GitHub: https://github.com/infopontes

---

## 📌 Project Overview

This project implements a complete Data Science workflow applied to **Canine Visceral Leishmaniasis (CVL)** using:

* Machine Learning
* Synthetic Data Generation (CTGAN, TVAE)
* Class Imbalance Handling
* Explainable Artificial Intelligence (XAI)

---

## 🎯 Objective

To evaluate whether **synthetic tabular data** can improve model performance in:

* Small datasets
* Imbalanced datasets
* Epidemiological scenarios

---

## 🐶 Dataset

The dataset contains clinical records of dogs investigated for CVL.

### Target Variable

* `diagnosis`: positivo / negativo

### Features

* Clinical signs (e.g., alopecia, lesions, mucosa color)
* Animal characteristics (sex, breed)

---

## ⚠️ Problem

* Small dataset (456 samples)
* Class imbalance (~30% positive)

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

* 10x synthetic dataset
* 30x synthetic dataset
* Balanced classes (50/50)

---

### 5. Synthetic → Real Evaluation

* Training: synthetic data
* Testing: real holdout data

---

## 📊 Key Results

* Baseline recall ≈ 0.26
* Balanced data recall ≈ 0.50
* Synthetic data (CTGAN 30x + KNN):

  * **Recall ≈ 0.51**

### 🔍 Interpretation

Synthetic data:

* Improved recall compared to baseline
* Matched traditional balancing methods
* Reduced false negatives

---

## 📉 Model Limitations

* Low ROC AUC (~0.52)
* High false positive rate

However:

> The model is suitable for screening scenarios where sensitivity is more important than specificity.

---

## 🔬 Statistical Validation

Synthetic data were validated using:

* Jensen-Shannon Distance (JSD)
* Total Variation Distance (TVD)
* Chi-square test

Results indicate strong similarity between real and synthetic distributions.

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

* Fixed random seeds
* Stratified splits
* Explicit preprocessing pipelines
* Saved results in CSV

---

## 📌 Conclusion

Synthetic data can:

* Improve recall in small datasets
* Match traditional imbalance techniques
* Support epidemiological screening models

---

## 📜 License

MIT License
