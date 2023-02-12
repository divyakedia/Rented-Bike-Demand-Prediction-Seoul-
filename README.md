# Rented-Bike-Demand-Prediction-Seoul-
## Project Summary

Bike sharing provides both locals and tourists an easy, low-cost, efficient means of transportation around cities. Users are able to pick up bicycles around the city from multiple bike stations.Bike sharing is striving to become a valid, reliable, and easy form of public transportation.
The low cost of bike sharing is also appealing to locals and tourists alike. 
Data used include Seoul Bike and Capital Bikeshare program data. Data have weather data associated with it for each hour.we have first started with the step knowing your data which includes loading dataset, null/missing value count etc then the next step was to know the variables , after this cleaning the data or data wrangling was done. After this we have done EDA for the project.After  we have done hypothesis testing followed by Data preprocessing and then MAchine learning model implementation .For the dataset, we are using linear regression model were train with optimize hyperparameters using a repeated cross validation approach and testing set is used for evaluation. Multiple evaluation indices such as R2 , Root Mean Square error are use to measure the prediction performance of the regression models. The performance of the model is vary with the time interval used in transforming data.

## Problem Statement
Currently Rental bikes are introduced in many urban cities for the enhancement of mobility comfort. It is important to make the rental bike available and accessible to the public at the right time as it lessens the waiting time. Eventually, providing the city with a stable supply of rental bikes becomes a major concern. The crucial part is the prediction of bike count required at each hour for the stable supply of rental bikes.

## Approach
- Understanding Business problem
- Data collection & Preprocessing
  - Data cleaning
  - Missing Data Handling
- Exploratory Data Analysis
  - Understanding categorical and numerical features
  - EDA conclusion
- Data manipulation
  - Feature Engineering
  - Outlier Detection & Treatment
  - Feature scaling
  - Categorical Data encoding
- Modelling
  - Train Test split
  - Fitting models to a Data
  - Hyperparameter Tuning
- Model Performance & Evaluation
  - Visualizing Model Performance
  - Base models v/s Tuned models
- Conclusion and Recommendations

## Data insights
1. People prefer rented bikes when temperature is high and humidity is low.
2. During holidays the demand for rented bikes is less compared to when there are no holidays.
3. People like to take rented bikes when rainfall and snowfall are low.
4. The demand is high in the morning and even higher in the evening which shows employees mostly prefer rented bikes before and after their working hours.
5. The demand is high in the month of June followed by July and May whereas the demand is lowest in the month of December, January and February.

# Model applied and Observations:
## For Test Set
|Model|	MAE	|MSE	|RMSE|	R2_score	|Adjusted R2|
|-----|-----|-----|----|------------|-----------|
|0. Linear regression|	4.382|	32.376|	5.690|	0.790	|0.79|
|1.Ridge regression	|4.382 |32.376	|5.690|	0.790|	0.79|
|2. Lasso regression|	7.504	|93.998	|9.695|	0.391|	0.38|
|3.	Elastic net regression|	5.589	|53.008|	7.281|	0.657	|0.65|
|4.	Dicision tree regression|	4.189|	34.665|	5.888|	0.775|	0.77|
|5.	Decision Tree gridsearchcv	|3.522	|22.899|	4.785|	0.852|	0.85|
|6.	Random forest regression	|0.906	|1.937|	1.392	|0.987	|0.99|
|7.	Random Forest gridsearchcv	|0.899	|1.855|	1.362|	0.988|	0.99|
|8.	Gradient boosting regression	|2.874|	15.696|	3.962|	0.898|	0.90|
|9.	Gradient Boosting gridsearchcv	|1.911|	7.768|	2.787|	0.950|	0.95|
## For Training Set
|Model|	MAE	|MSE	|RMSE|	R2_score	|Adjusted R2|
|-----|-----|-----|----|------------|-----------|
| 0	Linear regression	|4.323	|31.821	|5.641	|0.792|	0.79|
|1.	Ridge regression|	4.323|	31.817	|5.641|	0.792|	0.79|
|2.	Lasso regression	|7.435|	93.716|	9.681|	0.389	|0.37|
|3.	Elastic net regression Test	|5.506|	52.741|	7.262|	0.656|	0.65|
|4.	Dicision tree regression|	4.693|	43.774|	6.616|	0.714|	0.71|
| 5.	Decision Tree gridsearchcv|	3.902|	29.291|	5.412|	0.809|	0.80|
|6.	Random forest regression|	2.426	|12.996|	3.605|	0.915|	0.91|
|7.	Random Forest gridsearchcv|	2.416|	12.895|	3.591|	0.916|	0.91|
|8.	Gradient boosting regression|	3.055	|17.266|	4.155|	0.887|	0.88|
|9.	Gradient boosting Gridsearch CV	|3.055|	17.266|	4.155|	0.887|	0.88|

# Conclusion
- Random forest Regressor and Gradient Boosting  gives the highest R2 score of 99% and 90% respectively for Train Set and 91% and 88% for Test set.
-  After using hyperparameter tuning by GridSearchCV Random forest Regressor and Gradient Boosting gives highest R2 score of 99% and 95% respectively for Train set and 91% and 88% for Test set.
-  No overfitting is seen.
-  Feature Importance value for Random Forest and Gradient Boost are different.
- We can deploy this model.
