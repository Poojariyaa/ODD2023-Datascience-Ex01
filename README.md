# Ex-01_DS_Data_Cleaning

# AIM

To read the given data and perform data cleaning and save the cleaned data to a file.
# Explanation

Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.
# ALGORITHM
STEP 1

Read the given Data

STEP 2

Get the information about the data

STEP 3

Remove the null values from the data

STEP 4

Save the Clean data to the file

# CODE and OUTPUT
```
import pandas as pd
df=pd.read_csv("Data_set.csv")
print (df)
```
![263431352-d3943504-7d06-40c6-a42a-b9d33a2f2542](https://github.com/Poojariyaa/ODD2023-Datascience-Ex01/assets/127511817/3aa52696-d88f-4355-a0b3-c2865a6077ed)

```
df.head(10)
```
![263431414-ab88e21f-161b-4d9d-9123-9b4764edbd64](https://github.com/Poojariyaa/ODD2023-Datascience-Ex01/assets/127511817/cbe0adf8-a4e4-4965-8cb8-b55e40a70b58)

```
df.info()
```
![263431451-d12ab23c-9112-4a7a-9ae0-2a56fc50e162](https://github.com/Poojariyaa/ODD2023-Datascience-Ex01/assets/127511817/ef506a4f-f7dc-4116-bf70-d5c0dd5e6e4f)

```
df.isnull()
```
![263431477-82105415-c112-40aa-9ace-b07c4bc3024a](https://github.com/Poojariyaa/ODD2023-Datascience-Ex01/assets/127511817/272aa79a-1816-49a3-92b5-eb3ca190f23d)

```
df.isnull().sum()
```
![263431516-e4eb12ec-e7e7-4a34-a08b-f508b63982b3](https://github.com/Poojariyaa/ODD2023-Datascience-Ex01/assets/127511817/4468d497-fa34-4b77-98ac-564010ef3877)

```
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df.head()
```
![263431541-226762ab-d302-4b38-a6f7-6dd12b07fe42](https://github.com/Poojariyaa/ODD2023-Datascience-Ex01/assets/127511817/ae65be1a-22e5-4a9a-bcd3-7a08f186ac29)

```
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df.head()
```
![263431694-65d8d85f-8e88-4a95-8395-d934bd53fc86](https://github.com/Poojariyaa/ODD2023-Datascience-Ex01/assets/127511817/5b13f2cc-2804-4ce6-bb09-0907f72c888e)

```
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()
```
![263431828-a47c42bb-40c3-49d7-abd7-4ab9d9e9e95e](https://github.com/Poojariyaa/ODD2023-Datascience-Ex01/assets/127511817/25640003-27d6-459b-9e55-81de331604e5)

```
df['rating']=df['rating'].fillna(df['rating'].mean())
df.head()
```
![263432083-1846face-5de3-4ef8-a7cd-0ceca7d05a3a](https://github.com/Poojariyaa/ODD2023-Datascience-Ex01/assets/127511817/9327e098-9f0d-4164-bed5-ad6c11c15c7d)

```
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
```
![263432198-28c928ba-a8dc-4e85-a803-dd8de0072b35](https://github.com/Poojariyaa/ODD2023-Datascience-Ex01/assets/127511817/97cd001e-2cce-438e-8a51-707bf4c567a8)

```
df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()
```
![263432426-05ac82ac-53c7-416b-9900-a80a6fd28647](https://github.com/Poojariyaa/ODD2023-Datascience-Ex01/assets/127511817/c500ca2e-b022-4ad4-814e-20ddd4995587)

```
import pandas as pd
df=pd.read_csv("Loan_data.csv")
print (df)
```
![263432688-114ea423-6bc0-4a82-8769-ce3ae102772b](https://github.com/Poojariyaa/ODD2023-Datascience-Ex01/assets/127511817/3ad2967b-ff96-4596-9a23-a66646d4d53d)

```
df.head(10)
```
![263432824-00b5fe37-e676-4622-861f-14a6f33c0ef5](https://github.com/Poojariyaa/ODD2023-Datascience-Ex01/assets/127511817/74d3d6b3-451f-47c2-b531-5b06c9226e33)

```
df.info()
```
![263432943-54ff8bd2-9bd2-4da5-9824-a00072610476](https://github.com/Poojariyaa/ODD2023-Datascience-Ex01/assets/127511817/0d7a7d1c-a630-4c28-969d-d42d31bbf081)

```
df.isnull()
```
![263432967-744f80aa-f4c7-4d4f-a747-72b4fdf9c22c](https://github.com/Poojariyaa/ODD2023-Datascience-Ex01/assets/127511817/d9560834-9b4b-4f43-a8dc-71603291a72e)

```
df.isnull().sum()
```
![263432987-3127b10f-92e4-4d26-9b8f-0a5bd8251747](https://github.com/Poojariyaa/ODD2023-Datascience-Ex01/assets/127511817/42954eeb-face-4995-9739-c3651f08eafb)

```
df['Loan_ID']=df['Loan_ID'].fillna(df['LoanAmount'].mode()[0])
df.head()
```
![263432999-a0e4a84d-5f29-4acc-abd3-f8a10d4b5137](https://github.com/Poojariyaa/ODD2023-Datascience-Ex01/assets/127511817/7bf80a8d-ab6d-4f13-867d-03e10082cdd8)

```
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df.head()
```
![263433020-4183e39f-08f2-4225-8e93-eb1d80082586](https://github.com/Poojariyaa/ODD2023-Datascience-Ex01/assets/127511817/9a7a73ab-ae24-4f22-a949-e811eda029d8)

```
df['Education']=df['Education'].fillna(df['Education'].mode()[0])
df.head()
```
![263433046-910cc9d9-9788-4fc7-b73b-ee1e4e084a1d](https://github.com/Poojariyaa/ODD2023-Datascience-Ex01/assets/127511817/f5e74ce5-e362-4c24-bd56-7df563ebb478)

```
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df.head()
```
![263433068-0447c815-fc02-4f4c-8c93-37b55b894542](https://github.com/Poojariyaa/ODD2023-Datascience-Ex01/assets/127511817/3e7b85bf-e82e-4e22-b8f0-8206f76d0db0)

```
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()
```
![263433131-57870818-061b-4e30-b0df-814da8ee9181](https://github.com/Poojariyaa/ODD2023-Datascience-Ex01/assets/127511817/05023114-b0fe-43fb-bc21-d1d97643a275)

```
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()
```
![263433150-62ed5b96-5315-4cbc-a587-d57fae0dbe3b](https://github.com/Poojariyaa/ODD2023-Datascience-Ex01/assets/127511817/227dc135-2463-4dd9-b2a1-9609f7174990)

```
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df.head()
```
![263433167-beabdc8a-656f-4a7c-a088-5dc1daf5daef](https://github.com/Poojariyaa/ODD2023-Datascience-Ex01/assets/127511817/3069786e-4cfb-489a-8896-ac4338b8941b)

```
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].mean())
df.head()
```
![263433190-a46cde82-e89f-4d77-b307-53427c3d1af8](https://github.com/Poojariyaa/ODD2023-Datascience-Ex01/assets/127511817/e48c49e9-3e20-404a-85be-3ff64758a0d2)

# Result
Thus data set is cleaned successfully

