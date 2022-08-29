# Credit-Card-Churn-Prediction-Using-ANN


# Data problem

Credit card churning is the problem of customers rapidly opening and closing credit card accounts to use the rewards. The dataset is taken from [Kaggle](https://www.kaggle.com/sakshigoyal7/credit-card-customers), and it contains information on the credit card customers and their attrition status.

# Data exploration

We study the distributions of the different attributes using univariate, bivariate, and dynamic multivariate plots.

# Data preprocessing

Data was preprocessed first by studying the correlation matrix to discard features that were perfectly correlated, and then by performing one hot encoding for the categorical features and normalizing the numerical features.

# Data analysis

The following models were compared: K-Nearest Neighbors, XGBoost, Logistic Regression, and Random Forest. The hyperparameters of each model were tuned using grid search and random search on the evaluation metric roc_auc, and the models were trained with the optimized hyperparameters.

# Predictions

The models were compared on the basis of metrics like roc_auc, F1 score, and accuracy. XGBoost and Random Forest were found to be the best models.
