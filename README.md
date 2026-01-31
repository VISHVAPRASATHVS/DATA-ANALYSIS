# Restaurant Sales Analysis 

Project Overview:
This repository contains a comprehensive analysis of restaurant sales data. The project involves merging data from multiple sources, calculating key performance indicators (KPIs), and identifying top-performing menu items to drive business decisions.

Key Features:
Data Merging: Combines separate invoice datasets (i1.csv and i2.csv) using outer joins.
Sales Metrics: Calculates total revenue, average purchase value, and invoice counts.
Trend Analysis: Insights into daily sales and high-value transactions.
Item Performance: Identification of top 3 items by quantity sold and total revenue contribution.

Visualizations: Comparative bar charts for product performance.

Dataset Description:
The analysis is performed on restaurant invoice data containing columns such as:

Invoice No., Date, Timestamp
Item Name, Price, Qty.
Sub Total, Discount, Tax, Final Total
Category, Table No., Server Name
Key Insights from Data
Total Revenue Analyzed: ~2.39M
Average Bill Value: ~₹486
Total Unique Invoices: 4,925
Star Products: Chicken Biriyani and Butter Naan are top revenue drivers.

Requirements:
Python 3.x
Pandas
NumPy
Matplotlib

# Data Analysis EDA and Pickle

This project implements and compares Linear Regression and Random Forest Regressor models to predict a target variable based on multiple features from a provided dataset.

Project Overview:
The project follows a standard machine learning pipeline:

Data Loading: Importing the dataset using Pandas.
Exploratory Data Analysis (EDA): Checking data info, null values, and summary statistics.
Data Cleaning: Removing duplicate records.
Preprocessing: Splitting the data into training and testing sets and performing feature scaling using StandardScaler.
Model Training: Training a Linear Regression model and a Random Forest Regressor.
Evaluation: Measuring performance using Mean Squared Error (MSE), R2 Score, and Mean Absolute Error (MAE).
Visualization: Creating scatter plots to compare actual vs. predicted values.
Model Persistence: Saving the trained models and scalers using pickle for deployment.

Dataset:
The dataset (dataset-2.csv) contains 9 columns:

Features (x1 to x8): Numeric inputs representing different components or parameters.
Target: The numeric value to be predicted (e.g., Concrete Compressive Strength).
Results
Model	MSE	R2 Score	MAE
Linear Regression	~125.25	~0.58	~8.90
Random Forest	~27.06	~0.91	~3.58
Random Forest significantly outperformed Linear Regression in this task.

How to Use:
Prerequisites
Python 3.x
Libraries: numpy, pandas, matplotlib, scikit-learn

Running the Code:
Ensure dataset-2.csv is in the same directory.
Run the notebook cells sequentially.

The models will be saved as linear_regression_model.pkl and random_forest_model.pkl.

Loading the Model:
import pickle
with open('random_forest_model.pkl', 'rb') as f:
    data = pickle.load(f)
model = data['model']
scaler = data['scaler']

Visualizations:
The project includes side-by-side scatter plots comparing the prediction accuracy of both model
