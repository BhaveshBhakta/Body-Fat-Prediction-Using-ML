## Body Fat Prediction

### Project Overview

This project aims to predict an individual's **body fat percentage** based on various physical measurements. By analyzing features such as age, weight, height, and circumferences of different body parts (neck, chest, abdomen, hip, etc.), the goal is to develop a regression model that can accurately estimate body fat. This provides a non-invasive alternative to more complex body composition methods.

-----

### Technical Highlights

  * **Dataset**: The dataset used is `bodyfat.csv`, which contains body fat percentage and various body measurements.
  * **Size**: 252 entries, 15 columns.
  * **Key Features**:
      * `Age`, `Weight`, `Height`, `Neck`, `Chest`, `Abdomen`, `Hip`, `Thigh`, `Knee`, `Ankle`, `Biceps`, `Forearm`, `Wrist`.
  * **Approach**:
      * **Data Cleaning**: The dataset was clean with no missing values or duplicates. Outliers were removed using the Interquartile Range (IQR) method.
      * **Exploratory Data Analysis**: Histograms, box plots, and scatter plots were used for visualization to understand data distributions and feature relationships.
      * **Data Standardization**: `StandardScaler` was applied to all feature columns.
      * **Regression Task**: The target variable is `BodyFat`.
      * **Models Used**:
          * A suite of regression models were trained, including Ridge, XGBoost, Random Forest, AdaBoost, Gradient Boosting, Bagging, Decision Tree, SVR, and K-Nearest Neighbors (KNN).
  * **Best R² Score**:
      * **0.999** with Gradient Boosting Regressor.
      * **0.998** with Random Forest Regressor.
      * **0.997** with XGBoost Regressor.
      * The extremely high R² scores indicate that the models are highly effective at predicting body fat based on these physical measurements, which is expected as these measurements are often used in body fat estimation formulas.

-----

### Purpose and Applications

  * **Non-invasive body fat estimation** for fitness and health monitoring.
  * Assist fitness professionals in tracking client progress.
  * Support data-driven insights into the relationship between body measurements and body composition.
  * Provide a foundational model for personalized health and wellness applications.

-----

### Installation

Clone the repository and download the dataset.

Install the necessary libraries:

```bash
pip install pandas numpy seaborn matplotlib scikit-learn xgboost
```

-----

### Collaboration

We welcome contributions to improve the project. You can help by:

  * Investigating the impact of the data cleaning steps and trying alternative outlier handling strategies.
  * Performing comprehensive hyperparameter tuning and cross-validation for the top-performing regression models.
  * Exploring advanced feature engineering, such as calculating Body Mass Index (BMI) or other ratios from the raw measurements.
  * Adding explainability (e.g., SHAP or LIME) to understand which measurements are the most significant drivers of body fat prediction.
