# Project 2 - Ames Housing Data and Kaggle Challenge

## Problem Statement
We are a group of home improvement consultants that provide suggestions on how to refurbish the houses in selected neighborhoods in Ames, Iowa, including selecting the best features for homeowners to renovate, in order to improve the value of their homes in a cost-effective way.

Based on the provided data, we will:
- build several multiple linear regression models and select one best-performing model as our production model
- based on our production model, explore and recommend important features for home improvment
- build models for selected neighorboods, explore and recommend important features for home improvment

## Background
House value are influented by the following factors:([*source*](https://www.opendoor.com/w/blog/factors-that-influence-home-value))
- Neighborhood comps
- Location
- Home size and usable space
- Age and condition
- Upgrades and updates
- The local market
- Economic indicators
- Interest rates

As home improvement consultants, we are more interested at the factors or features which can be improved on the exsiting houses. 

## Dataset and Data Directory
- The dataset  ([*source*](https://www.kaggle.com/competitions/dsi-us-11-project-2-regression-challenge/data)) contains information from the Ames Assessor’s Office used in computing assessed values for individual residential properties sold in Ames, IA from 2006 to 2010.
- The Dataset has 82 columns which include 23 nominal, 23 ordinal, 14 discrete, and 20 continuous variables (and 2 additional observation identifiers). ([*source*](http://jse.amstat.org/v19n3/decock/DataDocumentation.txt))
- Some important features are listed as below 


|Feature|Type|Description|
|---|---|---|
|**SalePrice**|*Continuous*|sale price, we will treat it as house value| 
|**Neighborhood**|*nominal*|Physical locations within Ames city limits|
|**Overall Qual**|*ordinal*|Rates the overall material and finish of the house|
|**Year Built**|*Discrete*|Original construction date|
|**Mas Vnr Type**|*nominal*|Masonry veneer type|
|**Mas Vnr Area**|*Continuous*|PMasonry veneer area in square feet|
|**Foundation**|*Nominal*| Rating of basement finished area|
|**BsmtFin Type 1**|*Ordinal*|sale price| 
|**BsmtFin SF 1**|*Continuous*|Type 1 finished square feet|
|**Total Bsmt SF**|*Continuous*|Total square feet of basement area|
|**Gr Liv Area**|*Continuous*|Above grade (ground) living area square feet|
|**Fireplaces**|*Discrete*|Number of fireplaces|
|**Garage Area**|*Continuous*|Size of garage in square feet|
|**Open Porch SF**|*Continuous*| Open porch area in square feet|
|**HeatingQC**|*Ordinal*|Heating quality and condition|
|**Bedroom**|*Discrete*|Bedrooms above grade (does NOT include basement bedrooms)|
|**Kitchen**|*Discrete*|Kitchens above grade|
|**KitchenQual**|*Ordinal*|Kitchen quality|
|**TotRmsAbvGrd**|*Discrete*|Total rooms above grade (does not include bathrooms)|

## Conclusions and Recommendations
- We built several models and found lasso models has the best performance
- Based on the lasso model, we analyzed and found ' BsmtFin SF 1' and 'Fireplaces' as recommended features for home improvements
- We built models for some neighborhoods and recommended some feature for home improvement
- The neighorhood models also suggest that it is better to do home improvement for newer houses or high value houses because it can create more value
## Limitation and Future Enhancement
- Our multiple regression models cannot meet the LINE assumption, other non-regression models should be considered
- Many data are highly imbalance and barely useful. Data collector might redesign what to be collected in the future
- Many neigbhorhoods have insufficient data to build meaningful models. More data is needed
