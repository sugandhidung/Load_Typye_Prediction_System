# ⚡ Power System Load Type Prediction

A machine learning project for **predicting power system load types** using advanced feature engineering and ensemble learning techniques.  
The project improves baseline performance (~90%) to **94%+ accuracy** through optimized preprocessing, feature engineering, and model stacking.

---

## 📌 Project Overview

Power systems generate large volumes of sensor data that can be used to understand and predict **electric load behavior**.  
This project builds an optimized ML pipeline to classify **load types** based on electrical measurements and temporal features.

The workflow includes:

- Data cleaning and validation
- Smart missing value imputation
- Domain-driven feature engineering
- Hyperparameter tuning
- Ensemble model stacking
- Model evaluation and visualization

---

## 🚀 Key Improvements

| Improvement | Description |
|-------------|-------------|
| **Data Cleaning** | Clipped power factor values to valid range `[0,100]` and corrected NSM using modulo `86400` |
| **Advanced Imputation** | Used **IterativeImputer (MICE)** instead of simple median imputation |
| **Feature Engineering** | Created multiple power-system derived features and cyclical time encodings |
| **Model Optimization** | Applied **RandomizedSearchCV** with **Stratified K-Fold** cross-validation |
| **Ensemble Learning** | Built a **Stacking Classifier** combining multiple models |
| **Comprehensive Evaluation** | Compared models using accuracy, confusion matrix, and feature importance |

---

## 🧠 Machine Learning Models

The following models are used and compared:

- **XGBoost Classifier**
- **Random Forest**
- **HistGradientBoosting**
- **Stacking Ensemble**
  - Base models: XGBoost, HistGB, RandomForest
  - Meta learner: Logistic Regression

---

## 📊 Feature Engineering

Additional features were created to capture domain knowledge from power system data:

Examples include:

- Lagging / Leading Reactive Power relationships
- Power factor transformations
- Cyclical time encoding
  - Hour
  - Day of week
  - Month
- Derived electrical metrics

These engineered features improve model performance by exposing hidden correlations.

---

## 🗂 Dataset

The dataset contains **power system sensor readings** such as:

- Voltage
- Current
- Power Factor
- Reactive Power
- Active Power
- Time-based information

Target Variable:
Load_Type


Which represents the type of electrical load in the system.

---

## ⚙️ Installation

Clone the repository:

git clone https://github.com/yourusername/power-system-load-prediction.git
cd power-system-load-prediction

Install dependencies:
pip install -r requirements.txt

The notebook contains the full pipeline:

Data loading
Data cleaning
Feature engineering
Train-test split
Model training
Hyperparameter tuning
Ensemble stacking
Evaluation

📈 Evaluation Metrics

The models are evaluated using:

Accuracy
Confusion Matrix
Cross Validation
Feature Importance

📊 Visualization

The project includes visualizations such as:
Feature importance plots
Confusion matrix
Data distribution charts
These help interpret model performance and data patterns.

🛠 Tech Stack

Python
Scikit-learn
XGBoost
Pandas / NumPy
Matplotlib / Seaborn
Jupyter Notebook
