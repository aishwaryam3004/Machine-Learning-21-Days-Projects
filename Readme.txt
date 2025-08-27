# Day 1: Titanic Survival Prediction

## Objective
Predict whether a passenger survived the Titanic disaster using machine learning.  
This challenge focuses on **data preprocessing, exploratory data analysis, feature engineering, and Logistic Regression**.

---

## Dataset
- Source: [Kaggle Titanic Dataset](https://www.kaggle.com/c/titanic/data)
- Files used:
  - `train.csv` : Training data with labels (`Survived`)
  - `test.csv`  : Test data without labels

---

## Steps Taken

### 1. Data Preprocessing
- Removed unnecessary columns: `PassengerId`, `Name`, `Ticket`, `Cabin`
- Handled missing values:
  - `Age` → filled with median
  - `Embarked` → filled with mode
  - `Fare` (in test set) → filled with median
- Encoded categorical variables:
  - `Sex` → Male = 1, Female = 0
  - `Embarked` → One-hot encoding
- Converted datatypes where necessary

### 2. Exploratory Data Analysis (EDA)
- Visualized distributions of `Age`, `Fare`, `Pclass`, `Sex`
- Checked survival count by gender, passenger class, and age groups
- Plotted correlation heatmap of numerical features

### 3. Model Training
- Split training data into train/validation sets (80/20)
- Used **Logistic Regression** to predict survival
- Evaluated with:
  - Accuracy
  - Confusion matrix
  - Classification report

### 4. Prediction on Test Data
- Dropped `PassengerId` before prediction
- Predicted `Survived` for test set
- Created submission CSV with `PassengerId` and `Survived`

---

## Results
-  validation accuracy: `~81%` 
- **Classification Report:**
            precision    recall  f1-score   support

  0 (Died)       0.83      0.86      0.84       105
  1 (Survived)   0.79      0.74      0.76        74
---

## How to Run
1. Open `Titanic.ipynb` in Google Colab or Jupyter Notebook
2. Place `train.csv` and `test.csv` in the `data/` folder
3. Run all cells from preprocessing → model training → prediction
4. Download `titanic_submission.csv` for Kaggle submission

---

## Notes
- This challenge helped to learn **data preprocessing, encoding categorical features, handling missing values, visualization, and training a simple ML model**


