## CMPE 255 - Team Project - Spring 2022

# NYC-Housing-Price-Prediction

## Team Members
------------------------------------------------------------------------
|   SJSU ID    |         Name       |             Github               |
|--------------|--------------------|----------------------------------|
|  015280330   | Priyank Jagad      | https://github.com/priyank59     |
|  015923778   | Aanchal Agarwal    | www.github.com/Aaanchal10        |
|  015962128   | Abhiram Yenugadhati| https://github.com/neveram       |
|  015913495   | Praneetha Moturi   | https://github.com/praneetha-moturi                                 |

##Presentation Link
https://youtu.be/5wxmed8o8Ec

## Abstract

Price prediction of properties is one of the most important applications in real estate as the housing market goes through a lot of up-and-downs due to volatile economic cycles. A lot of real estate companies depend on the housing market for their bread and butter such as Real Estate Investment Trust. Such businesses also invest in the apartments and houses in New York state and try to regulate their internal pricing models. In New York City, the housing market including the property prices is quite buoyant due to a lot of macroeconomic reasons. However, it is pertinent to note that the inherent characteristics of the house also is a contributing factor to its pricing. Hence, for purchasers and house investors, having knowledge about the driving factors that influence the pricing of a house in United States is quite helpful in making wise purchasing decisions. The aim of this project is to predict the house listing’s prices in the United States, specifically the state of New York City as that is where housing prices are most volatile. We will use particular features of the nearby neighborhoods and perform regression analysis. After which, we will optimize our model with techniques such as model tuning, feature selection etc. The dataset that we have chosen is from the NYC department of finance which contains information about the sale of properties in New York City over a period of 12 months. The dataset contains about 167720 property sales information pieces. In our dataset, amongst most attributes we will have the Block, neighborhood, borough, Lot, Address, Apartment Number, Zip code. We will then try to implement supervised learning techniques. In this problem, our target variable will be sales price and the remaining features will help us to predict sales price for unseen data. Also, we will not use Sale Date during our prediction because our problem time at which our property got sold has no relation with target variable. There are many features like Borough, Neighborhood, Block, Lot, Address, Apartment Numbers, Zip Code are all related to location and there must be high co-relation among these features. We have also created visualization plots which will be helpful for classification of Commercial Units vs Sale Price and Residential unit’s vs Sale Price. We have plotted Box Plot for each feature in order to visualize the residing outliers present in each feature. We also implemented normalization techniques to scale like Min-Max normalization our numerical features in range of [-1,1]. Later on we have split our dataset into train and validation set to evaluate our model’s performance in unseen data. We have used hyperparameter tuning and r2-score metrics to find the best model with best parameters from different regression models available like Random Forest, Decission Tree, Linear Regression and XGBoost. We have also developed a web application which will take input features from user and predict sales price of house based on their input.


## Problem Statement

We will perform regression analysis, lasso regression, random forest regression and ridge regression and optimize our chosen model to the best accuracy
with feature selection, model tuning and other techniques. Meanwhile, the resulting model will create
potential benefits in multiple areas beyond basic price prediction, such as:
1) providing data-proven insights for individual house buyers and sellers;
2) enhancing a balanced leverages between the buyers and sellers;
3) understanding the housing market in general for economists, policy makers or interested
stakeholders/ decision makers.

## Dataset:

The dataset we are using is sales of appartments located in  5 different counties in newyork city.

Dataset : https://www1.nyc.gov/site/finance/taxes/property-annualized-sales-update.page.

Dataset consists of 21 Columns: Neighborhood, Building Class Category, Tax Class at Present, Address, Appartment No, Residential Units, Commercial Units, Total Units, Land Square feet, Gross Square feet, Year Built, Tax Class at Time of Sale, Building Class at Time of Sale, Sale Price, Sale Data.

## Methodology

Problem type : Supervised Learning

Algorithms : 

- Linear Regression
- Lasso Regression
- Ridge Regression
- Elastic Net
- Light Gradient Boosting Machine 
- XGBoost
- K-Neighbors Nearest Regression 
- Decision Tree
- Random Forest 
- Cat Boost
- Artificial Neural Network

## TO-DO :

- Data Preprocessing
- Feature Visualization
- Performing Normalisation
- Visualising Correlation plots among features
- Analyzing and visualization of the distribution of data
- Analysing Mean, Median sale price of buildings in different years

## Measurement of Success :

- The aim of our project is to find the best optimal model with parameters from different regression models to predict the house listing’s prices in New York city.







