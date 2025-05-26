# Predicting Housing Prices for a Real Estate Investment Trust (REIT)

## Project Description

This project aims to develop a predictive model for estimating the market price of residential properties based on features such as square footage, number of bedrooms, number of floors, and other house characteristics. The goal is to support a Real Estate Investment Trust (REIT) in making informed investment decisions by accurately predicting property values.

Who will benefit from this project?

* **Real Estate Investors** gain a reliable tool to estimate home prices, helping guide investment choices and portfolio management.
* **Data Analysts and Data Scientists** can learn practical data preprocessing, feature engineering, and regression modeling techniques applied to a real-world dataset.
* **Students and Learners** in data science benefit from exposure to hands-on predictive modeling and evaluation processes.

## Dataset Overview

The dataset used is the King County House Sales Dataset, publicly available on Kaggle. It contains detailed information on residential home sales in King County, Washington, including sales prices and features like square footage, bedrooms, bathrooms, floors, waterfront presence, and more.

## How Was This Project Done?

The approach involved several key steps:

1. **Exploratory Data Analysis (EDA)** to understand the data structure, detect missing values, and identify outliers using visualizations like boxplots and histograms.

2. **Data Preprocessing** included imputing missing values (e.g., bedrooms, bathrooms) with column means and encoding categorical features appropriately.

3. **Feature Engineering** prioritized highly correlated features such as `sqft_living`, `sqft_above`, and `grade` as key predictors. Additional features like floors, view, and waterfront were also included.

4. **Visualizations** such as correlation heatmaps highlighted strong positive relationships between features and house price, guiding model input selection.

5. **Model Development and Evaluation**: Multiple regression models were trained and compared:

   * **Simple Linear Regression** using longitude alone
   * **Multiple Linear Regression** with multiple features
   * **Ridge Regression** with regularization to reduce multicollinearity and overfitting
   * **Polynomial Regression with Ridge Regularization** to capture nonlinear relationships

Performance was measured using the R² metric to evaluate how well models explained the variance in housing prices.

## Key Findings

* **Does longitude alone predict house prices well?**
  No. Simple linear regression using longitude had an R² of only 0.00047, showing it is not a meaningful predictor by itself.

* **Does adding multiple features improve predictions?**
  Yes. Multiple linear regression with features like `sqft_living`, `bedrooms`, `grade`, and `waterfront` achieved an R² around 0.65, showing much better predictive power.

* **Can regularization improve the model?**
  Applying Ridge regression gave an R² of 0.6478, slightly lower but more robust by controlling overfitting.

* **Does modeling nonlinear relationships help?**
  Yes. Polynomial regression combined with Ridge regularization raised the R² to 0.7003, indicating a better fit by capturing complex patterns in the data.

* **What does the best model explain?**
  The best model explains approximately 70% of the variability in house prices based on the selected features.

## Conclusion

The project demonstrates that predicting housing prices requires combining multiple features and capturing nonlinear relationships. Polynomial regression with Ridge regularization proved to be the most effective approach, explaining about 70% of the price variance. This suggests that sophisticated modeling techniques are essential to accurately estimate property values in real estate.

This model offers a reliable foundation for REITs or investors to evaluate residential properties based on relevant home characteristics and market data.

## Recommendations

For practical deployment, further refinement can include:

* Incorporating additional external factors such as neighborhood quality or economic indicators.
* Continuous updating of the model with new sales data to maintain accuracy over time.
* Using more advanced nonlinear models or ensemble methods to potentially improve predictions.

Nonetheless, this project establishes a solid, interpretable baseline for housing price prediction in King County.

## Acknowledgements

This project was completed as part of the IBM Data Science Professional Certificate. The King County House Sales dataset was sourced from Kaggle. The methodology follows standard data science practices in regression modeling and feature engineering, providing valuable hands-on experience with real-world housing data.
