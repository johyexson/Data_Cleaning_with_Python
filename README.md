# Data_Cleaning_with_Python
![](Intro_Image.png)

# Data Overview
The dataset contains multiple rows and columns...
# Process
- Importing the data cleaning package and loading the dataset for wrangling and transformation 
```python
import pandas as pd
data= pd.read_csv(r'telecom_customer_churn.csv')
data.head()
```
- Checking for duplicates and removing duplicated rows from the data
```python
data.duplicated()
data.drop_duplicates(inplace= True)
data.duplicated().sum()
```
# Continuation
