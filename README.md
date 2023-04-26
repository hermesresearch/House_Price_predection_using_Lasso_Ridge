Housing Price Prediction using Ridge and Lasso Regression
Problem Statement:
Surprise Housing, a US-based housing company, wants to enter the Australian market. The company aims to use data analytics to purchase houses below their actual values and sell them at a higher price. They have collected a dataset from the sale of houses in Australia and want to build a regression model using regularization to predict the actual value of prospective properties. The company wants to know the significant variables in predicting house prices and how well those variables describe house prices. They also want to determine the optimal value of lambda for ridge and lasso regression.

Approach Taken:

* Read and understand the data, perform basic data cleanup.
* Check for missing values and impute them using business logic.
* Change data types of variables.
* Perform exploratory data analysis using SweetViz for auto EDA and correlation heatmap for univariate and bivariate analysis.
* Prepare the data for model building by performing log transformation of the target variable, train-test split, statistical imputation of missing values, encoding categorical * features, robust scaling of numerical features using median and quantile values, and variance thresholding to exclude features with almost zero variance.
* Build Ridge regression model with GridSearchCV to find the optimal value of alpha, and identify the top 25 features based on beta coefficient values.
* Build Lasso regression model with GridSearchCV to find the optimal value of alpha. Lasso eliminated 110 features (including dummy variables) and identified the top 25 * * * *  features based on beta coefficient values.
* Evaluate both models on training and test datasets.
* Choose the Lasso regression model as the final model since it has a similar r2 score and MAE on the test dataset as the Ridge model but eliminates 110 features, making it simpler.
Observations:

Both the Ridge and Lasso models have almost the same test and train accuracy, indicating no overfitting.
Lasso and Ridge both have similar r2 score and MAE on the test dataset. However, the Lasso model is simpler than the Ridge model since it eliminates 110 features, with a final number of features of 116 compared to Ridge's 226 features.
Lasso Regression model on the test dataset: r2 score= 0.8947, MAE= 0.0914, RMSE= 0.1335
Considering the above points, we can choose the Lasso Regression model as the final model.