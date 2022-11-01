# Life-Insurance-Sales
The objective of this project is to build a model, using data that provide the optimum insurance cost for an individual. The health and habit related parameters have been used for the estimated cost of insurance.
The given data set has 1460 rows and 81 columns. Out of the 81 columns, 11 are of float data type, 26 are of int data type, 43 object data type. The train data shape is (1460,81) and test data shape is (1459,80). Sale price is the target column. 

Data preprocessing technique

The columns are having various feature types:
Categorical features:    Nominal, Ordinal
Numerical features : Continuous, Discrete

The ‘Sale price’ is the target column and its right skewed.Therefore log transformation is applied.Skewed variables are usually transformed to Box-cox transformation.The logarithmic transformation (log 1+x) is one kind of box-cox transformation where λ =0. In box-cox transformation, the unnormalized data is normalized.It fits the data along with the lambda value that was used to fit the non-normal distribution to normal distribution.
 
Categorical values are encoded using pd.get_dummies() since it gives equal weightage to all the categorical variables.Label encoder is used when the categorical variable is ordinal.

Fixing outliers in the columns —-----------------------

Converting the columns to categorical feature—-------------------
using  two functions apply(str) and astype(str).

Missing value treatment 
fillna(“None”)
fillNa(0)
Mode()[0]
Median()

