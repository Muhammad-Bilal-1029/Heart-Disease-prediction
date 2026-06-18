# ❤️ Heart Disease Prediction Using Machine Learning

## 📌 Project Overview

Heart disease is one of the leading causes of death worldwide. Early detection can significantly improve treatment outcomes and reduce health risks.

This project uses multiple Machine Learning algorithms to predict whether a patient is likely to have heart disease based on various medical attributes. The project compares the performance of different classification models and evaluates them using standard machine learning metrics.

---

## 🎯 Objectives

* Predict the presence of heart disease in patients.
* Compare multiple machine learning algorithms.
* Evaluate model performance using classification metrics.
* Identify the most effective model for heart disease prediction.

---

## 🛠 Technologies Used

### Programming Language

* Python

### Libraries

* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* XGBoost

---

## 📂 Dataset

The project uses the **Heart Disease Dataset** (`heart.csv`).

### Features Included

| Feature  | Description                       |
| -------- | --------------------------------- |
| age      | Age of patient                    |
| sex      | Gender                            |
| cp       | Chest pain type                   |
| trestbps | Resting blood pressure            |
| chol     | Cholesterol level                 |
| fbs      | Fasting blood sugar               |
| restecg  | Resting ECG results               |
| thalach  | Maximum heart rate achieved       |
| exang    | Exercise-induced angina           |
| oldpeak  | ST depression                     |
| slope    | Slope of peak exercise ST segment |
| ca       | Number of major vessels           |
| thal     | Thalassemia                       |
| target   | Heart Disease (0 = No, 1 = Yes)   |

---

## 🔄 Project Workflow

### 1. Data Loading

The dataset is loaded using Pandas.

```python
df = pd.read_csv("heart.csv")
```

---

### 2. Feature Selection

Input features and target variable are separated.

```python
X = df.drop("target", axis=1)
y = df["target"]
```

---

### 3. Train-Test Split

The dataset is divided into:

* 80% Training Data
* 20% Testing Data

```python
train_test_split(
    X,
    y,
    test_size=0.2,
    random_state=42,
    stratify=y
)
```

---

### 4. Feature Scaling

Standardization is applied to improve model performance for algorithms such as Logistic Regression and SVM.

```python
scaler = StandardScaler()
```

---

### 5. Machine Learning Models

The following classification algorithms are trained and compared:

#### Logistic Regression

A statistical model used for binary classification problems.

#### Support Vector Machine (SVM)

Finds the optimal decision boundary between classes.

#### Random Forest

An ensemble learning algorithm that combines multiple decision trees.

#### XGBoost

A powerful gradient boosting algorithm widely used in machine learning competitions and real-world applications.

---

### 6. Model Evaluation

Each model is evaluated using:

* Accuracy
* Precision
* Recall
* F1 Score
* ROC-AUC Score

```python
accuracy_score()
precision_score()
recall_score()
f1_score()
roc_auc_score()
```

---

## 📊 Evaluation Metrics

| Metric    | Description                            |
| --------- | -------------------------------------- |
| Accuracy  | Overall prediction correctness         |
| Precision | Correct positive predictions           |
| Recall    | Ability to detect heart disease cases  |
| F1 Score  | Balance between Precision and Recall   |
| ROC-AUC   | Ability to distinguish between classes |

---

## 🚀 How to Run the Project

### Clone the Repository

```bash
git clone https://github.com/Muhammad-Bilal-1029/heart-disease-prediction.git
```

### Navigate to Project Directory

```bash
cd heart-disease-prediction
```

### Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost
```

### Run the Program

```bash
python heart_disease_prediction.py
```

---

## 📈 Sample Output

```text
==================================================
Logistic Regression
==================================================
Accuracy: 0.89
Precision: 0.88
Recall: 0.90
F1 Score: 0.89
ROC-AUC: 0.93

==================================================
SVM
==================================================
Accuracy: 0.91
Precision: 0.90
Recall: 0.92
F1 Score: 0.91
ROC-AUC: 0.95
```

---

## 📊 Models Compared

| Model               | Type                   |
| ------------------- | ---------------------- |
| Logistic Regression | Linear Model           |
| SVM                 | Support Vector Machine |
| Random Forest       | Ensemble Learning      |
| XGBoost             | Gradient Boosting      |

---

## 🔍 Key Findings

* Multiple machine learning models were evaluated.
* Feature scaling improved the performance of Logistic Regression and SVM.
* Ensemble methods such as Random Forest and XGBoost generally provide strong predictive performance.
* ROC-AUC Score provides a reliable measure of classification effectiveness.

---

## 🔮 Future Improvements

* Hyperparameter tuning using GridSearchCV.
* Cross-validation for robust evaluation.
* Feature importance visualization.
* Interactive dashboard using Flask or Streamlit.
* Deployment on cloud platforms.
* Integration with real-time patient data.

---

## 📚 Machine Learning Concepts Used

* Classification
* Data Preprocessing
* Feature Scaling
* Model Comparison
* Performance Evaluation
* Ensemble Learning
* Gradient Boosting

---

## 👨‍💻 Author

**Muhammad Bilal**

Machine Learning Enthusiast | AI Engineer |  pyrhon Programmer

---

## 📄 License

Feel free to use, modify, and distribute this project for educational and research purposes.
