# Medical Insurance Cost Predictor

An interactive web application and machine learning model built with Python, `scikit-learn`, and `Gradio` to predict individual annual medical insurance charges.

---

## 📌 Problem Statement
Medical expenses vary significantly based on personal demographics and health habits. The goal of this project is to build an interpretable machine learning pipeline that accurately estimates annual insurance costs to help users and insurers understand key risk drivers.

---

## 📊 Dataset Description
The model uses the Medical Cost Personal Dataset containing **1,338 policyholder records**:
* **`age`**: Age of the primary beneficiary
* **`sex`**: Gender (`female`, `male`)
* **`bmi`**: Body Mass Index ($kg/m^2$)
* **`children`**: Number of covered dependents
* **`smoker`**: Smoking status (`yes`, `no`)
* **`region`**: Residential location in the US (`northeast`, `southeast`, `southwest`, `northwest`)
* **`charges`** *(Target)*: Total annual medical insurance cost ($)

---

## 🛠️ Data Preprocessing & Modeling
1. **Data Cleaning**: Checked for missing values (dataset was completely clean).
2. **Encoding**: Used One-Hot Encoding (`pd.get_dummies`) to convert text categories (`sex`, `smoker`, `region`) into numerical indicators.
3. **Data Splitting**: Divided data into 80% training set and 20% test set with a fixed seed (`random_state=42`).
4. **Model Selection**: Trained a **Multiple Linear Regression** algorithm using `scikit-learn`.
5. **Deployment**: Built an interactive web interface using `Gradio`.

---

## 📈 Evaluation Results & Insights

* **Mean Absolute Error (MAE)**: ~$4,181.19
* **Mean Squared Error (MSE)**: ~33,596,915.80
* **Root Mean Squared Error (RMSE)**: ~$5,796.28
* **R-squared ($R^2$) Score**: `0.7836` (The model explains **~78.4%** of the variance in charges)

**Key Insight**: Smoking is the single largest factor driving costs higher—especially when paired with a high BMI ($\ge 30$).

---

## ⚠️ Limitations
* **Linearity Assumption**: Multiple Linear Regression assumes linear relationships and may miss complex non-linear health interactions.
* **Geographic Scope**: Dataset regions are limited to general US territories and may not generalize globally.


---

## 🚀 How to Run Locally

1. Clone this repository:
   ```bash
   git clone [https://github.com/your-username/medical-insurance-cost-prediction.git](https://github.com/your-username/medical-insurance-cost-prediction.git)
