# PowerCo Customer Churn Analysis and Prediction

## 📌 Overview
This project analyzes **customer churn** for PowerCo, an energy provider, using **EDA and Random Forest classification**. The main objective is to determine whether **customer churn is driven by price sensitivity**. The dataset contains various **customer attributes, electricity consumption, pricing details, and contract information**.

## 📂 Contents
1. [Introduction](#-introduction)  
2. [Data Exploration & Cleaning](#-data-exploration--cleaning)  
3. [Feature Engineering](#-feature-engineering)  
4. [Modeling: Random Forest](#-modeling-random-forest)  
5. [Key Findings & Insights](#-key-findings--insights)  
6. [Conclusion](#-conclusion)  
7. [How to Run the Project](#-how-to-run-the-project)  

---

## 📖 Introduction
Customer churn is a major concern for **PowerCo**. This project aims to:
✔ **Predict customer churn** using a **Random Forest model**.  
✔ **Analyze key factors influencing churn**, with a focus on price sensitivity.  
✔ **Provide business insights** for retention strategies.

---

## 🔍 Data Exploration & Cleaning
- **Datasets Used:**
  - `client_data.csv` – Customer details, energy consumption, contract data.
  - `price_data.csv` – Energy pricing per time period.
- **Missing Values Handling:**
  - Imputed missing values in **contract end dates, competition distances, and pricing fields**.
- **Data Types Fixing:**
  - Converted date columns to **datetime format**.
  - Encoded categorical variables like **sales channels and customer origin codes**.

---

## 🛠 Feature Engineering
✔ **Created New Features:**
   - `contract_duration`: Time between contract activation and renewal.
   - `price_sensitivity`: Difference between forecasted and actual energy costs.
   - `customer_loyalty`: Based on number of years as a client.
✔ **Encoded Categorical Variables:**
   - One-hot encoding for categorical columns.
✔ **Scaled Numerical Features:**
   - Standardized energy consumption and pricing values.

---

## 🤖 Modeling: Random Forest
### **1️⃣ Model Training**
✔ **Train-Test Split:** 75% training, 25% testing.  
✔ **Random Forest Classifier** was selected due to:
   - Ability to handle **categorical and numerical features**.
   - **Feature importance ranking** to interpret key churn drivers.

### **2️⃣ Hyperparameter Tuning**
✔ **GridSearchCV** was used to optimize:
   - Number of trees (`n_estimators`)
   - Maximum tree depth (`max_depth`)
   - Minimum samples per split (`min_samples_split`)

---

## 📊 Key Findings & Insights
✔ **Top Features Driving Churn:**
   - **Contract Length:** Shorter contracts correlated with more churn.
   - **Energy Consumption:** Lower consumption customers showed a higher churn rate.
   - **Price Sensitivity:** While it has some effect, it is not a primary driver of churn.
   
✔ **Price Sensitivity & Churn:**
   - Customers who experienced a higher-than-expected energy price increase **showed some churn tendency**, but price sensitivity was not a dominant factor.
   - Suggests that **competitive pricing strategies alone may not be enough to prevent churn** and other retention efforts should be explored.

---

## ✅ Conclusion
✔ **Churn is primarily influenced by contract length and energy consumption**, with price sensitivity playing only a minor role.  
✔ **PowerCo should focus on personalized contract renewal strategies and customer loyalty programs.**  
✔ **Future Work:** Consider **Gradient Boosting models (XGBoost) or time series forecasting** to improve churn prediction.

---


