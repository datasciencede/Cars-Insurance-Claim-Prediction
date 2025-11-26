# 🚗 Car Insurance Claim Prediction -- EDA & Machine Learning Project

## 📌 Project Overview

This project focuses on predicting **car insurance claim amounts** and
identifying whether a customer is likely to make a claim. It combines:

-   ✔ Exploratory Data Analysis (EDA)\
-   ✔ Data Cleaning & Preprocessing\
-   ✔ Multiple Machine Learning Models\
-   ✔ An Interactive Streamlit Web App\
-   ✔ Downloadable Predictions

The dataset includes customer demographics, vehicle details, income
level, car age, previous claims, and more. The goal is to help insurance
firms estimate claim risks and understand customer claim behavior.

------------------------------------------------------------------------

## 📂 Features of the Application

### 🔍 1. Show Raw Dataset

Displays the first few rows of the dataset for quick inspection.

### 📈 2. Numerical Column Distribution

Visualizes the distribution of numerical features using Seaborn
histograms.

### 🔥 3. Correlation Heatmap

Shows relationships among features using a correlation matrix and
heatmap.

### 🤖 4. Model Building

Users can:\
- Select features\
- Choose machine learning models:\
- **Linear Regression**\
- **Decision Tree Regressor**\
- **SVM Classifier** (binary: claim/no claim)\
- Train model\
- View model metrics: - **Regression Models**: MSE, MAE, R²\
- **Classification Model**: Accuracy, Classification Report, Confusion
Matrix\
- Download predictions as CSV

### 🎯 5. Make Predictions

Users can manually enter customer details to predict: - **Claim Amount**
(Regression)\
- **Claim or No Claim** (Classification -- SVM)

------------------------------------------------------------------------

## 📊 Dataset

Dataset includes:

-   AGE\
-   INCOME\
-   HOME_VAL\
-   BLUEBOOK\
-   CAR_AGE\
-   CLM_FREQ\
-   CLM_AMT\
-   Customer & vehicle demographics\
-   Previous claim history

------------------------------------------------------------------------

## 🧹 Data Preprocessing Steps

### ✔ Dropped Unnecessary Columns

`ID`, `BIRTH`, `OCCUPATION`, `CAR_TYPE`, `CLAIM_FLAG`

### ✔ Converted Categorical Values

Mapped to numerical values:\
- Yes/No → 1/0\
- Education Level → 0 (Low) to 3 (PhD)\
- Vehicle & region category mapping

### ✔ Cleaned Monetary Columns

Removed symbols like `$` and `,` and converted to float.

### ✔ Missing Value Treatment

Used mean or median imputation for:\
- AGE\
- YOJ\
- INCOME\
- HOME_VAL\
- CAR_AGE

------------------------------------------------------------------------

## 🔍 Exploratory Data Analysis

### 📦 Distribution Plots

Shows spread, skewness, and outliers for numerical columns.

### 🔥 Correlation Heatmap

Helps identify feature relationships and improve model feature
selection.

------------------------------------------------------------------------

## 🤖 Machine Learning Models Used

### 1️⃣ Linear Regression

Predicts **exact claim amount**.

### 2️⃣ Decision Tree Regressor

A non-linear alternative for predicting claim amount.

### 3️⃣ Support Vector Machine (SVM)

Used as a **binary classifier**:\
- Claim (1)\
- No Claim (0)

------------------------------------------------------------------------

## 📈 Model Evaluation Metrics

### **Regression Models**

-   Mean Squared Error (MSE)\
-   Mean Absolute Error (MAE)\
-   R-squared Score

### **SVM Classifier**

-   Accuracy Score\
-   Classification Report\
-   Confusion Matrix (Heatmap)

------------------------------------------------------------------------

## 🎨 Visualizations Included

-   Claim amount distribution\
-   Correlation heatmap\
-   Histograms for numerical columns\
-   Actual vs Predicted scatter plot\
-   Confusion Matrix (SVM)

------------------------------------------------------------------------

## 📁 Project Structure

📦 Cars-Insurance-Claim-Prediction/\
├── car_insurance.py\
├── car_insurance_claim.csv\
├── README.md\
└── requirements.txt (optional)

------------------------------------------------------------------------

## ▶️ Running the App

### 1. Install Dependencies

    pip install streamlit pandas numpy seaborn scikit-learn matplotlib

### 2. Run Streamlit

    streamlit run car_insurance.py

------------------------------------------------------------------------

## 🎯 Final Insights

-   Claim amount is influenced by income, vehicle value, car age, and
    previous claims.\
-   Regression models work well for estimating claim amounts.\
-   SVM effectively predicts **claim vs. no claim**.\
-   Streamlit UI makes EDA and modeling interactive and user‑friendly.

------------------------------------------------------------------------

## 🧠 Future Scope

-   Add advanced ML models (Random Forest, XGBoost, ANN)\
-   Deploy the app on cloud platforms\
-   Implement feature engineering\
-   Add outlier handling & scaling\
-   Build a complete automated ML pipeline
