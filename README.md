# 🏠 House Price Prediction – Machine Learning Project

## 📌 Project Overview

This project builds a **machine learning model to predict house prices** using various property features.
The workflow includes **data preprocessing, feature engineering, feature selection, model training, and evaluation**.

The goal is to develop a **robust regression model** capable of accurately predicting house prices using advanced ML techniques.

---

# 📊 Dataset Description

The dataset contains housing-related features such as:

* Bedrooms
* Bathrooms
* Square footage of living area
* Lot size
* Basement size
* Year built
* Renovation status
* Nearby property features

These variables are used to predict the **target variable: house price**.

---

# ⚙️ Project Workflow

## 1️⃣ Data Preprocessing

Initial preprocessing steps include:

* Importing necessary libraries
* Handling missing values
* Converting features to appropriate formats
* Selecting numeric features

Libraries used:

* numpy
* pandas
* matplotlib
* seaborn

---

## 2️⃣ Exploratory Data Analysis (EDA)

EDA helps understand the dataset and identify patterns.

Techniques used:

* Distribution analysis
* Histograms
* Skewness analysis
* Correlation analysis

This helps detect:

* Skewed features
* Important relationships
* Potential outliers

---

## 3️⃣ Feature Engineering

New features were created to improve model performance.

Examples:

* **HouseAge** = Current Year − Year Built
* Log transformations for highly skewed features

Example transformed features:

* sqft_lot_log
* sqft_lot15_log
* price_log

Log transformation reduces skewness and improves model stability.

---

## 4️⃣ Feature Scaling

Two scaling techniques were used:

### Standard Scaling

Applied to continuous variables such as:

* sqft_living
* sqft_above
* sqft_basement
* sqft_living15

### MinMax Scaling

Applied to count-based features like:

* bedrooms
* bathrooms

Scaling ensures features contribute evenly to the model.

---

## 5️⃣ Feature Selection

Three methods were used to select the most important features:

### 1. Correlation Filtering

Selects features most correlated with the target variable.

### 2. Recursive Feature Elimination (RFE)

Uses a linear regression model to recursively remove weaker features.

### 3. Random Forest Feature Importance

Ranks features based on importance scores.

Final features were chosen using the **intersection of all three methods**.

---

## 6️⃣ Model Training

Multiple regression models were tested.

Models explored include:

* Linear Regression
* Decision Tree Regressor
* Random Forest Regressor
* XGBoost Regressor
* LightGBM Regressor

The models were trained using:

* Train/Test split
* Cross-validation

---

## 7️⃣ Hyperparameter Tuning

Grid Search was used to optimize **XGBoost parameters**.

Example parameters tuned:

* n_estimators
* max_depth
* learning_rate
* subsample
* colsample_bytree

This helps improve model accuracy.

---

## 8️⃣ Model Evaluation

The model performance was evaluated using:

* **R² Score**
* Mean Absolute Error (MAE)
* Mean Squared Error (MSE)

Cross-validation was used to ensure reliable results.

---

# 📈 Final Model Performance

The final stacked model achieved approximately:

**R² Score ≈ 0.90**

This indicates the model explains about **90% of the variance in house prices**.

---

# 🧠 Key Skills Demonstrated

This project demonstrates skills in:

* Data preprocessing
* Exploratory Data Analysis
* Feature engineering
* Feature selection techniques
* Machine learning modeling
* Hyperparameter tuning
* Model evaluation
* Python data science ecosystem

---

# 🛠 Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* XGBoost
* LightGBM
* Jupyter Notebook

---

# 📂 Project Structure

```
House-Price-Prediction/
│
├── house_price.ipynb
├── README.md
└── dataset.csv
```

---

# 🚀 Future Improvements

Possible improvements include:

* Adding more advanced feature engineering
* Using deep learning models
* Implementing automated feature selection
* Deploying the model using a web API

---

# 📌 Conclusion

This project demonstrates a **complete end-to-end machine learning pipeline** for predicting house prices.
By combining **feature engineering, feature selection, and ensemble models**, the project achieves strong predictive performance.

---

⭐ If you found this project useful, consider giving it a star!
