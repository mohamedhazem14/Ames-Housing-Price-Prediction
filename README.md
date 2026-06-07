# 🏠 Ames Housing Price Prediction

## 📌 Project Overview

This project aims to predict house sale prices using the Ames Housing dataset and advanced machine learning techniques.

The workflow includes data preprocessing, feature engineering, model comparison, ensemble learning, and model persistence for deployment.

The objective is to build a robust regression model capable of accurately estimating housing prices based on property characteristics and neighborhood-related features.

---

## 📊 Dataset Description

The Ames Housing dataset contains detailed information about residential properties, including:

- Property size and living area
- Basement features
- Garage information
- Construction and remodeling years
- Number of rooms and bathrooms
- Porch and outdoor space features
- Neighborhood characteristics

### Target Variable

- **SalePrice** (log-transformed for improved model performance)

---

## ⚙️ Workflow

### 1. Data Cleaning

- Removed unnecessary columns (e.g., ID)
- Handled missing values using median and most frequent imputation

### 2. Exploratory Data Analysis (EDA)

- Sale price distribution analysis
- Correlation analysis
- Feature relationship visualization
- Heatmap of top correlated features

### 3. Feature Engineering

Created several domain-driven features:

- TotalSF
- TotalBath
- HouseAge
- RemodAge
- HasGarage
- HasFireplace
- TotalPorchSF
- LivAreaPerRoom

### 4. Data Preprocessing

- Missing value treatment
- One-Hot Encoding using Pandas
- Feature alignment between train and test sets
- Feature scaling using RobustScaler

### 5. Model Training

Data was split into:

- 80% Training Data
- 20% Testing Data

---

## 🤖 Models Used

- Ridge Regression
- Lasso Regression
- Elastic Net Regression
- Random Forest Regressor
- Gradient Boosting Regressor

### Ensemble Learning

A Stacking Regressor was implemented using:

- Random Forest Regressor
- Gradient Boosting Regressor

with:

- Ridge Regression as the final estimator

---

## 📈 Evaluation Metrics

Models were evaluated using:

- R² Score
- RMSE (Root Mean Squared Error)
- MAE (Mean Absolute Error)

---

## 🏆 Results

### Best Model

**Stacking Regressor**

The ensemble stacking approach achieved the strongest predictive performance by combining multiple machine learning models and leveraging Ridge Regression as the meta-learner.

---

## 📊 Visualizations

The project includes:

- Sale Price Distribution
- Correlation Heatmap
- Model Performance Comparison
- Actual vs Predicted Prices
- Error Distribution Analysis

---

## 💾 Model Saving

The final trained model was saved using Joblib:

```python
joblib.dump(stack, "ames_model.pkl")
```

This allows the model to be reused for future predictions and deployment.

---

## 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib

---

## 👤 Author

**Mohamed Hazem**

AI Engineer | Machine Learning Enthusiast
