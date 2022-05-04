# About the Project : 

Our team aims to predict the prices of the house listings in New York City. 
We use selected features of the close-by neighbourhoods. We will also perform regression analysis and optimise our chosen model to the best accuracy with feature selection, model tuning and other techniques. 

Our Final Resulting model will create potential benefits in multiple areas beyond price prediction as follows,

- Provides data-proven insights for individual house buyers and sellers.
- Enhances a balanced leverage between the buyers and sellers.
- Understanding the housing market in general for economics, policy makers or interested stakeholders or decision makers.

# About Dataset :

The NYC Department of Finance 1 provided the data for this study. 
The original dataset contains 167719 items of property sales data from January 2020 to December 2021 in New York City (over a two-year period). 
Each data instance includes demographics like address, region code, neighbourhood, building information like kind, number of units, building land area, and sale date. 
There are a total of 21 features (details are shown in appendix A). 
We will not investigate the impact of time on sale price in this project, hence SALE DATE will not be utilised to forecast the sale price (target variable) of a NYC property. 


# Data Preprocessing :

Definition : 

It is the process of converting raw data into an understandable format. In this step, the Quality of data is checked before applying data mining algorithms.

## Feature Selection 

Definition : 

It is used to find the best set of features for the model by reducing the input variable to your model by using only relevant data and getting rid of noise in data.

What we did? 

In this step we dropped the following columns;

Neighbourhood 
Address
Apartment numbers
Zip code
Building class at present
Building classat time of sale
Sale Date

We also dropped Easement because it only contains null values.

## Feature Engineering

Definition : 

It is a set of techniques that allows a system to automatically discover the representations needed for feature detection or classification from raw data.

## Classification :

Definition : 
It is a process of categorizing a given set of data into classes. It helps us segregate vast quantities of data into discrete values such as distinct, like 0/1, True/False, or a pre-defined output label class.

Observation :

The pattern is opaque based on the scatter plots of Commercial Units vs Sale Price and Residential Units vs Sale
Price. There are a lot of 0s and 1s in each plot. Hence we will classify them into six
groups. Here we will use a new variable “UNIT CATEGORY” representing the pattern of COMMERCIAL UNITS and RESIDENTIAL UNITS.

## Categorical features & One-hot encoding: 

Definition :

It is a process of converting categorical data variables so they can be provided to machine learning algorithms to improve predictions.
It creates a new binary feature for each possible category and assigns a value of 1 to the feature of each sample that corresponds to its original category.

Observation :

In order to build models, we will use one-hot encoding to transform BOROUGH, BUILDING CLASS CATEGORY, TAX CLASS AT TIME OF SALE and UNIT CATEGORY.
After one-hot encoding, we have 48889 instances with 64 columns, which is a little sparse. We will first
build models and see the performance.

## Numerical feature - Rescaling : 

Observation :

Based on the density plots and boxplots of Sale Price , Land Square Feet and
Gross Square Feet , the distribution is heavily right skewed and sparsely allocated. Hence we will perform
the log transformation on these three features.

## Feature Selection


Observation :

The features in the datasets of interest contain information in five major categories: location, building category, tax class, time and house area. 
Further exploration on the feature selection process could be conducted on some of these categories to improve the model performance and generalization
ability. Location information is embedded in the Borough, Block, Lot, Address, Apartment Number and Zip Code features. The first three features together form the Borough-Block-Lot (BBL) address system,
while the other three together are the common mailing address. In our study, we focused on the BBL system and zip code to generate relatively broad spatial groupings. Suggestions from other 2 studies
include using longitude and latitude from the addresses to create more precise spatial scales and add functionality-related spatial categorizations before the feature selection. For time information, not only
the Sale Date, but also some indicators of economic conditions corresponding to the dates could be added to generate more interpretability to the price change. The house area category includes Total
Unit, Commercial and Residential Unit, Land Square Feet and Gross Square Feet. The commercial unit and residential unit can be further explored if we can design and apply reasonable binning and
weighting methods with relevant information from other data sources.

# Result after Data Preprocessing : 

The cleansed data now has 81030 rows and 19 columns after specific data cleaning techniques described in the above Data Preprocessing stepS.

Exploratory Data Analysis
Target Variable[Sale Price]:

 It is observed that quite a few sale prices were absurdly small: $0 most commonly(40% of the sale price is zero). Hence, the distribution is sparse from the raw price. It is also observed that based on the information from the original resource, these sales denote the transfer of ownership from parents to the child after the parents leave home on account of retirement. Therefore, we set a reasonable range for sale price and eliminate the instances which are more than $12 million and less than $50000 since it will elimiate the special cases. Following which, we perform the log transformation. 

