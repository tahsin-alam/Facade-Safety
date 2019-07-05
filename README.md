## NYC-DOB

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


