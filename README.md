# Predicting the Mileage/Miles Per Gallon (mpg) of a car using some features of the car.

This repository contains the files of my data science and first machine learning project.The files presented above are: two csv data files that contain some technical specs of some cars,a file with the extension '.pkl' which is the final model with the best prediction accuracy,an a jupyter notebook with the '.ipynb' file extension which contains the python code for the whole project,
and the images of the charts presented in this project.

## About the dataset

The dataset is downloaded from UCI Machine Learning Repository.The link to the data is ![https://archive.ics.uci.edu/ml/datasets/auto+mpg](https://archive.ics.uci.edu/ml/datasets/auto+mpg)

### Content

* Title: Auto-Mpg Data

* Source: This dataset was taken from the StatLib library which is maintained at Carnegie Mellon University.The dataset was used in the 1983 American Statistical Association Exposition

* Relevant information: The data concerns city-fuel consumption in miles per gallon,to be predicted in terms of 3 multivariate discrete and 5 continuous attributes.The number of instances are 398 and the number of attributes are 9 including the class attribute.The attribute information are:

  1. mpg - Milieage/Miles Per Galon
  2. cylinders - the power unit of the car where gasoline is turned into power
  3. displacement - engine displacement of the car
  4. horsepower - rate of the engine performance
  5. weight - the weight of a car
  6. acceleration - the acceleration of a car
  7. model - model of the car
  8. origin - the origin of the car 
  9. car - the name of the car
  
  
  
## Insights from the dataset

Before applying a machine learning algorithm on the data to solve the problem,an Exploratory Data Analysis was made to know more about the data and below are some insights we gained from performing the analysis.

### Distributions of the variables/features.

![features distributions](https://github.com/prince381/car_mpg_predict/blob/master/cars_dist.png)

* The acceleration of the cars in the data is normally distributed and the most of the cars have an acceleration of 15 meters per second squared.
* Half of the total number of cars (51.3%) in the data have 4 cylinders.
* Our output/dependent variable (mpg) is slightly skewed to the right.

### Relationship between the Miles Per Gallon (mpg) and the other features.

![heatmap](https://github.com/prince381/car_mpg_predict/blob/master/cars_corr.png)

* We can see that there is a relationship between the mpg variable and the other variables and this satisfies the first assumption of Linear regression.
* There is a strong negative correlation between the displacement,horsepower,weight,and cylinders.This implies that,as any one of those variables increases,the mpg decreases.
* The displacement,horsepower,weight,and cylinders have a strong positive correlations between themselves and this voilates the non-multicollinearity assumption of Linear regression.Multicollinearity hinders the performance and accuracy of our regression model.To avoid this, we have to get rid of some of these variables by doing feature selection.
* The other variables.ie.acceleration,model and origin are not correlated with each other.
