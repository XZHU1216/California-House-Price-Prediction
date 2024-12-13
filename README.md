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
    - **Median absolute error (MedAE)**
  - Conducted error analysis to identify areas for improvement.

---

## **Results**
| Model              | Best Parameters                                                                 | R² Score (Nested CV) | MAPE (Nested CV)      | MedAE (Nested CV)        |
|--------------------|---------------------------------------------------------------------------------|-----------------------|-----------------------|--------------------------|
| Linear Regression  | {}                                                                              | 0.484 ± 0.011        | 30.955% ± 0.315%      | 39.026k$ ± 0.241k$       |
| Decision Tree      | {'max_depth': 10, 'min_samples_leaf': 5, 'min_samples_split': 2}                | 0.585 ± 0.011        | 22.832% ± 0.225%      | 25.831k$ ± 0.334k$       |
| Random Forest      | {'max_depth': None, 'min_samples_leaf': 2, 'min_samples_split': 2, 'n_estimators': 200} | 0.686 ± 0.011        | 19.357% ± 0.223%      | 20.921k$ ± 0.436k$       |
| Gradient Boosting  | {'learning_rate': 0.1, 'max_depth': 7, 'n_estimators': 200}                     | 0.688 ± 0.011        | 19.348% ± 0.256%      | 21.284k$ ± 0.118k$       |

---

## **Future Improvements**

1. Add additional data to enrich features, such as proximity to amenities, schools, or shopping areas, to better capture geographic factors.
    
2. Explore more advanced models like XGBoost or CatBoost, known for their robustness and performance with complex relationships.
    
3. Handle outliers better using techniques like quantile regression or adding indicator variables.
    
4. Optimize hyperparameters with techniques like RandomizedSearchCV to save time and perform in-depth analyses on cases where the model performed poorly.
