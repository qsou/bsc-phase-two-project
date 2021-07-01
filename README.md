# Housing Price Analysis

## Authors:
Bobby Oliver and Qiwen Ou

## Overview

This project will analyze how different variables affect housing prices. The dataset we used is from Kaggle and contains information about House Sales in King County, USA. The data shows the end sale price of each house and the different features each of them possesses. From these known features we used different statistical tools to come up with a model that could predict the sale price of the house.

## Business Problem

A Seattle real estate firm noticed there are no tools that allow their clients to enter information about their home and receive a prediction for their home's sale price. So, the real estate firm has hired us to produce a predictive model that can predict the sale price of a home in King County, Washington as accurately as possible.

## Data

We got this data from Kaggle, which they source from this specific website https://gis-kingcounty.opendata.arcgis.com/datasets/zipcodes-for-king-county-and-surrounding-area-shorelines-zipcode-shore-area/explore?location=47.505673%2C-121.477600%2C8.99. We also used this other specific website https://geodacenter.github.io/data-and-lab//KingCounty-HouseSales2015/ to learn what each feature means from the dataset. There were 21 feature columns and 21597 rows of house sales in the database. 

## Methods

To model our data, we examined the correlations between the price of the house and the other variables. From the 21 original variables down to price, sq ft living area, house age, bedrooms, bathrooms, floors, waterfront, condition, sq ft above, latitude, average neighborhood house size, and grade(construction quality of house). We then one hot encoded grade because we believed it was categorical data and then sorted it into 5 categories as we thought some of the original 13 grades were extremely similar to each other. We next created a function that created a linear regression model using split (75/25) training and testing data based on the data frame that was input into it, along with printing a graph that showed in what price ranges the most error occurred. After we ran the first data frame through the function, we then made a data frame where outliers are eliminated. This reduces the root mean squared error, by logging the price and then dropping any house that fell outside of 3 standard deviations. Lastly, we one hot encoded zip code and concatenated it to our second data frame, which we ended up running through the function.

## Results

After running our models, we were able to see a gradual improvement, leading to the changes made to the next iteration. All of our models gave us relatively similar testing and training root mean squared errors (equivalent to dollars off-target), meaning that our test was not over or under-fit. The first model gave us a testing root mean squared error(RMSE) of $208,440.52. Then the second gave us $165,753.05 and lastly it gave us $124,774.52. These numbers show clear improvement between models and how impactful the changes were. One thing to note was that while our RMSE was in the hundreds of thousands, the main cause of that stemmed from houses costing 1 to 1.1 million and above, with most of the lower costing houses sitting well below $50,000 for the final model.

## Conclusion and Future Improvements

After analyzing and experimenting with different variables, our final model shows that if your house price is roughly below 1.1 million, the model should accurately predict your house price with 50 thousand of the actual price. We would highly recommend our model for lower-range houses and not to people who have expensive homes. The reason being our model significantly undervalues the most expensive houses. Some of our Future improvements are to create more advanced predictive models and identify variables that impact the priciest homes. 

## For More Information

Please review our Jupyter Notebook or our presentation. For any additional questions, please contact Bobby Oliver at robertoliver2000@gmail.com and Qiwen Ou at Qiwen.ou0721@gmail.com.