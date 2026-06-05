# 💰 Salary Prediction Using Simple Linear Regression

## 📌 Project Overview

This project predicts an employee's salary based on their years of experience using the Simple Linear Regression algorithm. The model learns the relationship between experience and salary from historical data and can estimate salaries for new experience values.

The project demonstrates the complete Machine Learning workflow, including data collection, preprocessing, exploratory data analysis, model training, and evaluation.

---

## 🎯 Objective

To build a machine learning model that predicts salary based on years of professional experience.

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Scikit-Learn
* Matplotlib
* Jupyter Notebook / Google Colab
* KaggleHub

---

## 📊 Dataset Information

Dataset: Salary Dataset (Simple Linear Regression)

### Features

| Feature         | Description                    |
| --------------- | ------------------------------ |
| YearsExperience | Employee's years of experience |
| Salary          | Employee's annual salary       |

### Dataset Statistics

* Total Records: 30
* Input Feature: 1
* Target Variable: Salary
* No Missing Values
* No Duplicate Records

---

## 🔄 Project Workflow

### 1. Data Collection

Dataset downloaded using KaggleHub.

```python
path = kagglehub.dataset_download(
    "abhishek14398/salary-dataset-simple-linear-regression"
)
```

### 2. Data Preprocessing

* Load dataset
* Check data information
* Remove missing values
* Remove duplicate records
* Drop unnecessary columns

### 3. Exploratory Data Analysis

* Dataset inspection
* Correlation analysis
* Feature selection

The correlation between Years of Experience and Salary is very high, indicating a strong positive relationship.

### 4. Feature Selection

```python
X = data[['YearsExperience']]
y = data['Salary']
```

### 5. Train-Test Split

```python
from sklearn.model_selection import train_test_split

X_train, X_test, y_train, y_test = train_test_split(
    X,
    y,
    test_size=0.2,
    random_state=42
)
```

Training Data: 80%

Testing Data: 20%

### 6. Model Training

Simple Linear Regression is used to learn the relationship between experience and salary.

```python
from sklearn.linear_model import LinearRegression

model = LinearRegression()
model.fit(X_train, y_train)
```

### 7. Prediction

```python
predictions = model.predict(X_test)
```

---

## 📈 Machine Learning Algorithm

### Simple Linear Regression

Linear Regression models the relationship between:

Salary = m × (Years of Experience) + c

where:

* m = Slope
* c = Intercept

The model predicts salary by fitting the best straight line through the data points.

---

## 📂 Project Structure

```text
Salary-Prediction/
│
├── Salary_Prediction.ipynb
├── Salary_dataset.csv
├── README.md
├── requirements.txt
│
└── model/
    └── salary_prediction_model.pkl
```

---

## ▶️ Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/salary-prediction.git

cd salary-prediction
```

Install required libraries:

```bash
pip install pandas numpy scikit-learn matplotlib kagglehub
```

or

```bash
pip install -r requirements.txt
```

---

## ▶️ Run the Project

Open Jupyter Notebook:

```bash
jupyter notebook
```

Run:

```text
Salary_Prediction.ipynb
```

---

## 📊 Expected Output

Input:

```text
Years of Experience = 5
```

Output:

```text
Predicted Salary = ₹XX,XXX
```

The exact salary depends on the trained model coefficients.

---

## 🚀 Future Enhancements

* Multiple Linear Regression
* Salary Prediction Web App using Flask
* Streamlit Dashboard
* Model Deployment on Cloud
* Interactive Data Visualization

---

