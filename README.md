# Cars-Insurance-Claim-Prediction🚗 Car Insurance Claim Prediction – EDA & Machine Learning Project



📌 Project Overview

This project focuses on predicting car insurance claim amounts and identifying whether a customer is likely to make a claim. It combines:

✔ Exploratory Data Analysis (EDA)

✔ Data Cleaning & Preprocessing

✔ Multiple Machine Learning Models

✔ An Interactive Streamlit Web App

✔ Downloadable Predictions

The dataset includes customer demographics, vehicle details, income, car age, previous claims, and more. The goal is to help insurance firms estimate claim risks and understand customer claim behavior.

📂 Features of the Application
🔍 1. Show Raw Dataset

Displays the first few rows of the dataset for quick inspection.

📈 2. Numerical Column Distribution

Visualizes distribution of numerical features using Seaborn histograms.

🔥 3. Correlation Heatmap

Shows relationships among features using a correlation matrix + heatmap.

🤖 4. Model Building

Users can:

Select features

Choose ML model:

Linear Regression

Decision Tree Regressor

SVM Classifier (binary claim/no-claim)

Train model

View metrics:

MSE, MAE, R² (Regression)

Accuracy, Report, Confusion Matrix (SVM)

Download predictions as CSV

🎯 5. Make Predictions

Users can input manual customer data to predict:

Claim Amount (Regression)

Claim or No Claim (Classification – SVM)

📊 Dataset

The dataset contains customer, vehicle, claim, and income information.
Columns include:

AGE

INCOME

HOME_VAL

BLUEBOOK

CAR_AGE

CLM_FREQ

CLM_AMT

Vehicle/Driver Demographics

Previous claim history

🧹 Data Preprocessing Steps
✔ Dropped Unnecessary Columns

ID, BIRTH, OCCUPATION, CAR_TYPE, CLAIM_FLAG

✔ Converted Categorical Values

Mapped to numerical values:

Yes/No → 1/0

Education Level → Encoded (0 to 3)

Vehicle & region attributes → Numeric

✔ Cleaned Monetary Columns

Removed $ and , and converted to float.

✔ Missing Value Treatment

Used mean or median imputation for:

AGE

YOJ

INCOME

HOME_VAL

CAR_AGE

🔍 Exploratory Data Analysis
📦 Distribution Plots

Understanding spread & skewness of numerical columns

Useful to detect outliers and claim patterns

🔥 Correlation Heatmap

Visualizes feature relationships

Helps in feature selection for ML models

🤖 Machine Learning Models Used
1️⃣ Linear Regression

Used for predicting exact claim amount.

2️⃣ Decision Tree Regressor

A non-linear model for claim amount prediction.

3️⃣ Support Vector Machine (SVM)

Used as a binary classifier:

Claim (1)

No Claim (0)

Since SVM doesn’t support regression directly, target values are converted to binary:

y_train = (y_train > 0).astype(int)

📈 Model Evaluation Metrics
For Regression Models:

Mean Squared Error (MSE)

Mean Absolute Error (MAE)

R-squared Score

For SVM Classification:

Accuracy Score

Classification Report

Confusion Matrix (Heatmap)

🎨 Visualizations Included

Claim amount distribution

Correlation heatmap

Numerical feature histograms

Actual vs Predicted scatter plot

Confusion matrix (SVM)

📁 Project Structure
📦 Cars-Insurance-Claim-Prediction/
├── car_insurance.py
├── car_insurance_claim.csv
├── README.md
└── requirements.txt (optional)

▶️ Running the App
1. Install Dependencies
pip install streamlit pandas numpy seaborn scikit-learn matplotlib

2. Run Streamlit App
streamlit run car_insurance.py

🎯 Final Insights

Claim amount is influenced by income, vehicle value, previous claims, and car age.

Simple regression models perform well for numerical predictions.

SVM provides a strong classification approach for predicting claim vs. no claim.

The Streamlit interface allows interactive EDA + modeling without coding.

🧠 Future Scope

Add advanced ML models (Random Forest, XGBoost, ANN)

Deploy app on cloud (Streamlit Cloud / AWS / GCP)

Add feature engineering

Add outlier handling & scaling

Create a complete automated ML pipeline

