# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 2 - Ames Housing Data and Kaggle Challenge

### Problem Statement

An understanding of the housing market is important for homeowners, buyers, and real estate professionals. The goal of this project is to analyze the Ames Housing Dataset, and predict house prices in Ames, Iowa using machine learning model to understand elements that influence house prices in this area of the country. Features such as overall quality, living area, basement size, and more, are examined to develop a predictive model that accurately estimates house prices. 

Predicting house prices is important in the real estate industry. Accurate valuations is important for both buyers and sellers to make informed decisions. Machine learning models offers a good approach to analyze housing market data, and predict a reliable price estimates.


---

### Data Dictionary

| Feature       | Type  | Dataset | Description                                           |
|---------------|-------|---------|-------------------------------------------------------|
| OverallQual   | int   | train.csv | Overall material and finish quality                |
| GrLivArea     | int   | train.csv | Above grade (ground) living area square feet          |
| CentralAir    | object| train.csv | Central air conditioning                              |
| TotalBsmtSF   | float | train.csv | Total square feet of basement area                    |
| Street        | object| train.csv | Type of road access to property                       |
| YearBuilt     | int   | train.csv | Original construction date                            |
| FullBath      | int   | train.csv | Full bathrooms above grade                            |
| SalePrice     | int   | train.csv | Property's sale price in dollars (target variable)    |



---

### Executive Summary

#### Datasets

The following are the 3 datasets used for this project. 

**Datasets Used**

* [`train.csv`](./datasets/train.csv): Training datasets for Ames Iowa Housing with Sale Price
* [`test.csv`](./datasets/test.csv): Testing datasets for Ames Iowa Housing without Sale Price


#### Data Cleaning

* Selected numeric features with correlation >= 0.5 with the target (sale price), and randomly selected two categorical features 'Central Air' and 'Street'.
* Imputed missing values in the 'Total Bsmt SF' (`Total square feet of basement area`) column using KNNImputer.
* Addressed multicollinearity by retaining features correlated with the target but uncorrelated with each other.
* Identified and removed outliers to improve model.
* Developed baseline predictions and evaluated ridge regression and lasso models.

  
**Questions Explored**
* Which features contribute most to house prices in Ames, Iowa?
* What factors have the most significant impact on predicting house prices accurately?
* How do ridge regression and lasso regression models compare in predicting house prices?

#### Conclusions and Recommendations

##### Conclusions

* Features like overall quality, living area, and basement size significantly influence house prices in Ames, Iowa.
* The ridge regression model performs better than the baseline and lasso model, and it provides a more accurate predictions with lower mean squared error (MSE) and root mean squared error (RMSE) values.
* The lasso regression model have poor performance, and it shows that the selected features do not contribute to predictions.
* The model's accuracy in Ames, Iowa may not apply universally because of different housing market factors and demographics in different areas. For model to perform well for different cities, it is important to collect more data from different cities and areas.

##### Recommendations
* Homeowners should focus on improving overall quality and living space to increase property values.
* Buyers should prioritize properties with desirable features such as spacious living areas and modern amenities.
* Real estate professionals can use the predictive model to offer accurate pricing estimates, and this will help with informed decision-making in the housing market.


