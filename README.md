# Sales Revenue Prediction

## Marketing Sales Revenue Prediction using KNN Regression

## Project Overview

This project predicts sales revenue using marketing campaign data and Machine Learning techniques.

The model is built using the **K-Nearest Neighbors (KNN) Regression** algorithm and deployed using **Streamlit**.

The project follows a complete end-to-end Machine Learning workflow including:

- Data Collection
- Data Cleaning & Preprocessing
- Exploratory Data Analysis (EDA)
- Feature Engineering
- Model Building
- Hyperparameter Tuning
- Model Deployment

---

## Objective

The objective of this project is to predict **sales revenue** based on various marketing-related factors such as:

- Ad Spend
- Price
- Discount Rate
- Market Reach
- Impressions
- Click Through Rate (CTR)
- Competition Index
- Customer Segment
- Marketing Channel
- Product Category

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Streamlit
- Pickle

---

## Dataset

The project uses an **E-commerce Marketing and Sales dataset** containing marketing campaign performance and sales-related features.

### Files Used
- `train.csv`
- `test.csv`

The datasets were merged and later split using `train_test_split()` for model training and evaluation.

---

## Workflow

### 1. Data Collection
Collected marketing campaign and sales data from the dataset.

### 2. Data Cleaning & Preprocessing

Performed the following preprocessing steps:

- Converted date column to datetime format
- Handled missing values using **median** and **mode**
- Standardized inconsistent categorical values  
  (e.g., *North, north, NORTH → North*)
- Removed duplicate records
- Applied **One-Hot Encoding** for categorical variables
- Performed **outlier analysis using IQR method**
- Applied **log transformation (`log1p`)** to reduce skewness
- Applied **RobustScaler** for feature scaling

### 3. Feature Engineering

Extracted time-based features from the date column:

- Year
- Month
- Day
- Weekday
- Hour

### 4. Exploratory Data Analysis (EDA)

Performed analysis on:

- Feature distributions
- Correlation between variables
- Marketing channel effectiveness
- Pricing and discount impact
- Customer segment performance
- Feature relationships with sales revenue

### 5. Model Building

Implemented **K-Nearest Neighbors Regressor (KNN)**.

Model experimentation included:

- Testing **Uniform** and **Distance** weights
- Evaluating **K values from 1 to 120**
- Selecting best parameters based on performance metrics

### 6. Hyperparameter Tuning

### Best Model Configuration

- **Best K Value:** 13
- **Best Weight:** Distance

### 7. Model Evaluation

The model was evaluated using:

- MAE (Mean Absolute Error)
- MSE (Mean Squared Error)
- RMSE (Root Mean Squared Error)
- R² Score

### Final Model Performance

- **MAE ≈ 23.02**
- **R² Score ≈ 0.63**

---

## Key Insights / Observations

### Positive Factors Influencing Revenue
- Higher **Click Through Rate (CTR)** increases revenue
- Better **Market Reach** improves sales
- **Seasonal periods** positively impact revenue

### Negative Factors Influencing Revenue
- Higher **Price** reduces revenue
- Higher **Competition Index** decreases sales
- Large **Discount Rates** show weak negative impact

### Marketing Channel Performance
- **Influencer Marketing** performs best
- **Social Media** is the second-best channel
- **TV advertising** performs the worst

### Customer Segment Analysis
- **Premium customers** generate slightly higher revenue than Budget and Standard customers

---

## Model Deployment

The trained model is deployed using **Streamlit**.

Users can:

- Enter marketing-related input values
- Predict sales revenue instantly

---

## Project Structure

```text
project_folder/
│── app.py
│── code.ipynb
│── knn_model.pkl
│── scaler.pkl
│── columns.pkl
│── requirements.txt
│── train.csv
│── test.csv
│── README.md
```
## How to Run the Project
```
pip install -r requirements.txt
streamlit run app.py
```
## Future Improvements
- Experiment with models like Random Forest and XGBoost
- Improve feature engineering
- Perform advanced feature selection
- Improve model accuracy
- Deploy the project on cloud platforms
- Conclusion

## This project demonstrates a complete Machine Learning pipeline involving:

- Data preprocessing
- Exploratory Data Analysis (EDA)
- Feature engineering
- Model training
- Hyperparameter tuning
- Model deployment using Streamlit

The project provides practical experience in building and deploying a regression-based Machine Learning application for sales revenue prediction.
