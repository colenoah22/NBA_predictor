# 🏀 NBA 2K Player Rating Prediction

## Overview
This project builds a **linear regression model** to predict **NBA 2K player ratings** based on player attributes such as physical stats, salary, draft data, and team information.  
The goal is to identify which factors most strongly influence player ratings and evaluate how well a regression model can capture these relationships.  

**Dataset credit:** [Kostiantyn Isaienkov on Kaggle](https://www.kaggle.com/datasets/isaienkov/nba2k20-player-dataset)

---

## Methods / Modeling Approach
- **Data Cleaning & Preprocessing**
  - Converted height and weight into consistent numerical formats (cm and lbs).
  - Removed special characters (like `$`) and converted salary data to numeric values.
  - Handled missing values by filling numerical columns with median values and categorical ones with mode.
- **Feature Engineering**
  - Encoded categorical variables (team, position, country, draft info, etc.).
- **Modeling**
  - Trained a **Linear Regression model** using a **70/30 train-test split**.
  - Evaluated performance using **R² score** and other regression diagnostics.
- **Tools Used**
  - `pandas`, `numpy`, `scikit-learn`, `statsmodels`

---

## Results
- The final model provided a **solid baseline** for predicting player ratings, achieving a reasonably high **R² score** on the test set.  
- Features like **salary**, **draft position**, and **height/weight** showed strong relationships with overall ratings.  
- Further improvements could be made by using **nonlinear models** (like Random Forest or XGBoost) to capture deeper patterns.

---

## Compiling
1. Clone or download the repository.  
2. Make sure the dataset file (`nba2k-full.csv`) is in the same directory as the notebook.  
3. Install dependencies:
   ```bash
   pip install pandas numpy scikit-learn statsmodels
