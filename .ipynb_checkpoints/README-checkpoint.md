# Predicting Housing Prices for House Hunters in Ames, Iowa

As a data scientist hired by the reality TV show House Hunters, my task is to create a predictive model that accurately estimates housing prices in Ames, Iowa. The show's producers want me to provide a reliable tool for couples on the show to help them make informed decisions while searching for their dream home in Ames.

For this project, I will analyze the extensive Ames Housing Dataset, which includes a wide range of features associated with residential properties in Ames. My objective is to develop a machine learning model that can accurately predict the sale prices of houses based on these features. This will assist the House Hunters participants in understanding the fair market value of the properties they encounter during their search.


# Data Dictionary

Due to the large amount of features, all relevent information is linked below. 

https://jse.amstat.org/v19n3/decock/DataDocumentation.txt


# Executive Summary

To ensure high-quality data, I conducted a thorough data inspection, cleaning, and pre-processing phase. I handled missing numeric values by using robust median imputation and excluded features with over 50% missing values or consistent values throughout the dataset as non-informative. For houses lacking essential features like a garage or basement, I applied suitable categorical imputations to maintain dataset consistency.

In the feature selection process, I prioritized numeric features with a correlation coefficient above 0.3, indicating strong predictive potential. Categorical feature selection followed a customized approach that resembled real-life home purchase criteria. I identified and removed outliers through pairplot visualizations and comprehensive descriptions.

To ensure uniform scaling, I performed data standardization, which was crucial for creating polynomial features that could possibly amplify feature discrepancies. Categorical data were transformed into numerical formats using one-hot encoding, making them suitable for the machine learning model. I appropriately processed features like "Overall Quality" considering their numerical and categorical aspects.

The machine learning model I implemented, the LassoCV Regression, performed exceptionally well. It achieved an R-squared score of 0.938 on the training data and 0.936 on the test data, demonstrating high predicition power and good generalization to unseen data. The model predicted a base sale price of 168,274.13 when all house features are zero, with an average deviation from actual house prices of 20,179.96 (Root Mean Square Error).

The model's unbiased predictions and reliability were confirmed through evidence of homoscedasticity and normality of errors. The equal spread of residuals across predicted values and their normal distribution further affirmed the model's competence in accurately predicting Ames housing market prices.