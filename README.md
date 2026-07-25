
# 🏠 House Price Prediction using Machine Learning

## 📌 Project Overview

This project focuses on predicting house prices using Machine Learning techniques based on the **Ames Housing Dataset**.

The main goal is to analyze different factors affecting house prices, perform Exploratory Data Analysis (EDA), preprocess the data, and build a regression model capable of accurately predicting the final sale price.

---

# 📊 Dataset Information

**Dataset:** Ames Housing Dataset

| Feature | Value |
|---|---|
| Samples | 1460 |
| Features | 80 |
| Target Variable | SalePrice |
| Numerical Features | 38 |
| Categorical Features | 43 |

The dataset contains detailed information about residential properties, including:

- General information
- Location details
- Land characteristics
- House quality and age
- Exterior features
- Basement and foundation
- Living areas
- Garage information
- Outdoor features
- Sale conditions

---

# 🔍 Exploratory Data Analysis (EDA)

A detailed EDA process was performed to understand relationships between features and house prices.

## Missing Values Analysis

Several features contained missing values, but many represented the absence of a feature rather than missing information.

Examples:

- PoolQC → 99.5%
- MiscFeature → 96%
- Alley → 93.8%
- Fence → 80%

Handling strategy:
- Categorical missing values → Filled with `"None"`
- Numerical missing values → Median imputation

---

# 📈 Key EDA Findings

## Strongest Features Affecting House Prices

| Feature | Correlation with SalePrice |
|---|---|
| OverallQual | 0.79 |
| GrLivArea | 0.71 |
| TotalBsmtSF | 0.61 |
| 1stFlrSF | 0.61 |
| FullBath | 0.56 |
| TotRmsAbvGrd | 0.53 |

### Important Insights:

- Overall house quality is the strongest predictor of price.
- Larger living areas significantly increase property value.
- Basement quality and size positively affect prices.
- Garage capacity and quality contribute to higher prices.
- Neighborhood has a major impact on property value.

---

# 🛠 Data Preprocessing

## Missing Values Handling

- Filled categorical features where missing values represented feature absence.
- Applied median imputation for numerical columns.

## Feature Selection

Removed low-impact features based on EDA analysis:

- Id
- Utilities
- Condition2
- MiscFeature
- Several low-correlation features

## Outlier Handling

Applied IQR-based clipping to reduce the impact of extreme values.

## Encoding

### Ordinal Encoding
Applied to quality-based features:

- ExterQual
- KitchenQual
- BsmtQual
- GarageQual
- PoolQC
- FireplaceQu

### Target Encoding

Applied to nominal categorical variables by replacing categories with their mean SalePrice.

## Feature Scaling

Used:

- RobustScaler

to reduce the effect of outliers.

---

# 🤖 Machine Learning Model

## Model Used

### Linear Regression

The dataset was split:

- Training Data: 80%
- Testing Data: 20%

The model was trained to predict:

---

# 📊 Model Performance

| Metric | Score |
|---|---:|
| R² Score | **0.9153** |
| Mean Absolute Error (MAE) | **15,282** |
| Mean Squared Error (MSE) | **413,868,764** |

---

# ✅ Results

The Linear Regression model achieved an **R² score of 91.5%**, meaning it successfully explains approximately **91.5% of the variation in house prices**.

The results demonstrate that Machine Learning can effectively capture relationships between property characteristics and market prices.

---

# 🖼 Visualization

The project includes:

- Missing values analysis
- Feature correlation analysis
- Price distribution
- Feature vs SalePrice analysis
- Actual vs Predicted price visualization

---

# 🧰 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---


---

# 🚀 Future Improvements

Possible improvements:

- Test advanced regression models:
  - Random Forest Regressor
  - XGBoost
  - LightGBM

- Apply:
  - Hyperparameter tuning
  - Feature selection techniques
  - Ensemble learning

---

# 👨‍💻 Author

**Abdelrhman Khalil**

Machine Learning Student

---

⭐ If you find this project useful, feel free to give it a star!


