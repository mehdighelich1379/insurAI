# 🚗📊 InsurAI – Vehicle Insurance Risk Modeling  

Hi there! 👋  
This repository contains my project for **analyzing vehicle insurance data** and **modeling risk**.  

---

## 🎯 Project Goals
- **Classification Model** 🧮 → Predict whether a policy will result in a **claim (CLAIM_FLAG)**.  
- **Regression Model** 📈 → Estimate the actual **claim amount (CLAIM_PAID)** for policies with claims.  

---

## 🛠️ Workflow
1. **EDA & Visualization** 🔍  
   Explore and analyze the dataset to discover patterns, distributions, and risk factors.  

2. **Feature Engineering** 🧩  
   - Create new features (ratios, binary flags, log transforms, etc.).  
   - Handle missing values (NaN imputation).  

3. **Modeling** 🤖  
   - Train **CatBoostClassifier** for classification.  
   - Develop regression models to predict claim amounts.  

4. **Evaluation** 📊  
   - Metrics: Accuracy, Precision, Recall, F1-Score.  
   - Confusion Matrix & ROC Curve for classification.  
   - MAE & RMSE for regression.  

---

## 📂 Project Structure
📁 insurAI/  
┣ 📓 notebook.ipynb ← main notebook for analysis & modeling  
┣ 📁 catboost_info/ ← training logs & CatBoost outputs  
┣ 📄 .gitignore ← ignored files (logs, raw data, etc.)  
┣ 📄 README.md ← this documentation file  

---

## 📌 Current Status
✅ Initial data analysis completed  
✅ Feature engineering implemented  
✅ Classification model (CatBoost) trained and evaluated  
🚧 Regression model for claim amount is under development  

---

## 🚀 Next Steps
- Improve models with hyperparameter tuning 🔧  
- Experiment with other algorithms (XGBoost, LightGBM) 🔄  
- Build an interactive dashboard for risk visualization 📊  

---

## ⚠️ Note on Dataset & Model Performance
During exploration, I found that the **dataset has very weak signal for prediction**:  

- Correlation heatmaps show that most features have **very low correlation** with the target variables (`CLAIM_FLAG`, `CLAIM_PAID`).  
- Even after extensive **feature engineering** (ratios, log transforms, binning, vehicle age, etc.), the models could not extract strong predictive power.  
- This indicates that the dataset is **better suited for exploratory risk analysis** (e.g., claim rate trends by production year, insured value ranges, etc.) rather than high-performance predictive modeling.  

👉 **This limitation is due to the dataset itself, not the modeling process.**  
The value of this project lies in showing a **structured ML workflow** (EDA → Feature Engineering → Modeling → Evaluation) and demonstrating how to critically assess data quality before over-optimizing models.  

---

## ❤️ Acknowledgment
This project is developed as a hands-on exercise in **data science and machine learning**.  
I hope it can also serve as inspiration for others! 🌟
