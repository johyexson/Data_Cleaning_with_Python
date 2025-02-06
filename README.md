# Customer_Segmentation_Using_Python
![](Intro_Image.png)
# Table of Contents
- [Case Study](#case-study)
- [Data Source](#data-source)
- [Method of Analysis](#method-of-analysis)
- [Code](#code)
- [Findings and Recommendations](#findings-and-recommendations)

# Case Study
Customer segmentation in order to classify customer based on demographics, purchasing behaviour and other characteristics.
# Data Source
The data was gotten from Maven Analytics Data Playground.[Link](https://mavenanalytics.io/data-playground?search=customer%20churn)
# Method of Analysis 
- Importing the data cleaning package and loading the dataset for wrangling and transformation 
```python
import pandas as pd
data= pd.read_csv(r'telecom_customer_churn.csv')
data.head()
```
- Checking information about data to examine its structure, characteristics and other information 
```python
data.info()
data.describe()
data.count()
```
- Checking for duplicates and removing duplicated rows from the data
```python
data.duplicated()
data.drop_duplicates(inplace= True)
data.duplicated().sum()
```
- Removing columns that are irrelevant to the data
```python
data.columns
data.drop(columns= ["Latitude", "Longitude"], inplace = True)
```
- Checking for columns with null values and filling them with data
```python
data.isnull().sum()
data.fillna(['Not Applicable'], inplace= True)
```
- Converting data types in multiple columns to ensure consistency in data formats
```python
data.dtypes
data= data.astype({' Dependents': 'int','Zip_Code': 'int','Referrals': 'int','Tenure': 'int','Avg_Monthly_Long_Distance_Charges': 'int','Avg_Monthly_GB Download': 'int','Monthly_Charge': 'int','Total_Charges': 'int','Total_Refunds': 'int','Total_Extra_Data_Charges': 'int','Total_Long_Distance_Charges': 'int','Total_Revenue': 'int'})
```
# Code
You can view the full code [here](Data_Cleaning_with_Python.ipynb)
