# 💳 Credit Card Fraud Detection

A machine learning project that identifies fraudulent credit card transactions using multiple classification algorithms. The project focuses on handling a highly imbalanced dataset and compares different models to determine the most effective approach for fraud detection.

---

## 📌 Project Overview

Credit card fraud detection is a binary classification problem where the objective is to classify a transaction as either:

- **0 → Genuine Transaction**
- **1 → Fraudulent Transaction**

Since fraudulent transactions represent only a very small fraction of the dataset, the problem is highly imbalanced. Simply relying on accuracy can produce misleading results, so this project uses additional evaluation metrics such as Precision, Recall, F1-Score, ROC-AUC, and Confusion Matrix.

---

## 🎯 Objectives

- Explore and understand the credit card transaction dataset.
- Perform data cleaning and preprocessing.
- Handle class imbalance using SMOTE.
- Train multiple machine learning models.
- Compare model performance using different evaluation metrics.
- Save the trained model for future predictions.

---

## 📂 Dataset

This project uses the **Credit Card Fraud Detection** dataset from Kaggle.

### Dataset Information

| Property | Value |
|----------|-------|
| Total Transactions | 284,807 |
| Genuine Transactions | 284,315 |
| Fraud Transactions | 492 |
| Fraud Percentage | 0.17% |

The dataset contains anonymized numerical features generated using PCA.

Features include:

- Time
- Amount
- V1 – V28 (PCA Components)
- Class (Target Variable)

> **Note:** The dataset is not included in this repository because it exceeds GitHub's file size limit. You can download it from Kaggle and place `creditcard.csv` inside the project folder before running the notebook.

---

# 📁 Project Structure

```text
Credit_Card_Fraud_Detection/
│
├── Graphs/
│   ├── class_distribution.png
│   ├── confusion_matrix_lr.png
│   ├── confusion_matrix_rf.png
│   ├── confusion_matrix_xgb.png
│   ├── correlation_heatmap.png
│   ├── feature_importance.png
│   ├── fraud_pie_chart.png
│   └── roc_curve.png
│
├── Models/
│   ├── best_model.pkl
│   └── scaler.pkl
│
├── Result/
│   └── model_comparison.csv
│
├── Credit_Card_Fraud_detection.ipynb
├── requirements.txt
├── README.md
└── .gitignore
```

---

# ⚙️ Workflow

The project follows the following workflow:

### 1. Data Loading

- Imported dataset
- Examined dataset shape
- Displayed first few records

### 2. Data Exploration

- Checked missing values
- Checked duplicate records
- Removed duplicate transactions
- Analyzed class distribution

### 3. Data Visualization

Generated visualizations including:

- Class Distribution
- Genuine vs Fraud Percentage
- Correlation Heatmap
- ROC Curve
- Feature Importance
- Confusion Matrices

### 4. Data Preprocessing

- Feature scaling using StandardScaler
- Train-Test Split (80:20)
- Applied SMOTE only on the training data

### 5. Model Training

Three different machine learning models were trained:

- Logistic Regression
- Random Forest
- XGBoost

### 6. Model Evaluation

Each model was evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC Score
- Confusion Matrix

---

# 📊 Model Performance

| Model | Accuracy | Precision | Recall | F1 Score |
|--------|----------|-----------|---------|----------|
| Logistic Regression | 0.9737 | 0.0530 | 0.8737 | 0.1000 |
| Random Forest | 0.9994 | 0.8875 | 0.7474 | 0.8114 |
| XGBoost | 0.9947 | 0.2192 | 0.8421 | 0.3478 |

---

# 🏆 Best Performing Model

Among the three models, **Random Forest** achieved the highest F1-Score while maintaining excellent precision and accuracy.

It was selected as the final model and saved using **Joblib**.

---

# 📈 Visualizations Included

The repository contains the following plots:

- Class Distribution
- Genuine vs Fraud Pie Chart
- Correlation Heatmap
- ROC Curve Comparison
- Random Forest Feature Importance
- Logistic Regression Confusion Matrix
- Random Forest Confusion Matrix
- XGBoost Confusion Matrix

---

# 🧰 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- Imbalanced-learn (SMOTE)
- Joblib

---

# ▶️ How to Run

### Clone the repository

```bash
git clone https://github.com/tushar-ydv01/Credit_Card_Fraud_Detection.git
```

### Open the project

```bash
cd Credit_Card_Fraud_Detection
```

### Install required libraries

```bash
pip install -r requirements.txt
```

### Download Dataset

Download the Credit Card Fraud Detection dataset from Kaggle and place the `creditcard.csv` file inside the project directory.

### Run

Open the notebook and execute all cells sequentially.

---

# 📚 Key Learnings

Through this project I gained practical experience in:

- Working with real-world imbalanced datasets
- Data preprocessing and visualization
- Applying SMOTE for class balancing
- Comparing multiple classification models
- Understanding Precision, Recall and F1-Score
- Saving and loading trained machine learning models
- Evaluating models using ROC Curve and Confusion Matrix

---

# 🚀 Future Improvements

Possible enhancements include:

- Hyperparameter tuning
- Cross-validation
- Streamlit web application
- Model deployment
- Experimenting with LightGBM and CatBoost
- Real-time fraud prediction API

---

# 👨‍💻 About Me

I am **Tushar Yadav**, a B.Tech Computer Science student with an interest in Machine Learning, Data Science, and Artificial Intelligence.

This project was developed to strengthen my practical understanding of machine learning workflows, model evaluation, and handling real-world datasets.

---

## ⭐ If you found this project useful, consider giving it a star.