# 📊 Bank Marketing Campaign Optimization

## 📌 Project Overview

This machine learning project aims to increase the efficiency of **bank direct marketing campaigns** for long-term deposit subscriptions.  
By developing **predictive models** to identify customers most likely to subscribe, we reduce unnecessary contact attempts while maintaining or improving campaign success rates.  
This project follows the **CRISP-DM (Cross-Industry Standard Process for Data Mining)** methodology.

---

## 💼 Business Problem

Banks frequently conduct direct marketing via phone calls to promote term deposits. These efforts are often **costly and inefficient** when targeting uninterested customers.

**Our goal is to build a predictive model that:**
- ✅ Identifies customers with high subscription probability  
- 📉 Reduces the number of unnecessary calls  
- 🔧 Optimizes resource allocation  
- 💰 Improves campaign ROI  

---

## 📂 Dataset

The dataset comes from a **Portuguese banking institution** and includes:

- 👤 Customer demographics: `age`, `job`, `marital status`, `education`  
- 💳 Financial indicators: `housing loan`, `personal loan`  
- 📞 Campaign-specific data: `contact method`, `campaign outcomes`  
- 📉 Economic context: `employment rate`, `consumer price index`  
- 🎯 **Target variable**: Whether the client subscribed to a term deposit (`yes`/`no`)  

---

## 🛠️ Methodology

### 🔍 Data Preprocessing
- ✅ Encoding categorical variables  
- 🔄 Standardizing numerical features  
- 🧹 Handling missing values  
- 📊 Train-test splitting with stratification  

### 📊 Baseline Establishment
- Majority class classifier: ~90% accuracy (always predicts `no`)  
- Random stratified classifier: ~11–12% precision/recall  
- Simple logistic regression: provided a performance benchmark  

---

## 🤖 Model Development

- Tested multiple algorithms:
  - Logistic Regression  
  - K-Nearest Neighbors (KNN)  
  - Decision Trees  
  - Support Vector Machines (SVM)  
- Evaluated model performance using various metrics:
  - Accuracy, Precision, Recall, ROC-AUC, Lift  

---

## 📈 Summary of Findings

### 🔹 Correlation Insights
- **Call duration** has the strongest **positive correlation** with the target (`0.41`)  
- **emp.var.rate**, **euribor3m**, and **nr.employed** are negatively correlated with the target  
  → These indicate macroeconomic factors influence client decisions  

### 🔹 Targeted Insights
- **Top responding job groups**: `students` and `retired` customers  
- **Education**: Highest positive response from `illiterate` and `university.degree` groups  
- **Contact Method**: `cellular` far outperforms `telephone`  
- **Optimal Campaign Timing**: Highest responses in **March**, **December**, and **September**

### 🔹 Top Features (from model coefficients)
- 📉 `emp.var.rate`: strong negative influence  
- 📅 `month_mar`: strong positive influence  
- ⏱️ `duration`: positive influence  
- 📞 `contact_telephone`: negative impact  

---



