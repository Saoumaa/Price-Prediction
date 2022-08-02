# Paris House Price Prediction

This is a regression problem. The price of houses in paris are breing predicted with the use of machine learning algorithms. 
The dataset used is gotten from kaggle.com, it is titled Paris House Pricing.

## Importing Libraries
The first thing done is to import the necessary libraries needed to perform  regression analysis.
The imported librarioes include:
1. Pandas 
2. matplotlib.pyplot
3. numpy
4. seaborn 
5. sklearn and all needed functions in it.
6. catboostregrssor for performing regression analysis.

## Reading the dataset

The data set has 10000 rows and 17 columns including the price, and all the features numerical features.
The data is cleaned and properly distributed. It has no null cell in it.

## Exploratory Data Analysis (EDA)

Histogram plots were made to visualize the data.
Boxplots were made with seaborn to check for outliers, and from what was mentioned earlier, the dataset is cleaned, distributed (not skewed) and has no outlier in it.
The boxplots also shows that.
### Checkiong for corelation

using pandas attributes ,the correlation of the data was checked, the other features of the data were compared to the price of the houses to see how correlated they are. Among all the features of the data, only 'squareMeters' column is mostly correlated with the price. 
Looking at this result, the predictive model that is to be built might not perform excellently, hence it is suggested to perform Feature Engineering , where more features will be added to the data.

### Feature Engineering

The result of feature engneering include the following features: roomSizes, avgFloorSizes , garageSizes, livingRoomsm, prevOwnerSizes, pricePerSquaremeter, garagePrice, cityPartPrice. what brought about all this new features is the consideraton of the worth of some features of the house. 
With these new added features, there are more features correlating with the price.
All the previous features that aren't correlating with the data are removed.

## Preprocessing 

Since the data only comntains numerical data, the preprocessing needed is to standardize the data, and this was done using sklearn standardizing function.

After the features have been standardized, the data was splitted into training, validation and testing sets.
Now the last thing needed to be done is creating a model.

## Modeling

### LinearRegression. 
With linear regression, an accuracy of 99.9999455 accuracy was achieved. Corss validation was used to try improve it, but there wasn't any significant improvement.

### RandomForestRegressor

with the use of RandomForestRegressor, an accuracy of 99.99983% was achieved. Cross validation didn't bring any significant change to the model performance.

### Gradient Boosting
Gboosting achieved an accuracy of 99.999%, and cross validation couldn't improve it also.

Upon the usage of several regression models, The best model remains Linear Regression.
Now the price of houses can be predicted with a very good model.
