 Ex-01_DS_Data_Cleansing
# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Get the information about the data

## STEP 3
Remove the null values from the data

## STEP 4
Save the Clean data to the file

# CODE

import pandas as pd
df=pd.read_csv("/content/Loan_data.csv")
print(df)

df.head(5)

df.tail(5)

df.describe()

df.info()

df.isnull().sum()

df=df[~df.duplicated()]
print(df)

df['Gender'].fillna(value=df['Gender'].mode())

df['LoanAmount'].fillna(value=df['LoanAmount'].median())

# OUPUT

![data](https://user-images.githubusercontent.com/119560261/226187863-94cfbdeb-376c-424a-b36b-586c0c478da8.png)
![head](https://user-images.githubusercontent.com/119560261/226187877-f07de2e2-99d1-4281-ad5a-3bb2cea75e31.png)
![describe and info](https://user-images.githubusercontent.com/119560261/226187946-6904911a-6d6a-429d-950b-dfaed2880919.png)
![isnull](https://user-images.githubusercontent.com/119560261/226187969-2fffdc98-2fab-4231-ad46-474c90c87717.png)
![mean](https://user-images.githubusercontent.com/119560261/226187974-66112e8e-a774-4230-87fe-bce5b8526122.png)
