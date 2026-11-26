# Ames Housing Price Prediction 🏠

## Project Overview

This project focuses on predicting residential house prices using Machine Learning regression techniques.

The project uses the Ames Housing Dataset, which contains information about residential properties, including their size, quality, location, condition, and other characteristics.

The main objective is to explore the dataset, identify important factors affecting house prices, perform data preprocessing and feature engineering, and build regression models to predict house sale prices.

## Dataset

The dataset contains information about residential properties in Ames, Iowa.

- Training data: `train.csv`
- Testing data: `test.csv`
- Target variable: `SalePrice`

## Technologies & Libraries

- Python
- Pandas & NumPy
- Matplotlib & Seaborn
- Scikit-learn
- Jupyter Notebook

## Project Workflow

### 1. Exploratory Data Analysis (EDA)

- Understanding numerical and categorical features.
- Analyzing feature distributions.
- Identifying missing values and outliers.
- Studying correlations between independent variables.
- Exploring relationships between features and SalePrice.

### 2. Data Preprocessing

- Handling missing values using appropriate imputation techniques.
- Removing redundant and highly correlated features.
- Identifying and handling outliers.
- Removing low-information features.
- Encoding categorical and ordinal variables.
- Applying numerical scaling using RobustScaler.

### 3. Feature Engineering

Created additional features to improve predictive performance:

- TotalLot
- TotalBsmtFin
- TotalSF
- TotalBath
- TotalPorch

Also created binary features to represent the presence or absence of specific house characteristics.

### 4. Target Transformation

Applied logarithmic transformation to SalePrice to reduce positive skewness and improve the target distribution.

### 5. Model Building

Implemented and evaluated the following regression algorithms:

- Gradient Boosting Regressor
- Random Forest Regressor

Used cross-validation and hyperparameter search techniques during model development.

## Model Evaluation

The Gradient Boosting model achieved the following validation results:

| Metric | Score |
|---|---:|
| R² Score | 0.917 |
| 5-Fold Cross-Validation R² | 0.904 |
| MAE (Log Scale) | 0.079 |
| RMSE (Log Scale) | 0.110 |

Gradient Boosting performed better than Random Forest on the reported validation results.

## Key Learnings

- Performing effective Exploratory Data Analysis.
- Understanding the impact of missing values and outliers.
- Feature selection and feature engineering.
- Handling categorical and numerical data.
- Understanding data leakage and proper preprocessing practices.
- Training and evaluating regression models.
- Comparing Machine Learning model performance.

## Project Structure

```text
ames-housing-price-prediction/
│
├── data/
│   └── README.md
│
├── notebooks/
│   └── ames_housing_price_prediction.ipynb
│
├── requirements.txt
└── README.md
```

## How to Run

1. Clone this repository:

```bash
git clone https://github.com/YOUR_USERNAME/ames-housing-price-prediction.git
```

2. Navigate to the project directory:

```bash
cd ames-housing-price-prediction
```

3. Install the required libraries:

```bash
pip install -r requirements.txt
```

4. Download the dataset and place `train.csv` and `test.csv` in the appropriate data directory.

5. Open the Jupyter Notebook:

```bash
jupyter notebook
```

6. Run the notebook cells.

## Future Improvements

- Build a more robust preprocessing pipeline using Scikit-learn Pipelines.
- Perform more systematic hyperparameter optimization.
- Experiment with additional regression algorithms.
- Improve model evaluation and generalization.
- Develop a simple web application for house price prediction.

---

**Author:** Mohamed Hazem

**GitHub:** https://github.com/mohamedhazem14

**LinkedIn:** https://www.linkedin.com/in/mohamed-hazem-74001a2b6/
