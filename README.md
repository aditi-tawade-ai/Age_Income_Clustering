# Age_Income_Clustering
k-Means clustering web application using Streamlit

 📊 Age & Income K-Means Clustering

A machine learning web application built using Python and Streamlit that performs K-Means clustering on employee Age and Income data.

## 🚀 Project Overview

This application allows users to upload a CSV file containing Age and Income data. The pre-trained K-Means model processes the data and assigns each record to a cluster.

The application provides the cluster predictions in an easy-to-understand table.

## 🛠️ Technologies Used

- Python
- Pandas
- Scikit-learn
- Streamlit
- Matplotlib
- Seaborn
- Pickle

## ✨ Features

- Upload CSV dataset
- Display raw data
- Scale Age and Income data
- Predict K-Means clusters using a pre-trained model
- Display cluster predictions
- Download the prediction results as a CSV file

## 📂 Project Structure

```text
Age_Income/
│
├── app.py
├── kmeans.pkl
├── scaler.pkl
├── requirements.txt
└── README.md

##📤 Model Output (What You Get)
The model returns a cluster number for each record.
For example:
Age        Income       Cluster
22         25000            1
35         50000            0
45         80000            2
28         35000            1

##The application also provides:
📊 Cluster predictions
👀 Complete prediction table
📥 Downloadable CSV file containing the results

##🧠 How the Model Predicts Clusters
1. The model is a K-Means clustering algorithm from Scikit-learn.
2. The model was trained using Age and Income features.
3. During preprocessing, the Age and Income values were scaled using MinMaxScaler.
4. During prediction, the uploaded data is transformed using the same scaler used during training.
5. The trained K-Means model then predicts which cluster each record belongs to
6. The predicted cluster number is added to the original dataset.
In simple words:
The model looks at the Age and Income of each person and determines which group (cluster) they are most similar to

##🚀How to Run the Application
1. Create a virtual environment
  ``` python -m venv .venv
2. Activate the virtual environment
For Windows:
   ```.venv\Scripts\activate
3. Install the required libraries
   ```pip install -r requirements.txt
4. Run the Streamlit application
   ```python -m streamlit run app.py
5. The application will open in your browser at:
   ```(http://localhost:8501)

##📊 Application Workflow
Upload CSV
     ↓
Read Dataset
     ↓
Select Age & Income
     ↓
Scale Data
     ↓
Load Pre-trained K-Means Model
     ↓
Predict Clusters
     ↓
Display Results
     ↓
Download Predictions

##👩‍💻Author
Aditi Tawade

##🧑‍🏫Guide
Yameen sir
