![image](https://user-images.githubusercontent.com/36938994/62065746-a2f02480-b1fd-11e9-86a7-a161981c8377.png)


## Predicting Facade Risk with Deep Learning
The objective of this project is to create a risk probability rating for all buildings in the Façade Inspection Safety Program at the DOB. The results will be used to better inform proactive enforcement actions for high-risk facades. A façade is considered high risk when it is likely to fail causing property damage, injury or death.

The outcome variable is “unsafe” and is constructed from various DOB violation datasets. The predictors (independent variables) incorporate both behavioral and physical building characteristics. Behavioral predictors include building owner, façade inspectors and ownership type. Building characteristics include age, number of stories, square footage and building type.

### Deep Learning Algorithm
•	To obtain optimal results, the data should be of the same type. All variables were therefore converted into categories and then into dummy variables.

•	The data was partitioned into training, validation and holdout datasets.

•	Hyper-parameter tuning was used on the training and validation datasets to optimize model performance.

•	The final model was tested using the holdout dataset.

•	Using the final model, a probability of high risk was assigned to each building in the façade compliance universe.

### Results
•	There were 4515 total predicted high-risk facades

•	The model predicted 2155 additional high-risk facades that are not part of the known high-risk universe

### Independent variables considered to be highly correlated with a high-risk façade:
•	Ownership type = City Owned

•	Building Owner = Fred Camerata, Jacob Weinreb, etc.

•	Year Built = 1916 – 1937

•	Building Area = 250,000 to 1,000,000 square feet

•	Community Board = CB 103, CB 111, CB 107

### Some Buildings Predicted to be High Risk

![59791541-5b8e8400-92a0-11e9-8207-fff25ded3920](https://user-images.githubusercontent.com/36938994/60740994-e1176280-9f35-11e9-9ea5-94878159f419.png)

![59791654-98f31180-92a0-11e9-9ba4-f2d67426f5c7](https://user-images.githubusercontent.com/36938994/60741016-f1c7d880-9f35-11e9-827d-ce85b67195a6.png)

![59791859-f6875e00-92a0-11e9-867e-9f8e05e6abc6](https://user-images.githubusercontent.com/36938994/60741031-0015f480-9f36-11e9-99ea-f5a3f2d63478.png)


### MAP

![59791981-3a7a6300-92a1-11e9-90d9-7dd1fd2e8dd1](https://user-images.githubusercontent.com/36938994/60741065-19b73c00-9f36-11e9-9964-5c0c8447db7b.png)

![map with label](https://user-images.githubusercontent.com/36938994/60741123-52571580-9f36-11e9-8966-43036bb3cf7d.png)


The map above demonstarte a NYC community districts and associated facade violation(count) in each districts. We can see from the map that mostly Downtwon and Midtown Manhatttan has more high risk buildings with facade violation.This simple map was built using geopandas and mapclassify in python. 

### Dashboard and Map on ArcGis

![image](https://user-images.githubusercontent.com/36938994/119533547-f416c400-bd53-11eb-8dfa-872c08a3b1b8.png)

This is a facade violation dashbaord which shows the number of high risk buildings in New York city by  Community board, it highlghts the CB into a polygon shape feature layer by coloring them from deep to light representing high risk CB. The high risk buildings has been chosen according to their predicted confidence score after the modeling process.Confidence score of higher than 70-80% is placed into the high risk category for outcome violation "Yes". On the left side we have some attributes added into the dashboard such as buildings stories, area and year built as well as the pie chart on the top to understand what perecenatge of the high risk buildings falls into which categories. 


![image](https://user-images.githubusercontent.com/36938994/119535094-aac77400-bd55-11eb-8365-bb471fae0fef.png)

Another fetaure of this Map is, as we zoomed into a certain level we can have a full information on the stats of each individual buildings. The points on the map represents each buildings. This is the second feature layer used in this Map which is in point geometrical shape. 
 
