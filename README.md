# 🏦 E-Payment Growth Forecasting by Sector and Card Type in Bahrain

## 📄 Project Description

This project forecasts sector-level e-payment transaction growth across different card types (Credit and Debit) in Bahrain using advanced multi-class classification machine learning models. The work extends my June 2024 dissertation by adding recent data and advanced model tuning, providing actionable insights for financial institutions, policymakers, and businesses operating in the region.

---

## ❓ Problem Statement

The goal is to predict the number of e-payment transactions for 2025 by sector and card type, based on historical data from 2022–2024. Given the multi-class nature of the sectors and card types, and the imbalanced distribution of transactions across sectors, a robust and interpretable machine learning solution was needed.

---

## 📊 Dataset Description and Source

- **Source**: Real transaction data collected from Bahrain’s financial sector.
- **Features**:
  - `Sector`: Economic sector where the transaction occurred.
  - `Cards_type`: Type of payment card (Credit or Debit).
  - `No. of trans.`: Number of transactions.
  - `Value`: Value of transactions.
  - `CPI_Bahraini` and `CPI_Non_Bahraini`: Consumer price indices.
- **Target**: Predicted transaction volumes by sector and card type for 2025.

---

## ⚙️ Methodology Overview

1. **Data Preparation**: Cleaned missing values, handled imbalanced classes using SMOTE and Random Under Sampling.
2. **Feature Engineering**: Included card type, CPI indicators, and transaction metrics.
3. **Modeling**: Trained and evaluated multiple models, including:
   - Logistic Regression
   - Decision Tree
   - Random Forest
   - Bagging
   - Gradient Boosting
   - AdaBoost
   - XGBoost
4. **Hyperparameter Tuning**: Conducted GridSearchCV and RandomizedSearchCV on top models.
5. **Final Model**: Selected Random Forest (oversampled) as the best performer with 0.906 validation accuracy and an acceptable train-validation gap.

---

## 📈 Key Findings and Insights

- Education, Supermarket, and Miscellaneous Goods & Services sectors showed significant predicted growth in Credit transactions.
- Several sectors, including Department Stores and Jewelry, are expected to see declines.
- Credit transactions are projected to grow faster than Debit in high-growth sectors.
- Random Forest (oversampled) achieved the best performance for multi-class classification in this imbalanced dataset.

---

## 🛠️ Installation/Setup Instructions

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/epayment-forecasting-bahrain.git
   cd epayment-forecasting-bahrain

pip install -r requirements.txt

python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

from model_pipeline import train_and_forecast
train_and_forecast(df_train, df_test)
