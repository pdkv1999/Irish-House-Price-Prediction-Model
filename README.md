🏠 Dublin House Price Prediction
📌 Project Overview
This project applies predictive analytics and machine learning techniques to forecast housing prices in Dublin using the Ireland House Price.csv dataset. The primary goal is to explore factors that influence property prices and to create models that can assist stakeholders like homebuyers, investors, and developers in making data-driven decisions.

📂 Dataset Information
Rows: 13,320

Features: 12

Key Features:

total_sqft – Property area in square feet

price-per-sqft-$ – Price per square foot

location, property_scope, bathrooms, bedrooms, energy_rating, renovation_status

Target Variable: Property price

🔧 Data Preprocessing & Feature Engineering
Missing Value Imputation: Median for numerical features; averaging for range-based entries

Feature Creation: price_per_bedroom, size

Encoding: One-Hot Encoding for categorical variables

Scaling: StandardScaler for numeric features

Outlier Strategy: No explicit removal; robust tree-based models (Random Forest & Gradient Boosting) handle them inherently

🤖 Models Applied
Model	Purpose	Notes
Linear Regression	Baseline comparison	Poor fit
Support Vector Regressor (SVR)	Non-linear regression	Performed poorly
Random Forest Regressor	Tree-based, handles outliers	Best performer (R² = 0.0518)
Gradient Boosting Regressor	Ensemble boosting model	Best RMSE (0.4322), R² = 0.1493
Lasso Regression	Feature selection via L1 penalty	Applied for dimensionality reduction
Principal Component Analysis (PCA)	Dimensionality reduction	Improved performance in high-dimensional space

🎯 Results Summary
Best Model (Regression): Gradient Boosting Regressor

R²: 0.1493

RMSE: 0.4322

Best Model (Classification): Random Forest

Accuracy: 71.81%

Feature Importance:

total_sqft

location

size (bedrooms)

💡 Future Improvements
Advanced feature engineering

More aggressive outlier handling

Try deep learning models or ensemble stacking

Expand dataset to include macroeconomic or temporal features
