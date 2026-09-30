# medical-insurance-cost-prediction
End-to-end Machine Learning pipeline and Gradio web app for insurance cost prediction.

📌 Project OverviewMedical insurance costs depend heavily on personal health factors and lifestyle choices. The goal of this project is to build an interpretable Multiple Linear Regression pipeline that estimates annual charges based on age, BMI, smoking status, dependents, and region.📊 Dataset DetailsThe model is trained on the standard Medical Cost Personal Datasets (1,338 records):age: Age of the beneficiarysex: Gender (female, male)bmi: Body Mass Index ($kg/m^2$)children: Number of covered dependentssmoker: Smoking status (yes, no)region: Residential region in the US (northeast, southeast, southwest, northwest)charges (Target): Total annual medical bills in USD ($)🛠️ Machine Learning WorkflowData Cleaning: Checked for missing values and handled data formatting.Preprocessing: Applied One-Hot Encoding (pd.get_dummies) to convert categorical text features into numerical values.Train/Test Split: Separated data into 80% training set and 20% test set (random_state=42).Model Training: Fitted a Multiple Linear Regression model using scikit-learn.Deployment: Integrated the model into an interactive web UI using Gradio.📈 Results & PerformanceMean Absolute Error (MAE): ~$4,181.19Root Mean Squared Error (RMSE): ~$5,796.28$R^2$ Score: 0.7836 (Explains ~78.4% of the variance)Key Takeaway: Smoking status is the strongest predictor of high medical costs, especially when paired with a high BMI ($\ge 30$).🚀 How to Run LocallyBash# 1. Clone this repository
git clone https://github.com/your-username/medical-insurance-cost-prediction.git

# 2. Install required packages
pip install pandas numpy scikit-learn gradio

# 3. Run the notebook or application
python app.py
⚠️️ Model LimitationsAssumes linear relationships; extreme non-linear risk factors may require tree-based algorithms like Random Forest.Regional indicators are limited to US territories.
