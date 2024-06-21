Objective:

Telecom Churn Case Study
With 21 predictor variables we need to predict whether a particular customer will switch to another telecom provider or not.
In telecom terminology, this is referred to as churning and not churning, respectively.


Step 1: Importing and Merging Data
importing libraries and data here we have merged three dataset 
Churn.csv
Internet.csv
customer.csv
Step 2: Inspecting the Dataframe
Checking the shape of the data frame and looking for statistical aspects using info() method and describe() method

Step 3: Data Preparation
Dropping the repeated variables
Checking for Missing Values and Inputting Them
Variables creating dummy variables for the remaining categorical variables


Step 4: Test-Train Split
The dataset is split as train and test set using train_test_split method from sklearn library the split is done  between 80% train and 20% test set

Step 5: Feature Scaling
the feature scaling is done using standard scaler for continuous numeric variables

Step 6: Looking at Correlations
Dropping highly correlated dummy variables

Step 7: Model Building
using RFE feature selection we have selected important variables for the model 
Vif method to check the collinearity for the variables 
We have build four models based on below given algorithm 
Logistic Regression
Random Forest Classification 
Decision Tree Classification 
SVM 

Step 8: Model Selection   


Based on the accuracy score and confusion matrix of all the four models the test data accuracy on the Logistic Regression Model is slightly higher 
which is 80%.Since the dataset is unbalanced we can use f1_score to see predictability of both the classes hence
the objective of the problem is to accurately find churn customers the f1_score for churn in logistic regression model is 59% which is higher compared to other models.
We can  select the Logistic Regression model for prediction on unseen data. 
