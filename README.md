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
	- Use random search and grid search to tune hyperparameters
		- Maximize the negative mean squared error
- Results
	- Mean Absolute Error: 131426.5878
	- Mean Squared Error: 58914690993.4774
### WashingtonHouseSales-KNearestNeighborsAnalysis.ipynb
- Create graphs analyzing predicted price and actual price, and the absolute value of differences in predicted price and actual price
	- Shows predicted price and actual price have a fairly linear relationship
	- Shows some large absolute differences in prediction occur at all price levels, but the largest difference occurs at the highest price
		- Homes sold in Seattle and East Urban have the largest absolute prediction difference
		- Homes sold with a waterfront have the largest absolute prediction difference
		- Homes sold with a view rating of 4 have the largest absolute prediction difference
		- Homes sold with a condition rating of 5 have the largest absolute prediction difference
		- Homes sold with 7 bedrooms have the largest absolute prediction difference
### WashingtonHouseSales-RandomForest.ipynb
- Implement Random Forest with Sci-Kit Learn package
	- Use random search and grid search to tune hyperparameters
		- Maximize the negative mean squared error
- Results
	- Mean Absolute Error: 117519.3716
	- Mean Squared Error: 44596532085.3743
### WashingtonHouseSales-RandomForestAnalysis.ipynb
- Examine feature importance
	- Important features were 'sqftAbove' and 'bathroom'
	- Unimportant features were 'location'
- Create graphs analyzing predicted price and actual price, and the absolute value of differences in predicted price and actual price
	- Shows predicted price and actual price have a fairly linear relationship
	- Shows some large absolute differences in prediction occur at all price levels, but the largest difference occurs at the highest price
		- Homes sold in East Urban and Seattle have the largest absolute prediction differences
		- Homes sold with a waterfront have the largest absolute prediction differences
		- Homes sold with a view rating of 3 have the largest absolute prediction differences
		- Homes sold with a condition rating of 5 have the largest absolute prediction differences
		- Homes sold with 7 bedrooms have the largest absolute prediction differences
		- Homes sold with 4.25 bathrooms have the largest absolute prediction differences
### WashingtonHouseSales-SupportVectorRegression.ipynb
- Implement Support Vector Regression with Sci-Kit Learn package
	- Use random search and grid search to tune hyperparameters
		- Maximize the negative mean squared error
- Results
	- Mean Absolute Error: 203642.6582
	- Mean Squared Error: 142434180920.8759
### WashingtonHouseSales-SupportVectorRegressionAnalysis.ipynb
- Create graphs analyzing predicted price and actual price, and the absolute value of differences in predicted price and actual price
	- Shows predicted price and actual price are broken into two groups
		- The first group has predictions of less than $400000
		- The second group has predictions of $450000 to $600000
		- Both show a positive relationship, but both underestimate the sale price of homes
		- All predictions are less than $600000
	- Shows absolute differences in prediction initially decrease, and increase linearly for sale prices greater than $500000
		- Homes sold in East Urban have the greatest absolute prediction difference
		- Homes sold with a waterfront have the greatest absolute prediction difference
		- Homes sold with a view rating of 4 have the greatest absolute prediction difference
		- Homes sold with condition ratings of 5 have the greatest absolute prediction difference
		- Homes sold with 2.5 floors have the greatest absolute prediction difference
		- Homes sold with 7 bedrooms have the greatest absolute prediction difference
		- Homes sold with 4.75 bathrooms have the greatest absolute prediction difference
