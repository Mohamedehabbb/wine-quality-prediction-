# wine-quality-prediction-
End-to-End project
# 🍷 Wine Quality Prediction – Comprehensive Project README

## Project Problem Statement

Wine quality assessment is a **subjective and expensive process**, typically performed by human experts. The main challenge is to develop a **data-driven, reliable, and high-accuracy model** to predict wine quality using only physicochemical properties from laboratory tests.

### Problems We Addressed

1. **Data Imbalance**: Most wines are medium quality (5-7), with very few poor or excellent samples.
2. **Feature Relevance**: Not all physicochemical features are equally informative.
3. **Non-linear Relationships**: Some features have complex relationships with quality.
4. **Regression vs Classification**: Need to predict exact quality score and categorize wines.

---

## Step-by-Step Approach

### 1️⃣ Data Loading & Inspection

* Loaded the Vinho Verde dataset (white wine samples) using `pandas`.
* Checked for missing values, duplicates, and data types.
* Outcome: Dataset is clean with no missing values and all numeric features.

### 2️⃣ Exploratory Data Analysis (EDA)

* Plotted target distribution → Most wines are medium quality.
* Correlation heatmap → Identified that `alcohol` positively and `volatile_acidity` negatively affect quality.
* Feature vs target plots → Validated feature relationships and potential predictors.

### 3️⃣ Data Cleaning

* Checked for duplicates → None found.
* Confirmed all features are numeric and consistent.

### 4️⃣ Feature Engineering

* Created `quality_label` (Low/Medium/High) for classification tasks.
* Outcome: Enabled both regression and classification modeling.

### 5️⃣ Train-Test Split & Scaling

* Split data into training and testing sets (80/20).
* Scaled features using `StandardScaler` for linear models.
* Outcome: Data ready for modeling.

### 6️⃣ Regression Modeling

* **Linear Regression (Baseline)** → Established a baseline R² score.
* **Random Forest Regressor** → Improved performance with non-linear modeling.
* **Optimized Random Forest** using `GridSearchCV` → Tuned hyperparameters for better accuracy.
* **XGBoost & LightGBM Regressors** → Achieved highest R² score, demonstrating gradient boosting effectiveness.

### 7️⃣ Regression Evaluation & Insights

* RMSE and R² metrics calculated for each model.
* LightGBM is the most accurate, capturing complex patterns.
* Feature importance shows `alcohol`, `volatile_acidity`, and `sulphates` as top predictors.
* Actual vs Predicted plot shows tight alignment with LightGBM predictions.

### 8️⃣ Classification Modeling

* **Logistic Regression (Baseline)** → Provided initial classification performance.
* **Random Forest Classifier** with class balancing → Improved F1 Macro score for minority classes.
* Evaluated using precision, recall, F1 Macro → Random Forest significantly outperformed baseline.

### 9️⃣ Ultimate Visualization

* Created a 4-panel figure showing:

  1. Regression R² for all models
  2. Classification F1 Macro for models
  3. LightGBM feature importance
  4. Actual vs Predicted plot for LightGBM
* Outcome: Visual summary of model performance and feature impact.

### 🔟 Key Insights & Takeaways

* **Alcohol** is the strongest predictor of quality.
* Non-linear models (Random Forest, XGBoost, LightGBM) outperform linear models.
* Gradient boosting (LightGBM) provides the highest accuracy.
* Classification with balanced classes improves minority quality detection.
* Data-driven models can replace or assist expert wine tasters effectively.

### 1️⃣1️⃣ Future Work

* Apply SHAP explainability for deeper interpretation.
* Explore ordinal regression for finer-grained classification.
* Implement cross-validation for robust performance.
* Deploy model via API for real-time predictions.

---

## Tools & Libraries

* **Python Libraries:** pandas, numpy, matplotlib, seaborn
* **Scikit-learn:** LinearRegression, RandomForestRegressor/Classifier, LogisticRegression, StandardScaler, GridSearchCV
* **Gradient Boosting:** XGBoost, LightGBM

---

## Conclusion
This project demonstrates a full, professional data science workflow addressing the challenge of predicting wine quality. By combining EDA, feature engineering, regression, classification, and advanced gradient boosting models, we achieved maximum accuracy and extracted meaningful insights for decision-making. The approach is suitable for Kaggle notebooks, portfolio projects, and interview showcases.

This project demonstrates a **full, professional data science workflow** addressing the challenge of predicting wine quality. By combining EDA, feature engineering, regression, classification, and advanced gradient boosting models, we achieved **maximum accuracy** and extracted meaningful insights for decision-making. The approach is suitable for Kaggle notebooks, portfolio projects, and interview showcases.
