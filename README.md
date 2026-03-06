🛢️ Oil & Gas Production Prediction – SPE DATHON Project

📌 Project Overview
This project focuses on predicting oil, gas, and water production from well operational and reservoir-related parameters using machine learning. The notebook was developed as part of an SPE DATHON challenge, where the objective is to analyze wellbore conditions and production data to build accurate predictive models.

The project follows a full end-to-end data science workflow; exploratory data analysis, visualization, preprocessing, encoding, feature engineering, model training, evaluation, optimization, and deployment preparation.

🎯 Project Objectives

Understand well production behavior using pressure, temperature, and choke data
Predict Oil, Gas, and Water production rates
Compare multiple regression models
Improve model performance through scaling, feature selection, and hyperparameter tuning
Select the best-performing model for deployment

📂 1. Exploratory Data Analysis (EDA)

Pressure and Choke Analysis
Downhole pressure values range mainly between 200–300 PSI
Choke sizes are generally small, indicating controlled production settings
Smaller choke sizes are more frequently used

✔️ Interpretation
This suggests that production is carefully regulated to prevent formation damage and optimize recovery.

📊 2. Bivariate Visualization
Several bivariate plots are created to analyze relationships between variables:

Examples:
Choke Size vs Year
Downhole Pressure vs Year
Downhole Temperature vs Year

✔️ Observations
Changes in choke size across years reflect reservoir characteristics
Pressure variations indicate differences in deposit extent and exploitation methods
Temperature changes reflect mineral composition and operational conditions

📈 3. Trivariate Visualization
Trivariate plots explore deeper relationships:

Downhole Pressure vs Temperature vs Production
Pressure–Temperature interaction effects

✔️ Interpretation

Production behavior depends strongly on combined pressure and temperature conditions
Different deposits and exploitation methods influence these relationships

📆 4. Monthly Pressure Trends

Downhole pressure is analyzed for each month across years
Most wells show consistently high pressures
A few wells exhibit noticeable pressure decline

✔️ Insight
Stable pressure suggests sustained reservoir energy, while declining wells may require intervention.

🧠 5. EDA Conclusion

Most wells operate within safe pressure ranges
Wells in 2015 showed higher temperatures than those in 2016
Pressure and temperature are strong indicators of production performance
🔢 6. One-Hot Encoding

Categorical variables are transformed into numerical format using one-hot encoding.

✔️ Result

All categorical features become ML-compatible
No loss of information due to encoding

🧪 7. Train/Test Split
Dataset is divided into training and testing sets
Ensures unbiased evaluation of model performance

📉 8. Pairplot Analysis (Train Set)
Key variables visualized include:

Water Production (stb/day)
Liquid Ratio
Total Production

✔️ Observation
Clear linear and non-linear relationships exist between features and production targets.

🤖 9. Model Training
Multiple regression models are trained and evaluated:

Models Used:
Decision Tree
Random Forest
XGBoost
Gradient Boosting
CatBoost
AdaBoost
LightGBM
ExtraTrees Regressor

✔️ Evaluation Metrics:
R²
RMSE
MAE
Adjusted R²

🏆 10. Initial Model Results
Tree-based and boosting models perform significantly better
CatBoost and Gradient Boosting show strong performance
Errors reduce substantially compared to baseline models

⚖️ 11. Feature Scaling
Standard Scaler
Standardizes feature values
Slight improvement observed

✔️ Conclusion
Scaling alone improves consistency but does not guarantee optimal performance.

🔁 12. Cross-Validation
Cross-validation is applied to:

Reduce overfitting
Improve model generalization
Ensure stability across folds

🧬 13. Recursive Feature Elimination (RFE)
RFE is applied to:

Identify most important features
Remove redundant variables
Improve model simplicity

⚙️ 14. Hyperparameter Tuning
Hyperparameter optimization is performed using:

GridSearch
Cross-validation

✔️ Result
ExtraTreesRegressor emerges as the best model
Lowest MAE, MSE, RMSE
Highest R² score

🔍 15. GridSearch on Other Models
Additional tuning confirms:

ExtraTrees consistently outperforms other models
Boosting models remain competitive but slightly less accurate

🧪 16. Holdout Test
The best model is evaluated on unseen data:

Holdout Test → Strong performance confirmed

✔️ Result
The model generalizes well beyond training data.

🎯 17. Individual Target Evaluation
Models are evaluated separately for:

Water Production
Gas Production
Oil Production

✔️ Insight
Each target responds differently to input features, but ExtraTrees performs best across all.

💾 18. Saving the Model
The final trained model is saved for deployment and future inference.

🏁 Final Conclusion
Pressure and temperature are dominant production drivers
Ensemble models outperform linear models
ExtraTreesRegressor is the best-performing algorithm
Cross-validation and feature selection significantly improve accuracy
The model is suitable for real-world oil & gas production forecasting

🛠 Technologies Used
Python
Pandas, NumPy
Matplotlib, Seaborn
Scikit-learn
XGBoost, CatBoost, LightGBM
Jupyter Notebook

🚀 Future Improvements
Incorporate time-series forecasting
Add real-time sensor data
Deploy model via API
Integrate uncertainty quantification
