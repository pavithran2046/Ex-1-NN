# Introduction to Kaggle and Data preprocessing

### Name : PAVITHRAN S
### Reg  : 212223240113
### Date :  

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
### STEP 1:Importing the libraries<BR>
### STEP 2:Importing the dataset<BR>
### STEP 3:Taking care of missing data<BR>
### STEP 4:Encoding categorical data<BR>
### STEP 5:Normalizing the data<BR>
### STEP 6:Splitting the data into test and train<BR>

##  PROGRAM:

```
import pandas as pd
import io
from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split
```
```
df = pd.read_csv("Churn_Modelling.csv")
print(df)
```
```
print(df.isnull().sum())
```
```
df.duplicated().sum
```
```
df.describe()
```
```
df= df.drop(['Surname', 'Geography','Gender'], axis=1)
print(df)
```
```
scaler = MinMaxScaler()
df1 = pd.DataFrame(scaler.fit_transform(df), columns=df.columns)
print(df1)
```
```
X = df1.drop('Exited', axis=1)
y = df1['Exited']
print(X,y)
```
```
X_train ,X_test ,y_train,y_test=train_test_split(X,y,test_size=0.2)
```
```
print("X_train:\n", X_train)
print("X_test:\n", X_test)
print("y_train:\n", y_train)
print("y_test:\n", y_test)
```
## OUTPUT:

### Reading Dataset:
<img width="788" height="298" alt="image" src="https://github.com/user-attachments/assets/efe88967-4584-4ba0-8f76-bb48c80d5fad" />

### Missing values:
<img width="276" height="374" alt="image" src="https://github.com/user-attachments/assets/dc110856-0413-4ae6-a4f1-02d5ad0108f1" />


### Duplicate values:
<img width="419" height="300" alt="image" src="https://github.com/user-attachments/assets/90fd04f3-1f8a-4d05-8b5b-4cbd04e919cc" />

### Outlier Detection:
<img width="815" height="295" alt="image" src="https://github.com/user-attachments/assets/e6d67340-c0bd-4bd6-8f39-d670c5f8cbe7" />


### Remove UUnnecessary Columns:
<img width="673" height="300" alt="image" src="https://github.com/user-attachments/assets/a6f3fc34-8f44-4520-ad22-306ba0c4a4b8" />


### Normalize:
<img width="689" height="290" alt="image" src="https://github.com/user-attachments/assets/1e229e57-80ac-49c1-a978-b492d9ffbde7" />


### X and Y Columns:
<img width="735" height="285" alt="image" src="https://github.com/user-attachments/assets/2525785d-b08d-47ce-80e3-e3b3f113dfd8" />


### Xtrain and ytrain:
<img width="716" height="711" alt="image" src="https://github.com/user-attachments/assets/f058a65a-fe0d-41ca-bf5e-9ed2c1d1f5ba" />


## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


