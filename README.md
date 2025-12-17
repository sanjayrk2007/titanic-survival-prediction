
# Titanic Survival Prediction – Logistic Regression Baseline

## 📌 Project Overview
This project focuses on predicting passenger survival on the Titanic using **Logistic Regression**.  
The objective is to build a **clear and interpretable baseline model** using sound feature engineering practices, rather than leaderboard optimization.

This notebook serves as a **reference baseline** before moving on to more advanced models such as Random Forests and Gradient Boosting.

---

## 📂 Dataset
- Source: Kaggle – *Titanic: Machine Learning from Disaster*
- Files used:
  - `train.csv`
  - `test.csv`

### Target Variable
- `Survived`  
  - `0` → Did not survive  
  - `1` → Survived

---

## 🔍 Approach

### 1️⃣ Exploratory Data Analysis (EDA)
- Identified missing values in `Age`, `Fare`, and `Embarked`
- Observed strong survival dependency on:
  - Gender
  - Passenger class
  - Family structure
  - Passenger titles

---

### 2️⃣ Feature Engineering

The following features were engineered to improve predictive performance:

#### 🔹 Title Extraction
- Extracted passenger titles from the `Name` column
- Grouped rare titles into a single `Rare` category
- Normalized equivalent titles (e.g., *Mlle → Miss*)
- Encoded titles numerically

#### 🔹 Age Imputation
- Missing ages filled using **median age per title group**
- Preserves demographic and social structure

#### 🔹 Family-Based Features
- `FamilySize = SibSp + Parch + 1`
- `IsAlone` created to identify solo travelers

#### 🔹 Categorical Encoding
- `Sex` encoded as binary (`male = 0`, `female = 1`)
- `Embarked` encoded numerically

---

### 3️⃣ Feature Set Used
