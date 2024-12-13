# California-House-Price-Prediction

This project aims to predict housing prices in California using the California Housing Dataset "_housing.csv_". The analysis includes data preprocessing, feature engineering, model training, evaluation, and error analysis to build a robust predictive model. You can find more details and the program code in "_California Housing Prices.ipynb_".

The dataset contains 20640 entries and 10 variables following.

    Longitude
    Latitude
    Housing Median Age
    Total Rooms
    Total Bedrooms
    Population
    Households
    Median Income
    Median House Value
    Ocean Proximity

---

## **Project Overview**

Predicting housing prices is crucial for decision-making in real estate, city planning, and public policy. This project leverages machine learning models to predict median_house_value based on various features, including geographical data, socio-economic variables, and housing characteristics.

---

## **Key Steps**

- **Exploratory Data Analysis (EDA)**:
  - Visualized feature distributions and correlations.
  - Identified key predictors like `median_income` and geographical variables (`longitude`, `latitude`).

- **Data Preprocessing**:
  - Handled exteme values via imputation and delete missing data (`total_bedrooms`).
  - Performed feature transformations, including logarithmic transformations to reduce skewness.
  - Encoded categorical features like `ocean_proximity`.
  - Standardization to put numerical feartures on the same scale     

- **Model Development**:
  - Trained models:
    - Linear Regression
    - Decision Tree Regressor
    - Random Forest Regressor
    - Gradient Boosting Regressor (GBR)
  - Tuned hyperparameters using `GridSearchCV` and validated models with nested cross-validation.

- **Evaluation**:
  - Assessed model performance using metrics such as:
    - **R²** (Coefficient of Determination)
    - **Mean absolute percentage error (MAPE)**
    - **Median absolute error (MAE)**
  - Conducted error analysis to identify areas for improvement.

---

## **Results**
| Model              |   R² Score | Mean Absolute Percentage Error (MAPE)   | Median Absolute Error (MedAE)   |
|--------------------|------------|------------------------------------------|----------------------------------|
| Linear Regression  |      0.476 | 31.120%                                  | 39.200 k$                       |
| Decision Tree      |      0.585 | 22.548%                                  | 25.292 k$                       |
| Random Forest      |      0.693 | 19.162%                                  | 20.226 k$                       |
| Gradient Boosting  |      0.691 | 19.473%                                  | 21.059 k$                       |

---

## **Future Improvements**

1. Add additional data to enrich features, such as proximity to amenities, schools, or shopping areas, to better capture geographic factors.
    
2. Explore more advanced models like XGBoost or CatBoost, known for their robustness and performance with complex relationships.
    
3. Handle outliers better using techniques like quantile regression or adding indicator variables.
    
4. Optimize hyperparameters with techniques like RandomizedSearchCV to save time and perform in-depth analyses on cases where the model performed poorly.
