# 🌧️ Rainfall Prediction – Australia Weather Dataset

A machine learning project that predicts whether it will rain today in the Melbourne, Australia area, using historical weather observations and a complete Scikit-learn preprocessing and classification pipeline.

---

## 📌 Project Overview

Using real weather data from the Australian Government's Bureau of Meteorology, this project builds a predictive model to determine whether it will rain today, based on historical weather observations available up to and including the previous day. The project focuses on the Melbourne area (Melbourne, Melbourne Airport, and Watsonia) to build a localized, more accurate model.

---

## 🏗️ Approach & Methodology

1. **Data Cleaning**
   - Removed rows with missing values.
   - Renamed columns to reflect a same-day prediction target (`RainToday`) instead of a next-day target, avoiding data leakage.

2. **Feature Engineering**
   - Restricted the dataset to three closely located regions (Melbourne, Melbourne Airport, Watsonia) for a more localized, consistent model.
   - Extracted a **Season** feature from the `Date` column to capture seasonal weather patterns.

3. **Preprocessing Pipeline**
   - Numerical features scaled using `StandardScaler`.
   - Categorical features encoded using `OneHotEncoder`.
   - Combined into a single `ColumnTransformer`.

4. **Model Building**
   - Built a `Pipeline` combining preprocessing with a `RandomForestClassifier`.
   - Tuned hyperparameters using `GridSearchCV` with stratified k-fold cross-validation.

5. **Model Evaluation**
   - Evaluated using classification report, confusion matrix, and test accuracy.
   - Extracted and visualized feature importances to identify the strongest predictors of rainfall.

6. **Model Comparison**
   - Built a second model using `LogisticRegression` with its own hyperparameter grid.
   - Compared accuracy and confusion matrix results between Random Forest and Logistic Regression.

---

## 🧰 Tech Stack

- **Language:** Python
- **Data Handling:** Pandas, NumPy
- **Machine Learning:** Scikit-learn (Pipeline, ColumnTransformer, GridSearchCV, RandomForestClassifier, LogisticRegression)
- **Visualization:** Matplotlib, Seaborn
- **Environment:** Jupyter Notebook

---

## 📊 Workflow

1. **Data Loading & Cleaning** — Load the dataset, drop missing values, and address data leakage.
2. **Feature Engineering** — Filter by location, extract seasonality from dates.
3. **Train/Test Split** — Stratified split to preserve class balance.
4. **Preprocessing Pipeline** — Scaling for numeric features, one-hot encoding for categorical features.
5. **Model Training & Tuning** — Random Forest classifier tuned via GridSearchCV with cross-validation.
6. **Evaluation** — Classification report, confusion matrix, and feature importance analysis.
7. **Model Comparison** — Logistic Regression trained and compared against Random Forest results.

---

## 📈 Results

- The Random Forest model achieved strong test accuracy in predicting same-day rainfall for the Melbourne area.
- Feature importance analysis identified the weather variables most predictive of rainfall.
- A Logistic Regression model was trained as a comparison, with accuracy and confusion matrix results evaluated side-by-side against the Random Forest model.

---

## 🚀 How to Run

1. Clone this repository.
2. Open `FinalProject_AUSWeather.ipynb` in Jupyter Notebook or Google Colab.
3. Install the required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
   ```
4. Run all cells in order (**Kernel → Restart & Run All**).
5. View outputs including class distributions, classification reports, confusion matrices, and the feature importance chart.

---

## 🎓 Acknowledgment

This project was completed as part of the **IBM AI Engineering Professional Certificate** on Coursera, developed by IBM Skills Network.

---

## 👩‍💻 Author

**Umaira Tahir**
