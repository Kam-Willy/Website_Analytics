# 📊 Web Analytics Project

## 🔎 Overview

This project demonstrates how to analyze and model **website analytics data** in order to understand **traffic quality and user behavior patterns**.

The dataset contains Google Analytics–style metrics such as:

* **Sessions**
* **Users & New Users**
* **Pageviews**
* **Bounce Rate**
* **Average Session Duration**
* **Traffic Source / Medium**

The goal is to:

1. Explore and clean web analytics data.
2. Build models to **classify high vs. low bounce traffic**.
3. Apply **regression** to forecast bounce rates.
4. Use **clustering** to segment traffic sources/mediums by behavior.
5. Compare model performance and derive actionable insights.

---

## 🏗️ Project Structure

```
web-analytics-project/
│
├── data/
│   ├── raw/                   # Original dataset (CSV)
│   ├── processed/             # Cleaned and feature-engineered datasets
│
├── notebooks/
│   ├── websiteanalytics.ipynb # Original analysis
│   ├── websiteanalytics_explained.ipynb # With inline comments & explanations
│
├── src/
│   ├── cleaning.py            # Functions for data cleaning & type conversion
│   ├── classification.py      # Bounce rate classification
│   ├── regression.py          # Bounce rate regression
│   ├── clustering.py          # Source segmentation via KMeans
│   └── evaluation.py          # Comparison report for all models
│
├── reports/
│   ├── model_performance.md   # Performance summary
│   └── visuals/               # Plots & figures
│
└── README.md
```

---

## ⚙️ Installation

1. Clone the repo:

   ```bash
   git clone https://github.com/your-username/web-analytics-project.git
   cd web-analytics-project
   ```
2. Create and activate a virtual environment:

   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```
3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

---

## 📦 Dependencies

Key libraries used in this project:

* **Pandas** – data manipulation
* **NumPy** – numerical operations
* **Matplotlib & Seaborn** – visualization
* **scikit-learn** – modeling (classification, regression, clustering)
* **nbformat** – notebook handling

Install all with:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn nbformat
```

---

## 🚀 Usage

### 1. Run Exploratory Data Analysis (EDA)

Open the notebook:

```bash
jupyter notebook notebooks/websiteanalytics_explained.ipynb
```

This will guide you through loading, cleaning, and exploring the dataset.

### 2. Run Classification

Predict whether sessions are **high-bounce** or **low-bounce**:

```python
from src.classification import run_classification
run_classification("data/processed/web_analytics_clean.csv")
```

### 3. Run Regression

Predict **continuous bounce rate values**:

```python
from src.regression import run_regression
run_regression("data/processed/web_analytics_clean.csv")
```

### 4. Run Clustering

Segment traffic sources/mediums:

```python
from src.clustering import run_clustering
```

### 5. Compare Models

Generate a **comparison report** of classification, regression, and clustering:

```python
from src.evaluation import compare_models
compare_models()
```

---

## 📊 Model Performance Summary

### Classification

* **Accuracy:** 84%
* **F1 Score:** 85%
* **ROC-AUC:** 83%
  ➡️ **Best for identifying risky/high-bounce traffic.**

### Regression

* **MAE:** 8.503
* **RMSE:** 12.113
* **R²:** 0.6082
  ➡️ **Explains \~61% of variance; useful for forecasting bounce rate trends.**

### Clustering

* **Clusters:** 3
* **Silhouette Score:** 0.466
  ➡️ **Provides moderate separation of traffic sources; useful for segmentation.**

---

## 📌 Key Findings

* **Classification performed best**, making it suitable for operational monitoring (flagging high-bounce sessions).
* **Regression provided trend insights** but is less accurate at individual prediction.
* **Clustering uncovered broad audience segments**, valuable for marketing strategy.

---

## 🛠️ Future Improvements

* Add **time-series forecasting** for sessions and bounce rate.
* Expand clustering with **geography, device type, landing pages**.
* Deploy results into a **Streamlit dashboard** for interactive analysis.
* Integrate with **MLflow** for experiment tracking.

---

## 👨‍💻 Author

Developed by **[Wilfred Kamau]**

* Role: Data Scientist / Machine Learning Engineer
* Contact: [kamaunjenga675@gmail.com]

---
