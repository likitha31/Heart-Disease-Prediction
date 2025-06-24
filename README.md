# Heart Disease Prediction

A machine learning project to predict heart disease using clinical data from the UCI Heart Disease dataset. Built and evaluated multiple models, with a focus on balancing accuracy and recall for early detection.

## 📊 Key Highlights
- Cleaned and explored 296 patient records with 14 features
- Identified key predictors like chest pain type, ST slope, and major vessels
- Tested 12+ models including Logistic Regression, Random Forest, and XGBoost
- **Final Model**: LightGBM with 86% accuracy and 94% recall
- Used **SHAP** for explainability to identify top contributing features

## ⚙️ Tools & Libraries
Python, Pandas, Scikit-learn, LightGBM, SHAP, Matplotlib, Seaborn

## 📁 Project Structure
- `notebooks/` – EDA and modeling notebooks
- `data/` – Cleaned dataset
- `visuals/` – Plots and SHAP summaries
- `README.md` – This file

## 🔍 Try It Yourself
1. Clone the repo  
2. Install dependencies: `pip install -r requirements.txt`  
3. Run the notebook in `notebooks/` to explore the data and models

## 📎 Dataset
[UCI Heart Disease Dataset](https://archive.ics.uci.edu/ml/datasets/heart+Disease)

---

*This project was completed as part of a graduate course at George Washington University.*
