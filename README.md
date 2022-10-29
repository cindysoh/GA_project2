# Project 2 - Ames Housing Data and Kaggle Challenge

## Introduction

Beneath the small town charm of Ames, Iowa, beats the heart of a much larger city. With a population of more than 65,000, Ames offers cultural, recreational, educational, business, and entertainment amenities more common in bigger metros. As a growing city, Ames continues to focus on building a strong community filled with opportunities for all. 

There is a interest level in housing of Ames. Thus the need to predict the price of a house at sales. 

By creating a regression model based on the Ames Housing Dataset. This model will predict the price of a house at sale.

The Ames Housing Dataset is an exceptionally detailed and robust dataset with over 70 columns of different features relating to houses.


## Problem Statement

We are from a data-driven real estate company that wants to determine the most important characteristics that affect housing prices in Ames, Iowa.

Target audience: Investors in our company

Question to Answer:
- Which features appear to add the most value to a home?
- Which features hurt the value of a home the most?
- What are things that homeowners could improve in their homes to increase the value?
- What neighborhoods seem like they might be a good investment?


Before you begin working on this project, please do the following:

1. Sign up for an account on [Kaggle](https://www.kaggle.com/)
2. **IMPORTANT**: Click this link ([Regression Challenge Sign Up](https://www.kaggle.com/t/2dde5663e03b4165b853ff65e723c26d)) to **join** the competition (otherwise you will not be able to make submissions!)
3. Review the material and download data files on the [DSI-US-11 Regression Challenge](https://www.kaggle.com/c/dsi-us-11-project-2-regression-challenge)
4. Review the [data description](http://jse.amstat.org/v19n3/decock/DataDocumentation.txt).

## Content

### 1. EDA and Cleaning

* [1.1 EDA and Analysis](#1.1-EDA-and-Analysis)
    * [1.1.1 Numerical Features](#1.1.1-Numerical-Features)
    * [1.1.2 Categorical Features](#1.1.2-Categorical-Features)
    
* [1.2 Data Cleaning](#1.2-Data-Cleaning)
    * [1.2.1 Outlier](#1.2.1-Outlier)
    * [1.2.2 Null Values](1.2.2-Null-Values)
    * [1.2.3 Encoding Remaining Categorical Features](#1.2.3-Encoding-Remaining-Categorical-Features)
    * [1.2.4 Saving Cleaned Dataset](#1.2.4-Saving-Cleaned-Dataset)

### 2. Preprocessing and Feature Engineering

* [2.1 Feature Selection](#2.1-Feature-Selection)
    * [2.1.1 Skewed Distribution](#2.1.1-Skewed-Distribution)
    * [2.1.2 Correlation](#2.1.2-Correlation)
    * [2.1.3 P-Value](#2.1.3-P-Value)    
    * [2.1.4 Saving Final Dataset](#2.1.4-Saving-Final-Dataset)

### 3. Model Benchmarks

* [3.1 Feature Selection](#3.1-Model-Preparation)
    * [3.1.1 Scaling](#3.1.1-Scaling)
    * [3.1.2 Instantiate Models](#3.1.2-Instantiate-Models)
    * [3.1.3 Cross Validation](#3.1.3-Cross-Validation)    
    * [2.1.4 Saving Final Dataset](#2.1.4-Saving-Final-Dataset)
    
* [3.2 Models Fitting and Evaluation](#3.2-Models-Fitting-and-Evaluation)
    * [3.2.1 Linear Regression](#3.2.1-Linear-Regression)
    * [3.2.2 Lasso Regression](#3.2.2-Lasso-Regression)
    * [3.2.3 Ridge Regression](#3.2.3-Ridge-Regression)    

* [3.3 Optimising Alpha](#3.3-Optimising-Alpha)
    * [3.3.1 Lasso Regression](#3.3.1-Lasso-Regression)
    * [3.3.2 Ridge Regression](#3.3.2-Ridge-Regression)    
    * [3.3.3 Elastic Net](#3.3.3-Elastic-Net)

* [3.4 Conclusion](#3.4-Conclusion)

## Summary

From our finding and analysis, we can see certain feature have more positive and negative effect on SalePrice. Some of the top features for prediction are GrLivArea, OverallQual and YearBuilt which seem to be reasonable for affecting SalePrice. Certain Neigborhood seem to have positive effect on SalePrice, which might be those more desirable areas. Bsmt, Garage can also play a part in increasing SalePrice. 

### Top 10 Positive Coefficient Feature
|variable|coef|
|---|---|
|GrLivArea|27366.120619|
|OverallQual|11976.649996|
|YearBuilt8549.112980|
|Neighborhood_NridgHt|8242.509729|
|BsmtLivArea|8045.530091|
|TotalBsmtSF|7651.534862|
|ExterQual|6519.907073|
|OverallCond|6421.883374|
|Neighborhood_StoneBr|5920.283338|
|KitchenQual|5243.340334|

### Top 10 Negative Coefficient Feature
|variable|coef|
|---|---|
|MSSubClass_120|-6735.277092|
|MSSubClass_160|-4147.104147|
|MasVnrType_BrkFace|-3606.637346|
|BedroomAbvGr|-3360.376580|
|SaleType_COD|-3342.850812|
|SaleType_WD|-2860.737321|
|BsmtCond|-2784.738520|
|KitchenAbvGr|-2580.763355|
|Exterior_HdBoard|-1760.727968|
|GarageType_Attchd|-1718.178176|


## Data Dictionary

Review the [data description](http://jse.amstat.org/v19n3/decock/DataDocumentation.txt)
