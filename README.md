# Airline-Price-Prediction

1) importing libraries and dataset
2) dropping rows with missing values (since there were only 2/10683)
3) since ML model understands only integer values therefore coverting columns with datatype object into integers
  a) from journey date-date,day of month was extracted 
  b) arrival,departure time was converted to datetime stamp and hour,min was extracted
  c) the other columns with object datatype were considered as categorical data & dealt using onehotencoder & labelencoder
4) Outliers were detected using boxplot & distribution plot and replaced by median
5) dependent variables were put in x and target variable (price) in y
6) feature selection was done and column with 0 importance was dropped from x dataframe
7) dataset was split into 80%, 20% train and test set respectively
8) function was written to pass with different models and print their r^2, mae, mse, rmse
9) On comparing r^2 of various models random forest gave max accuracy of 81%
10) cross validation was then performed using randomized search and model was refitted with best paramters
11) final accuracy achieved after performing cross validation was 86%
