# ML_income_pred
The aim of the competition is to predict the income of people.

## Editor used
Jupyter Notebook

## Machine Learning Libraries
Sckiet Learn

### Other Major Libraries ###
* Pandas
* Numpy 
* Matplotlib.plt

## WorkFlow / Pipeline

* get the missiong values in the graph form using **missingno.matrix()**.
* Fill up the missing values with the mode of the column.
* Now the regression function cannot read in strings, so encoders were used to avoid such problems:
  * Label Encoder
  * One Hot Encoding
* Feature (Column) Selection, the features which are more corelated to the data are kept rest are dropped like **Hair Colour** is dropped.
* Column mismatching, there was column mismatch between actual test and train set, so to solve that issue both the data frame were concatinated and then one hot encoding was applied and then separated back to test and train.
* Now the actual trainig data was spit into train and testing set using **train_test_split(XTrain, YTest)**.
* Now the trainig data is to trainned using different models and fitted using **model.fit(X_train, y_train)**.
* After  training the the model will predict using **model.predict(X_test)**
* **RMSE** value is calculated using **sqrt(mean_squared_error(y_test, predictions))**.
* And then the model is run over actual test set and saved into the CSV file and then uploaded to the Kaggle.

## Model Selection

* Linear Regressoin
* Gradient Boosting Regression
* Random Forest Regressior
