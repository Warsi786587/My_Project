

# Used Car Price Prediction & Budget Classification (India Market)

**Accurate used car price prediction in India + Powerful tool for identifying budget-friendly cars (<10 lakh)**

## Problem Statement

"In recent years (2024-2025), India's used car market has surpassed new car sales, with pre-owned vehicles reaching ~5.9 million units in FY25 compared to ~4.3 million new passenger vehicles (sources: Volkswagen Indian Blue Book Report FY'25, CARS24)."


Most buyers hesitate due to uncertainty about the **fair market price**.

**Project Goal**:  
- Build ML models to **accurately predict used car selling price** (in Lakhs)  
- Compare regression models and select the best  
- Use real Indian market data for reliable predictions  
- Special focus: Effectively identify **budget cars (<10 lakh)** for price-sensitive buyers

## Data Dictionary (Key Features)
- Name: Brand & Model  
- Location: City  
- Year → CarAge (derived)  
- Kilometers_Driven  
- Fuel_Type: Petrol/Diesel/CNG  
- Transmission: Manual/Auto  
- Owner_Type: First/Second/Third  
- Mileage, Engine (cc), Power (bhp)  
- Seats  
- Price: Target (Lakhs, float)

## Tech Stack
- Python 3  
- pandas, numpy  
- matplotlib, seaborn  
- scikit-learn (LinearRegression, RandomForestRegressor, LogisticRegression, GridSearchCV, metrics)  

## Project Workflow
1. Data Loading & Cleaning  
2. EDA (distributions, correlations, trends)  
3. Outlier Handling (IQR/boxplot capping)  
4. Missing Value Imputation  
5. Feature Engineering & Encoding (One-Hot/Label)  
6. Model Building:  
   - Regression: Linear, Decision Tree, Random Forest + Tuning  
   - Classification: Tuned Logistic Regression (Budget <10L vs ≥10L)  
7. Evaluation & Interpretability  

## Key Results

**Regression (Price Prediction):**  
Best Model: **Random Forest Regressor**  
- Test R²: **0.821** (explains ~82% variance)  
- Test RMSE: **4.99 Lakhs** (average error ~₹5 lakhs)  
- Top features: Power (bhp), CarAge, Kilometers_Driven → Indian buyers prioritize performance, low age, and low usage.

**Classification (Budget <10L vs ≥10L):**  
Best Model: **Tuned Logistic Regression** (GridSearchCV: L1 penalty, C=10)  
- Test Accuracy: **~60%** (strong given ~76% premium class imbalance)  
- Recall on Budget cars (<10L): **52%** → Rarely misses affordable options  
- Ideal for recommendation engines to highlight budget-friendly cars.

**Feature Importance & Business Insights**  
- **Top price drivers** (Random Forest): Power, Car Age, Kilometers Driven dominate → buyers in India focus on engine performance and low depreciation/usage.  
- Tuned Logistic Regression excels in **budget car detection** (high recall on <10L segment) → perfect for platforms to quickly surface affordable options and target price-sensitive buyers.

**Verdict**:  
Strong regression performance (R² 0.82) for accurate pricing + reliable budget detection (52% recall on minority class) – ready for real-world use in Indian automotive marketplaces, dealerships, or apps like Cars24/OLX.

**Tech Demonstrated**: Feature engineering, hyperparameter tuning, imbalance handling, model interpretability.



  **Target Variable Graph**
  
   - <img width="3600" height="2100" alt="image" src="https://github.com/user-attachments/assets/56c406f7-ce4e-460c-8264-c22ec5b4a67d" />

   **Count Plot of Brand**

   - <img width="932" height="720" alt="image" src="https://github.com/user-attachments/assets/beb3b700-f19d-41b3-b28f-a26f7f8be6b0" />

   **Count Plot of Model**

   - <img width="564" height="596" alt="image" src="https://github.com/user-attachments/assets/45e469c1-9d98-400d-889f-120bab4f6076" />

   **Car_Age**

   - <img width="1115" height="625" alt="image" src="https://github.com/user-attachments/assets/d93db5ef-9e56-4db0-bc62-b29d17274c53" />

**Correlations Map**

- <img width="1051" height="607" alt="image" src="https://github.com/user-attachments/assets/4886720a-2f0d-42ef-8384-5ea83e0214e3" />

**Features Important in Regression**

- <img width="924" height="673" alt="image" src="https://github.com/user-attachments/assets/4cb92be1-0992-4bfb-9565-29b7333147bb" />

**Classification Important Features**










     




- 
