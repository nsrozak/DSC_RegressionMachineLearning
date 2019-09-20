## Purpose of the Project
- Predict house sale prices using data about Washington homes and regression machine learning models
- Learning goal: prepare data for machine learning, implement machine learning algorithms in Python, and analyze their results
## Files Included
### WashingtonHouseSales-DataPreprocessing.ipynb
- Clean  data
	- Remove unnecessary columns
	- Correct misentered data
	- Correct column data types
	- Remove predictor outliers
- Prepare data for machine learning
	- Binary encoding of categorical variables
	- Split data into predictors and response
	- Normalize predictor data so all features have equal priorities
	- Split data into train, validation, and test sets
### WashingtonHouseSales-DataVisualization.ipynb
- Create boxplots for sale price grouped by each categorical variable
	- Differences in boxplots indicate differences in price correlated with different levels of a categorical variable
- Create scatterplots for sale price against each quantitative variable
	- Examine correlation between sale price and each quantitative variable
- Create time series plots for price and time data
	- Plot the first, second, and third quantiles for each year
	- Examine whether there is a trend or change in variation
### WashingtonHouseSales-KNearestNeighbors.ipynb
- Implement K Nearest Neighbors with Sci-Kit Learn package
	- Use random search and grid search to tune hyperparameters by maximizing the negative mean squared error
- Results
	- Mean Absolute Error: 131426.5878
	- Mean Squared Error: 58914690993.4774
### WashingtonHouseSales-KNearestNeighborsAnalysis.ipynb
- Create graphs showing relationship between predicted price, actual price, and absolute differences between predicted price and actual price
### WashingtonHouseSales-RandomForest.ipynb
- Implement Random Forest with Sci-Kit Learn package
	- Use random search and grid search to tune hyperparameters by maximizing the negative mean squared error
- Results
	- Mean Absolute Error: 117519.3716
	- Mean Squared Error: 44596532085.3743
### WashingtonHouseSales-RandomForestAnalysis.ipynb
- Examine feature importance
	- Important features were 'sqftAbove' and 'bathroom'
	- Unimportant features were 'location'
- Create graphs showing relationship between predicted price, actual price, and absolute differences between predicted price and actual price
### WashingtonHouseSales-SupportVectorRegression.ipynb
- Implement Support Vector Regression with Sci-Kit Learn package
	- Use random search and grid search to tune hyperparameters by maximizing the negative mean squared error
- Results
	- Mean Absolute Error: 203642.6582
	- Mean Squared Error: 142434180920.8759
### WashingtonHouseSales-SupportVectorRegressionAnalysis.ipynb
- Create graphs showing relationship between predicted price, actual price, and absolute differences between predicted price and actual price
## Conclusion
- Random Forest model is the best at predicting housing prices since it has the smallest mean absolute error and the smallest mean squared error
- Support Vector Regression is the worst at predicting housing prices since it has the largest mean absolute error and the largest mean squared error
	- Additionally, all predictions are less than $600000, so the model is not trained to recognize expensive homes
- For all models, grouping absolute prediction difference by category shows
		- Homes sold in East Urban have the greatest absolute prediction difference
		- Homes sold with a waterfront have the greatest absolute prediction difference
		- Homes sold with a view rating of 4 have the greatest absolute prediction difference
		- Homes sold with 7 bathrooms have the greatest absolute prediction difference
	- One should be wary of sale prices predicted for homes with these attributes
## Analysis
- Model may improve if more outliers are removed during data cleaning
	- The greatest differences in observed and actual prices occurred for homes selling at high prices 
- None of the models are overfitted since the models behave similarly on training, validation, and test sets
	- All features can be used since the model is not overfitted
