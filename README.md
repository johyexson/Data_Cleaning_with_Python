# Data_Cleaning_with_Python
![](Intro_Image.png)

# Data Source
The data was gotten from Maven Analytics Data Playground. The customer churn data includes details about customer demographics, location, services and current status. It consists of multiple tables, 7043 records and 34 fields stored in a csv file. [Link](https://mavenanalytics.io/data-playground?search=customer%20churn)
# Process
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
