# Predicting Housing Prices for a Real Estate Investment Trust (REIT)

## Introduction

In this project, the objective is to predict the market price of residential real estate based on a set of features such as square footage, number of bedrooms, number of floors, and additional house characteristics. The Real Estate Investment Trust (REIT) seeks to start investing in residential properties and needs an accurate pricing model to help guide their investments. As part of the Data Science Professional Certificate offered by IBM, this project was undertaken to explore different data analysis techniques, data preprocessing steps, feature engineering, and machine learning models.

## Data Collection

The data used in this project was obtained from a publicly available dataset called King County House Sales Dataset. This dataset contains information about various houses in King County, Washington, including their sales price and features such as square footage, number of bedrooms, number of floors, and more.

The dataset was accessed via Kaggle, a popular platform for sharing datasets and learning about data science. The link to the dataset can be found here.

## Audience and Beneficiaries

The primary audience for this project includes:

Data Analysts and Data Scientists: They will benefit from understanding the detailed steps involved in the data preprocessing, exploration, and model development process. The project demonstrates various techniques that can be applied to real-world datasets to create predictive models.

Real Estate Investors: The model can help REITs and individual investors in estimating property values based on key features. The insights gained from the analysis can be used to make informed investment decisions.

Academia and Learners: Individuals studying data science or machine learning can gain hands-on experience with real-world datasets and gain insights into model selection and evaluation.
Exploratory Data Analysis (EDA)

Exploratory Data Analysis (EDA) is a crucial step in understanding the structure and characteristics of the dataset. In this project, we first examined the data to understand its features, check for any missing values, and identify potential outliers or anomalies.

## Data Preprocessing:

Missing values were handled by imputing the mean of the respective columns (e.g., bedrooms, bathrooms) for missing data.
Outliers were detected and visualized using boxplots and histograms.

Categorical columns were processed and encoded appropriately.
Feature Engineering:

Some features such as sqft_living, sqft_above, and sqft_basement were found to be highly correlated with the target variable (price), so they were kept as key predictors in the models.
Other features like floors, view, and waterfront were also included as they play a significant role in determining house prices.

## Visualizations:

Correlation Heatmap: This helped visualize the relationships between various features and the target variable (price). For instance, sqft_living, sqft_above, and grade showed strong positive correlations with price.

Boxplots and Histograms: These were used to explore the distribution of house prices and identify outliers.

## Models Used and Their Performance

Several machine learning models were applied to predict housing prices. The following models were tested:

Linear Regression:

Linear regression was used to model the relationship between house prices and a single feature (long for longitude).
The R² value was calculated to evaluate the performance, resulting in an R² of approximately 0.00047, indicating that the feature long was not a strong predictor of price on its own.
Multiple Linear Regression:

A multiple linear regression model was built using a set of features, including floors, waterfront, lat, bedrooms, sqft_basement, view, bathrooms, sqft_living15, sqft_above, and grade.
The model achieved a considerably higher R² value, indicating that combining multiple features improved the model's predictive power.
Ridge Regression:

Ridge regression was applied with the regularization parameter set to 0.1. Ridge regression is useful when dealing with multicollinearity among features.
The R² value for the Ridge regression model was 0.6478, suggesting that regularization improved the model by reducing overfitting.
Polynomial Regression:

A second-order polynomial transformation was applied to the training and test data, followed by fitting a Ridge regression model.
The R² value improved to 0.7003, which was a notable increase over the simple Ridge regression model. This indicates that the polynomial transformation allowed the model to better capture nonlinear relationships between the features and the target.

## Results and Insights

After training and evaluating various models, the following results were obtained:

Linear Regression with a Single Feature (long):

R²: 0.00047
This result suggests that the longitude feature alone is not sufficient to predict house prices accurately.
Multiple Linear Regression with Key Features:

R²: 0.65
A significantly better model, leveraging multiple features such as sqft_living, sqft_above, and grade.
Ridge Regression:

R²: 0.6478
Ridge regression performed slightly worse than multiple linear regression but was still a strong contender. It helped to reduce overfitting by introducing regularization.
Polynomial Regression with Ridge Regularization:

R²: 0.7003
The best-performing model was polynomial regression with Ridge regularization. The polynomial transformation helped capture more complex, nonlinear relationships, and Ridge regularization improved the model by preventing overfitting.

## Conclusion
The best-performing model was the Ridge regression model with polynomial transformation, which achieved an R² of 0.7003. This indicates that the model was able to explain approximately 70% of the variance in house prices based on the features provided. The polynomial transformation allowed the model to better capture non-linear relationships, while Ridge regularization helped prevent overfitting.

Thus, this model can be considered the most reliable for predicting house prices, especially when dealing with complex, non-linear relationships in real estate data.

## Acknowledgements

This project is part of the IBM Data Science Professional Certificate. The dataset was obtained from Kaggle, and the methods used for the analysis were inspired by standard practices in data science and machine learning. This project helped deepen the understanding of regression techniques and the importance of feature selection, model evaluation, and transformation in predictive modeling.

## Final Thoughts

This project serves as a valuable hands-on experience for anyone looking to gain expertise in data science and machine learning. By working with real estate data, exploring different preprocessing and modeling techniques, and evaluating the results, this project provides a comprehensive view of the steps involved in building an effective predictive model. Whether for real estate investment, business analysis, or educational purposes, the techniques learned here can be applied to various datasets and industries.






