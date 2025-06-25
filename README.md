# 🧠 ML-Project-Premium-Predictions

An intelligent machine learning system to predict health insurance premiums based on user profile, medical history, and risk indicators. The project demonstrates full-stack data science skills including EDA, feature engineering, model training, evaluation, and deployment using Streamlit.

---

## 🚀 Overview

This ML application predicts the annual insurance premium cost for individuals based on features such as age, income, BMI, genetic risk, diseases, employment, and lifestyle choices. The model has been enhanced by segmenting predictions for young individuals and including a custom-calculated risk score.

---

## 📊 Dataset Details

- **Size**: 50,000 rows × 13 columns
- **Target Variable**: Annual Premium Amount

---

## 🧪 Machine Learning Algorithms Used

- Linear Regression
- Ridge Regression
- Lasso Regression
- XGBoost Regressor
- **Model Selection**: GridSearchCV was used to pick the best-performing model.
- **Separate Models**: Trained separate models for:
  - Users aged ≤ 25 (`model_young`)
  - Users aged > 25 (`model_rest`)
- **Scaling**: Separate scalers were trained and exported for both groups.

---

## 🔧 Project Workflow

### ✅ Step-by-step Process:

1. **Data Loading & Exploration**
   - Handled missing values
   - Removed duplicates
   - Performed univariate and bivariate analysis

2. **Feature Engineering**
   - Calculated **Total Risk Score** by mapping medical conditions to numeric risk values.
   - Normalized the total risk to enhance model sensitivity.
   - Conducted **VIF (Variance Inflation Factor)** analysis to check for multicollinearity.
   - Scaled numerical features for better model performance.

3. **Model Training & Selection**
   - Trained multiple ML models (Linear, Ridge, Lasso, XGBoost)
   - Used **GridSearchCV** for hyperparameter tuning
   - Selected best model for each age segment

4. **Error Analysis**
   - Measured overall accuracy
   - Evaluated **error percentage**
   - Visualized histograms to analyze prediction errors
   - Discovered that **age ≤ 25** group caused 99% of major errors

5. **Model Segmentation**
   - Split model training into two: Young (≤25) and Rest
   - Results remained similar until an additional feature was introduced

6. **Feature Addition**
   - Added **Genetic Risk** as a new input feature
   - Reduced error from **77% to 2%**

7. **Model Export**
   - Exported final models (`joblib`)
   - Exported group-specific scalers

8. **Deployment**
   - Built interactive Streamlit app (see below)

---

## 🌐 Deployment

- **Frontend**: Built with [Streamlit](https://streamlit.io/)
- **Backend**: Two separate models and scalers depending on age group
- Hosted on **Streamlit Cloud**

## link for streamlit app
[🔗 Click here to view the Streamlit App](https://vamshi-ml-project-premium-prediction.streamlit.app/)




