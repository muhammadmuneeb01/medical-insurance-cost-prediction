# Medical Insurance Cost Predictor

A simple Machine Learning project that predicts annual medical insurance charges based on personal health and demographic details. 

This project uses **Multiple Linear Regression** to make predictions and includes an interactive web app built with **Gradio**.

---

## 📌 Project Overview
Medical expenses vary a lot from person to person. The goal of this project is to build a model that estimates how much a person will pay for health insurance based on factors like age, BMI, and smoking habits.

---

## 📊 Dataset Info
The dataset has **1,338 rows** with the following details:
* **`age`**: Age of the person
* **`sex`**: Gender (`female` or `male`)
* **`bmi`**: Body Mass Index (measures body fat based on height and weight)
* **`children`**: Number of dependents/children
* **`smoker`**: Whether the person smokes (`yes` or `no`)
* **`region`**: Location in the US (`northeast`, `southeast`, `southwest`, `northwest`)
* **`charges`**: Annual medical cost in USD ($) — *This is what we predict!*

---

## 🛠️ How It Was Built
1. **Data Cleaning**: Checked for missing values (there were none).
2. **Encoding**: Converted text columns into numbers using One-Hot Encoding (`pd.get_dummies`).
3. **Train-Test Split**: Split data into 80% for training and 20% for testing.
4. **Model Training**: Trained a Linear Regression model using `scikit-learn`.
5. **App Creation**: Built a simple web interface using `Gradio` so users can test predictions live.

---

## 📈 Model Performance
* **Mean Absolute Error (MAE)**: ~$4,181
* **Root Mean Squared Error (RMSE)**: ~$5,796
* **R² Score**: `0.7836` (The model accurately explains about **78%** of the cost differences)

**Key Insight:** Smoking is the biggest factor that increases insurance costs, especially when combined with a high BMI!

---

## 🚀 How to Run the Project
1. Clone this repository:
   ```bash
   git clone [https://github.com/your-username/medical-insurance-cost-prediction.git](https://github.com/your-username/medical-insurance-cost-prediction.git)
