# Age_Income_Clustering
# 👥 Employee Income Segmentation using K-Means Clustering

## 📌 Project Overview

This project uses the **K-Means Clustering** algorithm to group employees into different clusters based on their **Age** and **Income**.

The goal of this project is to identify groups of employees with similar age and income characteristics using an **unsupervised machine learning** approach.

The trained K-Means model and scaler are saved as `.pkl` files and can be used for making predictions on new employee data.

---

## 🎯 Objective

The main objective of this project is to segment employees into groups based on:

* Age
* Income

Unlike supervised learning, this project does not require a target variable. The K-Means algorithm automatically groups similar data points into clusters.

---

## 📊 Dataset

The dataset contains **24 employee records** and three columns:

| Column | Description            |
| ------ | ---------------------- |
| Name   | Name of the employee   |
| Age    | Age of the employee    |
| Income | Income of the employee |

### Features used for clustering

```text
Age
Income
```

`Name` is an identifying column and is not used for clustering.

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
* Joblib
* Streamlit

---

## 🤖 Machine Learning Algorithm

### K-Means Clustering

K-Means is an **unsupervised machine learning algorithm** used to divide data into a predefined number of clusters.

The algorithm works by:

1. Choosing the number of clusters `K`
2. Initializing cluster centroids
3. Assigning each data point to the nearest centroid
4. Recalculating the centroids
5. Repeating the process until the clusters stabilize

---

## 🔍 Choosing the Number of Clusters

The number of clusters can be selected using methods such as:

* Elbow Method
* Silhouette Score
* Domain Knowledge

In this project, the final K-Means model uses:

```text
Number of Clusters (K) = 5
```

The saved model is configured with **5 clusters**, `n_init=10`, `max_iter=100`, and `random_state=42`.

---

## 📏 Data Scaling

Since Age and Income have different numerical ranges, the data is scaled before applying K-Means.

A **MinMaxScaler** is used to scale the features.

```python
from sklearn.preprocessing import MinMaxScaler

scaler = MinMaxScaler()
X_scaled = scaler.fit_transform(X)
```

The trained scaler is saved as:

```text
scaler.pkl
```

---

## 🔄 Machine Learning Workflow

```text
Dataset
   ↓
Data Analysis
   ↓
Select Age & Income
   ↓
Feature Scaling
   ↓
Choose K
   ↓
K-Means Clustering
   ↓
Create Clusters
   ↓
Visualize Clusters
   ↓
Save Model
   ↓
Deployment
```

---

## 💾 Model Saving

The trained K-Means model is saved using Joblib:

```python
import joblib

joblib.dump(kmeans, "kmeans.pkl")
```

The scaler is also saved:

```python
joblib.dump(scaler, "scaler.pkl")
```

These files are used during deployment.

---

## 📁 Project Structure

```text
Employee_Income_Clustering/
│
├── app.py
├── Employee_income_1.csv
├── kmeans.pkl
├── scaler.pkl
├── requirements.txt
└── README.md
```

---

## 🌐 Deployment

The trained K-Means model can be deployed using **Streamlit**.

The application can accept:

```text
Age
Income
```

The entered values are first scaled using the saved `scaler.pkl` and then passed to the saved K-Means model.

The model returns the cluster to which the employee belongs.

---

## ⚙️ Installation

Create a virtual environment:

```bash
python -m venv venv
```

Activate the virtual environment on Windows:

```bash
venv\Scripts\activate
```

Install the required libraries:

```bash
pip install -r requirements.txt
```

---

## 📦 Requirements

Create a `requirements.txt` file containing:

```text
pandas
numpy
scikit-learn
joblib
streamlit
matplotlib
seaborn
```

---

## ▶️ Run the Application

Run the following command in the VS Code terminal:

```bash
streamlit run app.py
```

The Streamlit application will open in the browser.

---

## 📌 Example Application Flow

The user enters:

```text
Age: 35
Income: 90000
```

The application:

```text
User Input
    ↓
MinMaxScaler
    ↓
K-Means Model
    ↓
Cluster Prediction
```

The application then displays the cluster assigned to the employee.

---

## 📚 Key Learning Outcomes

Through this project, I learned:

* Unsupervised Machine Learning
* K-Means Clustering
* Selecting the value of K
* Elbow Method
* Feature scaling
* MinMaxScaler
* Cluster formation
* Cluster prediction
* Data visualization
* Model serialization using Joblib
* Machine learning model deployment using Streamlit

---

## 📈 Project Insights

The clustering approach helps identify groups of employees with similar **age and income patterns**.

These clusters can potentially be useful for:

* Employee segmentation
* Income-level analysis
* Workforce analysis
* Identifying similar employee groups
* Data-driven business analysis

---

## 👩‍💻 Project Details

**Author:** Aditi Tawade

**Guide:** Yameen Hakim Sir

**Degree:** B.Tech — Electronics & Telecommunication Engineering

---

## ⭐ Conclusion

This project demonstrates the implementation of an **unsupervised machine learning workflow using K-Means Clustering**.

The project starts with employee data, scales the numerical features, applies K-Means clustering with **5 clusters**, saves the trained model and scaler, and prepares the model for deployment using Streamlit.

It provides practical experience in **clustering, feature scaling, data analysis, model persistence, and machine learning deployment**.

---

## 🚧 Project Status

**Completed & Deployed**

This project is part of my ongoing journey of building practical skills in **Python, Data Science, and Machine Learning**.

