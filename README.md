# House Sales Linear Regression Analysis
<img width="514" alt="image" src="https://github.com/FridaOyucho/Predicting-Housing-Prices/assets/151248454/86c195e2-09c1-4f4c-bc27-232592bc3549">

## Authors
[Frida Oyucho]
[Thomas Otiende]
[Yvonne Kirigo]
[Sonia Ojay]
[Charles Egambi]
[Myles Mulusa]


## Overview

This repository contains the code and documentation for a project focused on utilizing multiple linear regression modeling to analyze house sales in a King county, Washington DC, where the housing market is undergoing substantial challenges. This project aims to predict house prices using linear regression based on various features such as the number of bedrooms, bathrooms, square footage, and location. The dataset used for this project contains information about houses sold, including their features and sale prices to provide insights and recommendations to stakeholders, particularly Real estate agents, Property owners, Homebuyers, Investors and Regulatory bodies, regarding how home renovations can potentially increase the estimated value of their properties and foster a more transparent, efficient, and competitive housing market in the county.


## Business Problem

<img width="513" alt="image" src="https://github.com/FridaOyucho/Predicting-Housing-Prices/assets/151248454/05c59b39-b0e7-4474-a97d-56f166e6d144">

The primary challenge facing stakeholders in King County's real estate market is accurately predicting house prices.
The dynamic nature of the housing market, coupled with factors such as population growth, economic fluctuations, and changing buyer preferences, makes it difficult to determine optimal pricing strategies for properties. 
Real estate agents and homeowners often struggle to set competitive prices that reflect the true value of their properties and meet market demand. 
In the absence of accurate price predictions, stakeholders may encounter difficulties in selling properties efficiently, maximizing returns on investments, and maintaining competitiveness in the market. 
Addressing this business problem requires developing robust predictive models and leveraging data-driven insights to guide pricing decisions effectively in the County's real estate market.


## Data

The data used in this analysis was from 'kc_house_csv' database. The selected datasets from the listed database provide information needed when looking at house prices.


## Methods

The project uses descriptive analysis and inferential analysis including histograms, scatter plots, bar graphs, relation matrix e.t.c. 

The following steps were undertaken:
Data Understanding: Explore the dataset to understand the features and their potential impact on home values. Identify any data quality issues or limitations that may need to be addressed.

Data Preparation: Clean the data by handling missing values or outliers and perform any necessary feature engineering to prepare the dataset for regression modeling.

Model Training: We train a linear regression model using the 'LinearRegression' class from scikit-learn. The training data is preprocessed by scaling numerical features and encoding categorical variables. After training the model, we make predictions on the test data and evaluate its performance using metrics such as mean absolute error.

Model Evaluation: We evaluate the trained model's performance using mean absolute error (MAE) and R-squared score. The MAE measures the average absolute difference between the predicted and actual house prices, while the R-squared score indicates the proportion of variance in the target variable explained by the model.

Dealing with Categorical Data: Categorical variables are one-hot encoded before training the model. This ensures that categorical features are represented as binary vectors, making them suitable for linear regression.


## Results

Univariate Analysis:

<img width="570" alt="image" src="https://github.com/FridaOyucho/Predicting-Housing-Prices/assets/151248454/1ce4b7c1-2560-4f4f-838e-fcdd5990a929">

The analysis reveals that houses with average condition have the highest count at 10,903.
Further, about 4,461 houses have a good condition while there are only 17 houses in poor condition.


Bivariate Analysis:

<img width="578" alt="image" src="https://github.com/FridaOyucho/Predicting-Housing-Prices/assets/151248454/67a6ec3d-e058-4232-8d5f-f24ffae1ea82">

The distribution of the latitude is negatively skewed.
The number of houses increase as the latitude increases.
Majority of the houses are located between approximately latitude 47.48-47.72 degrees above sea-level.

Multivariate Analysis:

<img width="543" alt="image" src="https://github.com/FridaOyucho/Predicting-Housing-Prices/assets/151248454/122cdc85-9f61-4aff-8cf6-bb25a977aebe">

From the correlation matrix, sqft_living has the highest positive correlation with price at 0.57. This suggests a moderately positive linear relationship between the living area size (in square feet) and the price of the property.

This is in line with the expectation of the houses with larger sqft living commanding higher prices. Sqft lot has the weakest negative correlation with price at -0.026. This implies that the size of the lot (in square footage) is not a strong determinant of the property price in the dataset.

### Simple Linear Regression Model

![image](https://github.com/FridaOyucho/Predicting-Housing-Prices/assets/151248454/8f42e8e0-d6bc-4162-8215-32f2b1791589)

1. The r-squared value of the Simple Linear regression model was 32.7%. This value indicates that approximately 32.7% of the variability in the dependent variable (Price) is accounted for by the independent variable(sqft_living) in our model. Meaning the remaining 67.3% of the variability is not accounted for.
2. The r-squared value of 32.7% suggests a moderate level of explanatory power of our regression model. This result highlights the need for further research to explore additional variables and factors that may influence the dependent variable (Price) and to improve the predictive accuracy and explanatory power of the model.
3. Is the model statistically significant at 𝛼=0.05? The p-value obtained is  0.000 which is less than the 𝛼=0.05 thereby concluding that the model is statistically significant.
Further results show that a y-intercept of $144,762.76 was achieved, meaning for every increase of 1 square foot living area, the price increases by $166.98



### Multiple Linear Regression Model

![image](https://github.com/FridaOyucho/Predicting-Housing-Prices/assets/151248454/de23c021-d430-4ff8-97d0-a741b5de08ea)

1. The Multiple Regression model had an r-squared value of 69.1% demonstrating substantially improved explanatory power compared to the simple linear regression model which had an r-squared value of 32.7%.
2. The inclusion of additional independent variables in the multiple regression model significantly enhanced the model's ability to explain the variability in the price.
3. The r-squared values and the comparison between the two models highlight the importance of considering multiple factors and variables in regression analysis to develop a more comprehensive and accurate understanding of the relationship between the independent variables and the price.


## Conclusion

The analysis provides valuable insights into the factors influencing house prices in King County's real estate market. By leveraging these insights and adopting data-driven pricing strategies, stakeholders can optimize pricing decisions, maximize returns on investments, and maintain competitiveness in the dynamic real estate market.

