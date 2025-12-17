# Titanic Survival Prediction – End-to-End Machine Learning Project

## 📌 Project Overview
This project predicts passenger survival on the Titanic using classical machine learning techniques.  
The primary objective is to **learn and apply ML concepts correctly**, starting from a strong baseline and gradually moving to more advanced models.

Rather than leaderboard chasing, this project emphasizes:
- Proper data understanding
- Logical feature engineering
- Model comparison
- Knowing when to stop optimizing

---

## 📂 Dataset
- Source: Kaggle – *Titanic: Machine Learning from Disaster*
- Files used:
  - `train.csv`
  - `test.csv`

**Target Variable**
- `Survived`
  - `0` → Did not survive
  - `1` → Survived

---

## 🧭 Project Workflow

1. Data exploration and understanding  
2. Feature engineering and preprocessing  
3. Baseline model (Logistic Regression)  
4. Performance evaluation and stopping criteria  
5. Extension to tree-based models  

---

## 🔍 Exploratory Data Analysis (EDA)
Key observations from EDA:
- Missing values present in `Age`, `Fare`, and `Embarked`
- Survival strongly correlated with:
  - Gender
  - Passenger class
  - Family structure
  - Social titles (extracted from names)

EDA guided feature engineering decisions instead of applying blind transformations.

---

## 🧪 Feature Engineering

### 🔹 Title Extraction
- Extracted titles from the `Name` column
- Rare titles grouped into a single `Rare` category
- Titles mapped to numerical values

### 🔹 Age Imputation
- Missing `Age` values filled using **median age grouped by title**
- Preserves demographic and social patterns

### 🔹 Family-Based Features
- `FamilySize = SibSp + Parch + 1`
- `IsAlone` feature created to capture solo travelers

### 🔹 Categorical Encoding
- `Sex`: binary encoding
- `Embarked`: numerical encoding

---

## 📊 Final Feature Set
```text
Pclass
Sex
Age
Fare
Embarked
Title
IsAlone


