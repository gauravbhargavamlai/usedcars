# Used Car Price Prediction

This project applies the CRISP-DM (Cross-Industry Standard Process for Data Mining) methodology to build a regression model that predicts used car prices. The dataset is sourced from a real-world used vehicle listing.

## 🧠 CRISP-DM Phases Followed

### 1. Business Understanding  
Understand pricing dynamics in the used car market and build a model to aid dealer decision-making.

### 2. Data Understanding  
The dataset was loaded and explored to understand its structure, data types, and potential anomalies. Some examples of domain-specific quality checks:

- **Future Years**: Vehicles with a manufacturing year beyond 2025 (impossible or mistyped).
- **High Prices**: Prices above $100,000 flagged as suspicious.
- **Low Prices**: Vehicles priced under $1,000 considered potentially invalid listings.
- **Old Cars**: Cars older than 20 years (before 2005) excluded based on dealer preference.
- **High Odometer**: Vehicles with mileage over 150,000 miles flagged for scrutiny.

These checks helped improve data integrity and align the dataset with dealership goals (modern cars with reasonable usage and pricing).

### 3. Data Preparation  
- Missing values handled using `SimpleImputer`
- Categorical encoding using `OrdinalEncoder`
- Scaling and transformation of numeric features
- Filtering outliers and unrealistic records

### 4. Modeling  
Regression models were trained using:
- `LinearRegression`
- `Lasso`
- Polynomial feature transformations
- Feature selection via mutual information and sequential selectors

Hyperparameter tuning was done using `GridSearchCV`.

### 5. Evaluation  
Performance was evaluated using:
- **R² Score**
- **RMSE**
- Feature importance plots and residual analysis

### 6. Deployment  
Final plots and outputs were saved in the `/images` directory for delivery to stakeholders.

## 🚀 Technologies Used

- Python
- Pandas, NumPy
- Scikit-learn
- Seaborn, Matplotlib
- Google Colab & Google Drive
