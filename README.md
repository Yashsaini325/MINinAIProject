# MINinAIProject

# AI for Market Trend Analysis: Product Sales Forecasting📌

Project OverviewAccurate sales forecasting is a cornerstone of efficient business operations. This project implements a Supervised Machine Learning approach to predict future product sales by analyzing historical trends and seasonal patterns.By leveraging the Random Forest Regressor, the system identifies complex non-linear relationships within time-series data to help businesses optimize inventory management and reduce waste.


# 🚀 Key FeaturesSynthetic Data Generation:
Simulates three years of realistic daily sales data including linear trends, sinusoidal seasonality, and Gaussian noise.Advanced Feature Engineering:

* Temporal features (Day, Month, Year, Day of Week).Lag Features: Captures sales values from 1, 7, and 30 days prior.Rolling Statistics:
*  Calculates 7-day and 30-day moving averages to smooth noise and highlight trends.Data Visualization: Visualizes sales cycles and compares actual vs. predicted values using Matplotlib.Performance Metrics:
*   Evaluates accuracy using MAE, RMSE, and R² Score.
*   🛠️ Tech StackLanguage: PythonData Manipulation: pandas, numpyMachine Learning: scikit-learnVisualization: matplotlib📋 Methodology1.
*    Data Understanding & PreparationThe dataset consists of daily sales records. We performed a time-series safe split (80% training, 20% testing) to ensure the model does not "leak" future information into the past.2. Feature EngineeringRaw dates were transformed into high-dimensional features:Lags: Lag_1, Lag_7, Lag_30 (Previous performance).Moving Averages: Rolling_7, Rolling_30 (Smoothed trends).Scaling: Applied StandardScaler to normalize features for the regressor.3.
*
*  Model ArchitectureWe utilized the Random Forest Regressor with the following configuration:n_estimators: 300max_depth: 10random_state: 42This ensemble method was chosen for its robustness against outliers and its ability to handle multi-collinearity between lag features.
*
*    📊 ResultsThe model achieved the following performance on the test set:MetricValueMean Absolute Error (MAE)~7.10Root Mean Squared Error (RMSE)~8.94R² Score0.73
*    Interpretation: An R² score of 0.73 indicates that the model explains approximately 73% of the variance in sales data, proving highly effective for a trend-based forecast.

*    
*   # 📂 Project StructurePlaintext
*    ├── Project.ipynb
*    # Main Jupyter Notebook with code and analysis
├── README.md
# Project documentation

# ⚙️ How to RunEnsure you have Python installed.Install dependencies:Bashpip install pandas numpy matplotlib scikit-learn

Open Project.ipynb in Jupyter Notebook or VS Code and run all cells.📈 Future ImprovementsIntegration of external factors like holidays or promotion events.Experimentation with Gradient Boosting models (XGBoost or LightGBM).Deployment via a web interface (Streamlit or Flask) for real-time forecasting.
# Author: Yash Saini 
# Project Category: AI for Market Trend Analysis
