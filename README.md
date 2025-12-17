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

## 🤖 Model 1: Logistic Regression (Baseline)
Why Logistic Regression?

Simple and interpretable

Strong baseline for binary classification

Helps validate feature engineering quality

Training Details

Minimal hyperparameter tuning

No ensembling or leakage tricks

Focused on clean implementation

📈 Performance

Kaggle Public Score: 0.77990

This score is close to the practical performance ceiling for Logistic Regression on this dataset.

🛑 Why Optimization Was Stopped

Further improvements using Logistic Regression resulted in diminishing returns.

At this stage:

Small gains required heavy feature hacks

Improvements no longer reflected learning value

The model was frozen to preserve a clean and honest baseline.

🧠 Key Learnings

Feature engineering often matters more than model choice

Logistic Regression quickly saturates on non-linear problems

Understanding why a model works is more valuable than squeezing extra accuracy

Knowing when to stop is an important ML skill

🚀 Next Steps (Planned Extensions)
🔹 Model 2: Random Forest

Capture non-linear relationships automatically

Reduce need for manual feature transformations

Analyze feature importance

🔹 Model 3: Gradient Boosting

XGBoost / LightGBM

Performance comparison with Random Forest

Bias–variance tradeoff analysis

The same feature set will be reused initially to ensure fair comparison.

📁 Project Structure
├── data/
│   ├── train.csv
│   └── test.csv
├── notebooks/
│   └── titanic_logistic_regression.ipynb
├── README.md

📌 Notes

This project prioritizes learning ML fundamentals correctly

Avoids leaderboard-specific tricks and data leakage

Designed to be interview-ready and extensible

👤 Author

Second-year B.Tech CSE student
Focused on Machine Learning fundamentals and long-term skill building


---

### ✅ This README is:
- Resume-safe  
- Interview-safe  
- Future-proof (you can extend without rewriting)  
- Honest about learning intent  

If you want next, I can:
- Add a **Random Forest section + results**
- Turn this into a **GitHub-ready project description**
- Help you write a **resume bullet using this project**

Just say the word.


