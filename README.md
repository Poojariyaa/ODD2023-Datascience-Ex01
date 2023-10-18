# Ex-01_DS_Data_Cleaning

# AIM
 To read the given data and perform data cleaning and save the cleaned data to a file.

 # Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

 # ALGORITHM
  ### STEP 1: Read the given Data
  ### STEP 2: Get the information about the data
  ### STEP 3: Remove the null values from the data
  ### STEP 4: Save the Clean data to the file

# CODE and OUTPUT

## DATA SET:
~~~
import pandas as pd
df=pd.read_csv("Data_set.csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna (df['aired_on'].mode()[0])
df['original_network']=df[ 'original_network'].fillna (df['aired_on'].mode()[0])
df.head()
df['rating']=df['rating'].fillna (df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
df['watchers']=df['watchers'].fillna (df['watchers'].median())
df.head()
df.info()
df.isnull().sum()
~~~

## LOAN DATA:
~~~
import pandas as pd
df=pd.read_csv("Loan_data.csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
df['Loan_ID']=df['Loan_ID'].fillna(df['LoanAmount'].mode()[0])
df.head()
df['Dependents']=df['Dependents'].fillna (df['Dependents'].mode()[0])
df.head()
df['Gender']=df['Gender'].fillna (df['Gender'].mode()[0])
df.head()
df['Education']=df['Education'].fillna (df['Dependents'].mode()[0])
df.head()
df['Self_Employed']=df['Self_Employed'].fillna (df['Self_Employed'].mode()[0])
df.head()
df['LoanAmount']=df['LoanAmount'].fillna (df['LoanAmount'].mean())
df.head()
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df.head()
df['Credit_History']=df['Credit_History'].fillna (df['Credit_History'].median())
df.head()
df.info()
df.isnull().sum()
~~~
# OUTPUT:

## DATA SET:

### DATA:
![image](https://github.com/Poojariyaa/Data_cleaning/assets/127511817/46b956a2-b91e-4e86-840d-ffdb2c6f6379)
### NON NULL BEFORE:
![image](https://github.com/Poojariyaa/Data_cleaning/assets/127511817/f8d93eea-2710-411f-9652-07795027c39a)
### NON NULL AFTER:
![image](https://github.com/Poojariyaa/Data_cleaning/assets/127511817/4bc6e13e-5dd3-4401-bce2-96be2f4bed5c)

## LOAN DATA:

### DATA:
![image](https://github.com/Poojariyaa/Data_cleaning/assets/127511817/132a3606-90ae-4d64-82af-1b8b807a54b8)

### NON NULL BEFORE:
![image](https://github.com/Poojariyaa/Data_cleaning/assets/127511817/1eef24f6-d730-4ace-8b96-a4e1edc72b04)

### MODE:
![image](https://github.com/Poojariyaa/Data_cleaning/assets/127511817/cbcd953b-e153-4de3-8d80-9a97966c1abb)

### MEAN:
![image](https://github.com/Poojariyaa/Data_cleaning/assets/127511817/ee567387-c56c-403c-bee6-a617b0d1b6b3)

![image](https://github.com/Poojariyaa/Data_cleaning/assets/127511817/d3aa4b65-e39d-4b01-8136-ae8543f3f0ab)

![image](https://github.com/Poojariyaa/Data_cleaning/assets/127511817/7c123978-ff4b-4bc4-b941-1fa6f0cec683)

![image](https://github.com/Poojariyaa/Data_cleaning/assets/127511817/4609ac7d-71a0-4cc5-950f-dfc5f4187d77)

###  MEDIAN:
![image](https://github.com/Poojariyaa/Data_cleaning/assets/127511817/b88fcb17-9738-4210-b62f-95c97295a3cf)


###
![image](https://github.com/Poojariyaa/Data_cleaning/assets/127511817/b5b0f35b-d8c2-418f-994e-380ad2442e74)


###
![image](https://github.com/Poojariyaa/Data_cleaning/assets/127511817/111698ba-5a56-4989-9085-5e0c664229f5)

### NON NULL AFTER:
![image](https://github.com/Poojariyaa/Data_cleaning/assets/127511817/4cb95fba-311e-4c0f-ad54-9388cf2af8a8)

# Result
Thus data set is cleaned successfully.





