# Predicting House Prices in King County

This multiple linear regression project was completed as part of Flatiron School's Data Science Bootcamp (Module 2 Final Project).

### Problem statement

As a junior data scientist at real estate company PropertiesInc., I have been tasked with investigating house sales in the King County area and building a model to predict sale price. Key executives are keen to launch an advertising campaign directed towards home owners in that area who might consider selling their house, focusing on higher-end residential properties.

Before building the model, we will address the following descriptive questions through data exploration:

Which zipcodes around King County area have the highest median house prices?

Which house features positively impact sale price?

When should one plan to market and sell?

Components

Jupyter Notebook
The Jupyter Notebook is our key deliverable and contains details of our approach and methodology, data cleaning, exploratory data analysis and model building and validation. The key models have also been saved using Pickle.

I recommend using nbviewer to view the Jupyter Notebook.

Presentation
The presentation gives a high-level overview of our approach, findings and recommendations for non-technical stakeholders. It is aimed to be between 5 and 10 minutes long.

Data
The dataset can be found in the file "kc_house_data.csv" in the Data folder, in this repository. It was originally provided in the following repository.


Technologies/ Packages

Python version: 3.6.9
Matplotlib version: 3.1.3
Seaborn version: 0.9.0
Pandas version: 0.25.1
Numpy version: 1.16.5
Statsmodels version: 0.10.1
Scikit-learn version: 0.21.2
Folium version: 0.9.1
Pickleshare version: 0.7.5

To get started

Dataset can be found in the file "kc_house_data.csv".
Check requirements in Technologies section above and download libraries if necessary.

## Conclusions

##### EDA

- Location: near the waterfront, in tier 1/2 zipcodes
- Worthwhile house features: sqft_living, grade, bedrooms, renovations since 2000
- When: prep to sell during April-July, starting marketing in Feb/March

##### Models

- Model 1 (Accuracy = .75) uses zip code tiers: 27 features, decreased RMSE of simple linear regression by 1/3 (70K)
    - suggest the waterfront is worth 234K, 2000 sqft living space is worth 153K more than 1000K, zip code tier 1 70k more than zip code tier 2 but at least double what a house in zip code tier 5 would cost
    
- Model 2 (Accuracy = 0.79) accounts for interactions: higher R^2 adjust, lowest RMSE of group
    - suggest you will start losing money if you sell in a tier 5 zipcode, 0 importance to look at lot size, just livable space, renovations add about 60k to what the house is worth, zip tier 1 is worth double of tier 3
    
- RFE good calibrating model when you have many features, but no better performance than model 1 or 2

### FUTURE WORK

- consider industries in the region and how that might increase housing value
- compare against broader region base (how does climate and presence of other land features (mountains etc. affect how valuable certain housing features are)