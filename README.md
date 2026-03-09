# 🌸 Iris Flower Classification using Naive Bayes

## 📌 Project Overview
This project performs **classification on the Iris dataset** using the **Naive Bayes Machine Learning algorithm**.  
The goal is to predict the **species of an iris flower** based on its physical features such as sepal and petal measurements.

The project demonstrates the **complete machine learning workflow**, including data exploration, preprocessing, model training, and evaluation using Python and Scikit-learn.

---

## 📂 Dataset
The dataset used is the **Iris dataset**, one of the most popular datasets in machine learning.

### Features
- Sepal Length
- Sepal Width
- Petal Length
- Petal Width

### Target
- Iris-setosa
- Iris-versicolor
- Iris-virginica

---

## 🛠 Technologies Used

| Technology | Purpose |
|------------|--------|
| Python | Programming Language |
| Pandas | Data manipulation |
| NumPy | Numerical operations |
| Scikit-learn | Machine learning algorithms |
| Jupyter Notebook | Development environment |

---

## ⚙️ Project Workflow

```
Dataset Loading
      ↓
Data Exploration
      ↓
Feature Selection
      ↓
Train-Test Split
      ↓
Feature Scaling
      ↓
Model Training (Naive Bayes)
      ↓
Prediction
      ↓
Model Evaluation
```

---

## 📊 Steps Implemented in the Project

### 1️⃣ Import Required Libraries
Libraries used for data processing and machine learning.

- pandas
- numpy
- sklearn

---

### 2️⃣ Load the Dataset

The Iris dataset is loaded into a **Pandas DataFrame**.

```python
df = pd.read_csv("Iris.csv")
```

---

### 3️⃣ Data Exploration

Basic dataset inspection was performed using:

- `head()`
- `tail()`
- `describe()`
- `dtypes`
- `columns`

These functions help understand:
- dataset structure
- statistical summary
- feature types

---

### 4️⃣ Data Cleaning

The **Id column** is unnecessary for prediction, so it is removed.

```python
df.drop("Id", axis=1)
```

---

### 5️⃣ Feature and Target Separation

Features (`X`) and target (`y`) are separated.

```python
X = df.iloc[:, :-1]
y = df.iloc[:, -1]
```

---

### 6️⃣ Train-Test Split

The dataset is split into **training and testing sets**.

- **70% Training Data**
- **30% Testing Data**

```python
train_test_split(X, y, test_size=0.3, random_state=42)
```

---

### 7️⃣ Feature Scaling

Standardization is applied to normalize the feature values.

```python
from sklearn.preprocessing import StandardScaler
scaler = StandardScaler()
```

This ensures all features contribute equally to the model.

---

### 8️⃣ Model Building

The **Gaussian Naive Bayes classifier** is used.

```python
from sklearn.naive_bayes import GaussianNB
model = GaussianNB()
model.fit(X_train, y_train)
```

Naive Bayes is based on **Bayes' Theorem** and assumes independence between features.

---

### 9️⃣ Prediction

The trained model predicts the species of flowers in the test dataset.

```python
y_pred = model.predict(X_test)
```

---

### 🔟 Model Evaluation

Accuracy is calculated to measure model performance.

```python
from sklearn.metrics import accuracy_score
accuracy_score(y_test, y_pred)
```

---

## 📈 Result

The model successfully classifies iris flower species with **high accuracy** using the Naive Bayes algorithm.

---

## 📚 Learning Outcomes

Through this project, the following concepts were understood:

✔ Data preprocessing  
✔ Feature scaling  
✔ Train-test splitting  
✔ Machine learning model training  
✔ Classification using Naive Bayes  
✔ Model evaluation using accuracy score  

---

## 🚀 Future Improvements

Possible enhancements include:

- Visualization of dataset using **Matplotlib or Seaborn**
- Testing other models like:
  - Logistic Regression
  - Decision Trees
  - KNN
- Comparing model performances

---

## 👩‍💻 Author

**Shana Parveen KT**

Data Science Student  
Passionate about **Mathematics, Data Science, and Machine Learning**

---

⭐ If you found this project helpful, feel free to give it a star!
