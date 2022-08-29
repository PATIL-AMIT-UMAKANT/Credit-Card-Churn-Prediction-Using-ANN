# Credit-Card-Churn-Prediction-Using-ANN
![credit-card-4-e1591553820561](https://user-images.githubusercontent.com/94529852/187268665-4f857872-7d74-4a73-aed9-244f8529ed3f.jpg)

Credit card institutions use customer churning to predict who is going to stop using their credit card services. This churn metrics helps institutions improve customer retention.

This dataset consists of 10,000 customers mentioning their age, salary, marital_status, credit card limit, credit card category, etc. There are nearly 18 features.

Aknowledgement:
The original dataset can be found on this [website](https://www.kaggle.com/sakshigoyal7/credit-card-customers)

## Goal:
My goal is to predict customer churn from the dataset and gain some insights on how the bank can reduce the customers who have churned. 
___
## Table of Contents: 
1. Importing Libraries
2. Loading the Dataset
    * Load data into a Pandas DataFrame
    * Print the Datatypes of the dataset    
3. Data Cleaning
    * Remove the duplicates if any
    * Check for the null values in each column
    * Drop unnecessary columns - There are 2 columns which seem unnessary
4. Exploratory Data Analysis and Data Visualization  
    * Customer age distribution to see if customer age is normally distributed.
    * Proportion of customer gender **count** (countplot and piechart)
    * Proportion of existing and attrited customers **count**
    * Proportion of existing and attrited customers **by gender** (countplot and piechart)  
    * Proportion of entire education levels
    * Proportion of education level **by existing and attrited customer**
    * Proportion of education level **by gender** (pieplot and countplot)
    * Proportion of marital status **by attrited and existing customers** 
    * Correlation using heatmap
    * Proportion of income category
    * Proportion of income category by customer
    * Customer age count by customer
5. Customer Churn Prediction
    * Preprocessing to transform categorial to numerical to data prediction
    * Merge categorical and numerical dataframe
    * Test Train Split 
    * RandomForestClassifier
    * Model Building (du XGboost, random forest to find the best model score!
6. Conclusion
   * There are 16.07% of customers who have churned.
   * The proportion of gender count is almost equally distributed (52.9% male and 47.1%) compare to proportion of existing and attributed customer count (83.9% and 16.1%) which is highly imbalanced
   * The proportion of attrited customers by gender **there are 14.4% more male than female who have churned** 
   * **Customers who have churned are highly educated** - A high proportion of education level of attrited customer is Graduate level (29.9%), followed by Post-Graduate level (18.8%)** 
   * A high proportion of marital status of customers who have churned is Married (43.6%), followed by Single (41.1%) compared to Divorced (7.4%) and Unknown (7.9%) status  - **Marital stuats of the attributed customers are highly clustered in Married status and Single** 
   * As you can see from the proportion of income category of attrited customer, it is highly concentrated around $60K - $80K income (37.6%), followed by Less than $40K income (16.7%) compare to attrited customers with higher annual income of 80K-120K(14.9%) and over $120K + (11.5%). **I assume that customers with higher income doesn't likely to leave their credit card services than meddle-income customer** 
 
# Data problem

Credit card churning is the problem of customers rapidly opening and closing credit card accounts to use the rewards. The dataset is taken from [Kaggle](https://www.kaggle.com/sakshigoyal7/credit-card-customers), and it contains information on the credit card customers and their attrition status.

 

# Data exploration

We study the distributions of the different attributes using univariate, bivariate, and dynamic multivariate plots.

# Data preprocessing

Data was preprocessed first by studying the correlation matrix to discard features that were perfectly correlated, and then by performing one hot encoding for the categorical features and normalizing the numerical features.


The following models were compared: K-Nearest Neighbors, XGBoost, Logistic Regression, and Random Forest. The hyperparameters of each model were tuned using grid search and random search on the evaluation metric roc_auc, and the models were trained with the optimized hyperparameters.

# Predictions

The models were compared on the basis of metrics like roc_auc, F1 score, and accuracy. XGBoost and Random Forest were found to be the best models.
