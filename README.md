# Ex-01_DS_Data_Cleansing


## AIM
To read the given data and perform data cleaning and save the cleaned data to a file. 

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Get the information about the data
### STEP 3
Remove the null values from the data
### STEP 4
Save the Clean data to the file

```
## developed by :
            shabrena vincent

## register number:
            212222230141

```
# CODE :


LOAN_DATA_CSV



```
import pandas as pd
df=pd.read_csv("/Loan_data.csv")
print(df)
df.head(10)
df.info()
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()

df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()

df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()

df.info()
df.isnull().sum()
```

DATA_SET.CSV



```
import pandas as pd
df=pd.read_csv("/Data_set.csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()

df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()

df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()

df.info()
df.isnull()
df.isnull().sum()
```
# OUTPUT:


## FOR LOAN_DATA:



```
import pandas as pd
df=pd.read_csv("/Loan_data.csv")
print(df)
df.head(10)
```





![image](https://github.com/shabreenavincent/ODD2023-Datascience-Ex01/assets/119475721/fb7ce5e6-74a0-4eef-88bb-a4ce576516c4)


NON NULL BEFORE:


```
df.info
```


![image](https://github.com/shabreenavincent/ODD2023-Datascience-Ex01/assets/119475721/5af272fb-8e80-44bd-94aa-4ffb9cda5ac1)


MODE:
```
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()
```



![image](https://github.com/shabreenavincent/ODD2023-Datascience-Ex01/assets/119475721/a73feeec-8a20-4787-ba90-35c7a7a45bb7)




MEAN



```
df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()
```



![image](https://github.com/shabreenavincent/ODD2023-Datascience-Ex01/assets/119475721/08a2c785-0aec-4c57-b187-e6658fa0571d)



MEDIAN:



```
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()
```



![image](https://github.com/shabreenavincent/ODD2023-Datascience-Ex01/assets/119475721/5bab01fa-77f6-4446-8219-02236c53c279)



NON NULL AFTER



```
df.info()
```



![image](https://github.com/shabreenavincent/ODD2023-Datascience-Ex01/assets/119475721/26882fcf-1d0d-42ef-a84c-c9efdfd2c37d)



```
df.isnull().sum()
```



![image](https://github.com/shabreenavincent/ODD2023-Datascience-Ex01/assets/119475721/de4d8243-e283-4c9a-b8cf-6bf6cce150cd)



## FOR DATA_SET:


DATA


```
import pandas as pd
df=pd.read_csv("/Data_set.csv")
print(df)
df.head(10)
```



![image](https://github.com/shabreenavincent/ODD2023-Datascience-Ex01/assets/119475721/a066355d-8fc3-438b-b71c-773ffc7f51d8)


NON NULL BEFORE



```
df.info()
```


![image](https://github.com/shabreenavincent/ODD2023-Datascience-Ex01/assets/119475721/77664b6a-f971-49bb-abef-761129aebaa8)


```
df.isnull()
```


![image](https://github.com/shabreenavincent/ODD2023-Datascience-Ex01/assets/119475721/70545501-202b-42c5-9afe-eef925891d5a)



MODE



```
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()
```



![image](https://github.com/shabreenavincent/ODD2023-Datascience-Ex01/assets/119475721/adba94fc-b7b4-4a16-a12b-1cb99c658873)


MEAN


```
df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
```


![image](https://github.com/shabreenavincent/ODD2023-Datascience-Ex01/assets/119475721/5a89ab38-7af5-4a85-8650-b5938eb6b8fc)



MEDIAN



```
df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()
```


![image](https://github.com/shabreenavincent/ODD2023-Datascience-Ex01/assets/119475721/b1d14106-f314-4159-a469-dc8a06e297d0)


``
df.info()
``


![image](https://github.com/shabreenavincent/ODD2023-Datascience-Ex01/assets/119475721/f10ff65a-c552-4f05-b9a5-c4473a4f20da)


```
df.isnull()
```


![image](https://github.com/shabreenavincent/ODD2023-Datascience-Ex01/assets/119475721/1eee1f82-8e3f-4b78-a1e4-bf60baea6aea)


```
df.isnull().sum()
```



![image](https://github.com/shabreenavincent/ODD2023-Datascience-Ex01/assets/119475721/765df05b-1f64-4bfc-adbb-f1b4fc61d30e)



# RESULT:
Thus,the given data is read,cleansed and the cleaned data is saved into the file.

