# Rain-_Predictor

## Problem Statement
### Read the Australian weather dataset and analyze the various parameters to predict the probability of rainfall. Use different models for the same and compare the accuracy and error rate of these models.

## Variables
## We analysed a dataset that has the following weather details about Australia.
###  Date - date of the observation
### Location - name of the Australian city
### MinTemp - the minimum temperature on that day
### MaxTemp - the maximum temperature on that day
###  Rainfall  - the rainfall on that day
### Evaporation - amount of water that evaporates 
### Sunshine - amount of sunshine available during that day
### WindGustDir -  direction of increase of the speed of wind
### WindGustSpeed - increase in the speed of wind
### WindDir9am - the direction of wind at 9am 
### WindDir3pm - the direction of wind at 3pm
### WindSpeed9am - the speed of wind at 9am
### WindSpeed3pm - the speed of wind at 3pm- 
### Humidity9am - the amount of humidity in the air at 9am
### Humidity3pm - the amount of humidity in the air at 3pm
### Pressure9am - the pressure at 9am
### Pressure3pm - the pressure at 3pm
### Cloud9am - number of clouds in the air at 9am
### Cloud3pm - number of clouds in the air at 3pm
### Temp9am - temperature at 9am
### Temp3pm - temperature at 3pm
### RainToday - a Boolean variable that signifies whether it rained today or not
### RainTomorrow - - a Boolean variable that signifies whether it will rain tomorrow or not

## Process
### Initially, we load the dataset into a dataframe using pandas.
### We scan for the presence of null values as a part of data pre-processing.
### We encode the attribute ‘Location’ and create a timestamp for the variable ‘Date’
### For the rest of the columns where we have null values, we replace them with the mode of that column.
### We then plot a heatmap using the seaborn library to visualize the correlation of variables.
### Since we must predict rainfall, we choose the ‘RainTomorrow’ feature as the target variable and the rest of them as the independent variables.
### Next, we split the independent and dependent variables into training and testing data using train_test_split.
### Normalization is done using StandardScalar.
### Then we used three algorithms- Logistic Regression, Decision Tree, and Random Forest Classifier to predict the rainfall.
### We calculate the confusion matrix for each algorithm and the related terms likeprecision, accuracy, error rate and recall.
### We evaluate the model for each algorithm for the training as well as testing set.
### Lastly, we compare the accuracy and error rates of all three to arrive at proper conclusions.

## Results
### We received the following values for accuracy after training the dataset for all three algorithms
### 83.77% - Logistic Regression
### 78.70% - Decision Tree
### 84.28% - Random Forest Classifier
### The Root Mean Squared Error value for the three algorithms is
### 0.40 - Logistic Regression
### 0.46 - Decision Tree
### 0.39 - Random Forest Classifier

## Conclusion
### We obtain the highest accuracy with the help of Random Forest Classifier i.e. 84.29%.
### The least error (all three types) is found in Random Forest Classifier, thus making it more accurate and precise.
### This is possible because random forest collects the data of each tree and forecasts the future based on the majority of predictions, rather than relying on a single decision tree.
