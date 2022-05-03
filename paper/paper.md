## About this Project : 

Our team aims to predict the prices of the house listings in New York City. 
We use selected features of the close-by neighbourhoods. We will also perform regression analysis and optimise our chosen model to the best accuracy with feature selection, model tuning and other techniques. 

Our Final Resulting model will create potential benefits in multiple areas beyond price prediction as follows,

- Provides data-proven insights for individual house buyers and sellers.
- Enhances a balanced leverage between the buyers and sellers.
- Understanding the housing market in general for economics, policy makers or interested stakeholders or decision makers.

## About Dataset :

The NYC Department of Finance 1 provided the data for this study. 
The original dataset contains 167719 items of property sales data from January 2018 to December 2019 in New York City (over a two-year period). 
Each data instance includes demographics like address, region code, neighbourhood, building information like kind, number of units, building land area, and sale date. 
There are a total of 21 features (details are shown in appendix A). 
We will not investigate the impact of time on sale price in this project, hence SALE DATE will not be utilised to forecast the sale price (target variable) of a NYC property. 

## Data Preprocessing :

Definition : 




## Feature Selection 

Definition : 

In this step we dropped the following columns;

Neighbourhood 
Address
Apartment numbers
Zip code
Building class as of final roll 18/19
Building class at time of sale
Tax class as of final roll 18/19
Sale Date

We also dropped Easement because it only contains null values.

## Feature Engineering

Definition : 

Classification :

Definition : 


Observation :

Based on the scatter plots of Commercial Units vs Sale Price and Residential Units vs Sale
Price, the pattern is opaque and there are lots of 0s, 1s in each plot. Hence we will classify them into six
groups. Here we will use a new variable “UNIT CATEGORY” representing the pattern of COMMERCIAL UNITS and RESIDENTIAL UNITS.

Categorical features & One-hot encoding: 

Definition :


Observation :

In order to build models, we will use one-hot encoding to transform BOROUGH, BUILDING CLASS CATEGORY, TAX CLASS AT TIME OF SALE and UNIT CATEGORY.
After one-hot encoding, we have 48889 instances with 64 columns, which is a little sparse. We will first
build models and see the performance.

Numerical feature - Rescaling : 

Definition : 


Observation :

Based on the density plots and boxplots of Sale Price , Land Square Feet and
Gross Square Feet , the distribution is heavily right skewed and sparsely allocated. Hence we will perform
the log transformation on these three features.

Feature Selection

Definition : 


Observation :

The features in the datasets of interest contain information in five major categories: location, building category, tax class, time and house area. 
Further exploration on the feature selection process could be conducted on some of these categories to improve the model performance and generalization
ability. Location information is embedded in the Borough, Block, Lot, Address, Apartment Number and Zip Code features. The first three features together form the Borough-Block-Lot (BBL) address system,
while the other three together are the common mailing address. In our study, we focused on the BBL system and zip code to generate relatively broad spatial groupings. Suggestions from other 2 studies
include using longitude and latitude from the addresses to create more precise spatial scales and add functionality-related spatial categorizations before the feature selection. For time information, not only
the Sale Date, but also some indicators of economic conditions corresponding to the dates could be added to generate more interpretability to the price change. The house area category includes Total
Unit, Commercial and Residential Unit, Land Square Feet and Gross Square Feet. The commercial unit and residential unit can be further explored if we can design and apply reasonable binning and
weighting methods with relevant information from other data sources.

## Result after Data Preprocessing : 

The cleansed data now has 81030 rows and 19 columns after specific data cleaning techniques described in the above Data Preprocessing steps.


