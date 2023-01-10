# Life-Insurance-Sales
The objective of this project is to build a model, using data that provide the optimum insurance cost for an individual. The health and habit related parameters have been used for the estimated cost of insurance.
The given data set has 1460 rows and 81 columns. Out of the 81 columns, 11 are of float data type, 26 are of int data type, 43 object data type. The train data shape is (1460,81) and test data shape is (1459,80). Sale price is the target column. 

Data preprocessing technique

The columns are having various feature types:
Categorical features:    Nominal(has no rank), Ordinal(has an order rank)
Numerical features : Continuous, Discrete

The ‘Sale price’ is the target column and its right skewed.Therefore log transformation is applied(log 1+x).Skewed variables are usually transformed to Box-cox transformation.The logarithmic transformation (log 1+x) is one kind of box-cox transformation where λ =0. In box-cox transformation, the unnormalized data is normalized.It fits the data along with the lambda value that was used to fit the non-normal distribution to normal distribution.
 
 
 
Categorical values are encoded using pd.get_dummies() since it gives equal weightage to all the categorical variables.Label encoder is used when the categorical variable is ordinal.

Fixing outliers in the 8 columns in the given dataset
OverallQuad,LotFrontage,GrLiveArea,GarageArea,LotArea,YearBuilt,TotalBsmtSF,1stFlrSF

Converting the columns to categorical feature MSsubclass,Mosold,YrSold
using  two functions apply(str) and astype(str).
Some non-numeric predictors are stored as numbers. We have to convert them to string.Here in this project, we convert
MsSubClass- apply (Str): The apply() gets the result faster than astype() 
YrSold- astype(Str)
MoSold(Str)


Missing value treatment 
fillna(“None”)
fillna replaces NULL values with specified value.Inplace = True so that original dataframe gets changed.Otherwise the inplace function returns a new dataframe object  
fillNa(0)- Quality of basement finished area 
fillna.mode(0)- Saletype
Median()-LotFrontage

