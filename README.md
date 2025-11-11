🧠 Fitness Data – Machine Learning Regression Project

This project explores a synthetic fitness dataset using supervised Machine Learning regression models.
The goal is to analyze relationships between physiological and lifestyle factors and predict key fitness indicators.

🎯 Objectives

The project aims to answer the following questions:

Predict VO2max – a measure of aerobic endurance based on age, sex, weight, training habits, sleep, and other factors.
→ Useful for evaluating physical fitness without performing an actual test.

Predict body fat percentage (body_fat_pct) – based on anthropometric and lifestyle data.
→ Helps to understand which habits most strongly influence body fat levels.

Predict 5 km running time (run_5k_min) – using fitness and training data.
→ Goal: to build a model that forecasts sports performance.

⚙️ Models Used

For each regression task, three different models were trained and compared:

Linear Regression – baseline interpretable model.

Random Forest Regressor – non-linear model that performs well with mixed feature types.

XGBoost Regressor – powerful boosting model often achieving the best overall performance.

Model performance was evaluated using RMSE and MAE metrics, along with cross-validation for robustness.

🧩 Workflow

Data generation (synthetic dataset).

Exploratory data analysis (EDA) and feature understanding.

Preprocessing with pipelines (imputation, scaling, one-hot encoding).

Model training and hyperparameter tuning (GridSearchCV / RandomizedSearchCV).

Evaluation and comparison of results.

Visualization of predictions and feature importance.

📊 Results

Different models performed best for different target variables:

Simpler models (Linear Regression) generalized better in some cases.

Tree-based models (Random Forest, XGBoost) achieved lower RMSE but showed signs of overfitting on training data.

All models were visualized and compared using saved figures in the /out/ directory.

📁 Project Structure
├── data/               # Synthetic dataset  
├── notebooks/          # Main Jupyter notebooks  
├── out/                # Saved plots and model outputs  
├── models/             # Trained model files (.pkl)  
└── README.md

🧠 Notes

The dataset is synthetic, created for educational and demonstration purposes.

No deployment stage is included (optional in assignment).
