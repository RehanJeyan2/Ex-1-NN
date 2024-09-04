<H3>ENTER YOUR NAME: REHAN JEYAN</H3>
<H3>ENTER YOUR REGISTER NO: 212223040167</H3>
<H3>EX. NO.1</H3>
<H3>DATE : 4/9/2024</H3>
<H1 ALIGN =CENTER> Introduction to Kaggle and Data preprocessing</H1>

## AIM:

To perform Data preprocessing in a data set downloaded from Kaggle

## EQUIPMENTS REQUIRED:
Hardware – PCs
Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook

## RELATED THEORETICAL CONCEPT:

**Kaggle :**
Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

**Data Preprocessing:**

Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis.
Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

**Need of Data Preprocessing :**

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set.
Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.


## ALGORITHM:
STEP 1:Importing the libraries<BR>
STEP 2:Importing the dataset<BR>
STEP 3:Taking care of missing data<BR>
STEP 4:Encoding categorical data<BR>
STEP 5:Normalizing the data<BR>
STEP 6:Splitting the data into test and train<BR>

##  PROGRAM:
'''
#importing libraries
import pandas as pd
import io
from sklearn.preprocessing import StandardScaler
from sklearn.model_selection import train_test_split

#Reading the dataset
df=pd.read_csv("Churn_Modelling.csv", index_col="RowNumber")
df

#Dropping the unwanted Columns
df.drop(['CustomerId'],axis=1,inplace=True)
df.drop(['Surname'],axis=1,inplace=True)
df.drop('Age',axis=1,inplace=True)
df.drop('Geography',axis=1,inplace=True)
df.drop('Gender',axis=1,inplace=True)
df

#Checking for null values
df.isnull().sum()

#Checking for duplicate values
df.duplicated()

#Describing the dataset
df.describe()

#Scaling the dataset
scaler=StandardScaler()
df1=pd.DataFrame(scaler.fit_transform(df))
df1

#Allocating X and Y attributes
x=df1.iloc[:,:-1].values
x
y=df1.iloc[:,-1].values
y

#Splitting the data into training and testing dataset
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2)
print(x_train)
print(len(x_train))
print(x_test)
print(len(x_test))
'''

## OUTPUT:
## DataSet:
![image](https://github.com/user-attachments/assets/92b00f6e-f0de-4b3f-8785-885369b3e0f0)
## Dropping the Unwanted DataSet:
![image](https://github.com/user-attachments/assets/b47674a7-59ad-406e-a6fb-5a26b31f446b)
## Checking NULL Values:
![image](https://github.com/user-attachments/assets/49e110fe-2a99-4fc5-b142-436405c04527)
## Checking For Duplication:
![image](https://github.com/user-attachments/assets/37182ea7-0d2f-4e91-9433-f8fe01f31414)
## Describing The DateSet:
![image](https://github.com/user-attachments/assets/2bc1359f-cb1f-406e-a28a-69664179795b)
## Scaling The DataSet:
![image](https://github.com/user-attachments/assets/f5dff33a-b13f-4355-be5c-3a3f737acd89)
## X Features:
![image](https://github.com/user-attachments/assets/b61fc73d-f2be-4fb2-8cd6-c1b584f91092)
## Y Features:
![image](https://github.com/user-attachments/assets/84189f8b-668c-4b63-91d7-99b31f95c7fe)
## Splitting The Training And Testing DataSet:
![image](https://github.com/user-attachments/assets/e9f9f9d9-bc60-4414-b1e3-95637f9fff80)










## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


