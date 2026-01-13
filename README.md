# My_Project
# Used Car Price Predictions 
**Accurate used car price prediction in India + Powerful tool for identifying budget-friendly cars (<10 lakh)**  

## Problem Statement

The used car market in India is growing rapidly. While new car sales have slowed down in recent years, the pre-owned car market has continued to expand and is now larger than the new car market.  
For example, in 2018-19, around 3.6 million new cars were sold, while approximately 4 million second-hand cars were bought and sold.

**Biggest Challenge**:  
Most buyers hesitate to purchase a used car because they don't know the **fair market price**.

**Project Goal**:  
- Build a Machine Learning model to **accurately predict the selling price** of used cars  
- Compare different regression models and select the best one  
- Use real Indian market data (various brands, locations, features) to make reliable predictions  
- Special focus: Effectively identify and highlight **budget-friendly cars (<10 lakh)**

  **Data Dictionary (Compact)**:
- Name: Brand & Model (String)
- Location: City (String)
- Year: Manufacturing Year (int)
- Kms_Driven: Total KM (int)
- Fuel_Type: Petrol/Diesel/CNG (str)
- Transmission: Manual/Auto (str)
- Owner_Type: First/Second/Third (str)
- Mileage: kmpl/kmkg (float)
- Engine: cc (float)
- Power: bhp (float)
- Seats: Number (int)
- New_Price: New price (Lakhs, float)
- **Price**: Target - Used price (Lakhs, float)

## Project Workflow

1. **Data Loading & Cleaning**  
   - Raw data import  
   - Initial inspection & data type corrections  

2. **Exploratory Data Analysis (EDA)**  
   - Distribution analysis, correlations, trends by brand/location/fuel etc.  

3. **Outlier Detection & Handling**  
   - Identification using IQR / boxplots  
   - Capping or removal of extreme values  

4. **Missing Value Treatment**  
   - Imputation (median/mean/mode) or removal  

5. **Feature Encoding**  
   - One-Hot Encoding for categorical variables  
   - Label Encoding where needed  

6. **Model Building & Training**  
   - **Regression** (for continuous price prediction):  
     - Linear Regression  
     - Decision Tree Regressor  
     - Random Forest Regressor  
     - Grid Search CV for hyperparameter tuning  
   - **Classification** (Budget <10L vs Premium ≥10L):  
     - Same models as classifiers  
     - Precision, Recall, F1-Score, ROC-AUC Curve  

7. **Model Evaluation & Comparison**  
   - Regression: R², MAE, RMSE  
   - Classification: Confusion Matrix, ROC Curve, Feature Importance  

8. **Feature Importance & Business Insights**  
   - Top features impacting price  
   - Strong bias towards budget cars (98% recall) → Business recommendations

  **Target Variable Graph**
   - ![Price Histogram](https://raw.githubusercontent.com/Warsi_786857/My_Project/main/images/C:/Users/Warsi/Desktop/Regression & Classification/prie_histogram.png)


     




- 
