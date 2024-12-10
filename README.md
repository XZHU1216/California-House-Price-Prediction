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
  - Handled missing data (`total_bedrooms`) via imputation.
  - Performed feature transformations, including logarithmic transformations to reduce skewness.
  - Encoded categorical features like `ocean_proximity`.
  - Standardization to put numerical variables on the same scale     

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
    - **Mean Squared Error (MSE)**
  - Conducted error analysis to identify areas for improvement.

---

## **Results**

| Model                  | Best Parameters                               | R² (Cross-Validated) |
|------------------------|-----------------------------------------------|----------------------|
| **Linear Regression**  | None                                         | 0.484 ± 0.009       |
| **Decision Tree**      |Tuned via Nested Cross-Validation       | 0.585 ± 0.012       |
| **Random Forest**      | Tuned via Nested Cross-Validation       | 0.686 ± 0.013       |
| **Gradient Boosting**  | Tuned via Nested Cross-Validation            | 0.700 ± 0.006       |

---

## **Future Improvements**

1. Add additional data to enrich features, such as proximity to amenities, schools, or shopping areas, to better capture geographic factors.
    
2. Explore more advanced models like XGBoost or CatBoost, known for their robustness and performance with complex relationships.
    
3. Handle outliers better using techniques like quantile regression or adding indicator variables.
    
4. Optimize hyperparameters with techniques like RandomizedSearchCV to save time and perform in-depth analyses on cases where the model performed poorly.
