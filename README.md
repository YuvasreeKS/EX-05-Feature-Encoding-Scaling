# EX:05 Feature Encoding & Scaling

# AIM
To read the given data and perform Feature Generation process and save the data to a file.

# Explanation
Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.

# ALGORITHM
STEP 1
Read the given Data

STEP 2
Clean the Data Set using Data Cleaning Process

STEP 3
Apply Feature Generation techniques to all the feature of the data set

STEP 4
Save the data to the file

# PROGRAM
Developed by:Yuvasree K S

Register number:212221040188

# For Encoding.csv file
```
import pandas as pd
df=pd.read_csv('Encoding Data.csv')
df.head()
df['ord_2'].unique()
from sklearn.preprocessing import LabelEncoder,OrdinalEncoder
climate = ['Cold','Warm','Hot']
en= OrdinalEncoder(categories = [climate])
df['ord_2']=en.fit_transform(df[["ord_2"]])
df
le = LabelEncoder()
df['Nom_0'] = le.fit_transform(df[["nom_0"]])
df
!pip install --upgrade category_encoders
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data = be.fit_transform(df['bin_1'])
df  = pd.concat([df,data],axis=1)
df
be = BinaryEncoder()
data = be.fit_transform(df['bin_2'])
df  = pd.concat([df,data],axis=1)
df
```
# Data.csv
```
import pandas as pd
df1 = pd.read_csv("data.csv")
df1.head()
df1['Ord_1'].unique()
from sklearn.preprocessing import LabelEncoder,OrdinalEncoder
climate = ['Cold','Warm','Hot','Very Hot']
en= OrdinalEncoder(categories = [climate])
df1['Ord_1']=en.fit_transform(df1[["Ord_1"]])
df1
df1['Ord_2'].unique()
cl = ['High School','Diploma','Bachelors','Masters','PhD']
en= OrdinalEncoder(categories = [cl])
df1['Ord_2']=en.fit_transform(df1[["Ord_2"]])
df1
le = LabelEncoder()
df1['City'] = le.fit_transform(df1[["City"]])
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
dat = be.fit_transform(df1['bin_1'])
df1  = pd.concat([df1,dat],axis=1)
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data1 = be.fit_transform(df1['bin_2'])
df1  = pd.concat([df1,data1],axis=1)
df1
```
# BMI.csv file
```
import pandas as pd
df2 = pd.read_csv("/content/bmi.csv")
df2.head()
be = BinaryEncoder()
data2 = be.fit_transform(df2['Gender'])
df2  = pd.concat([df2,data2],axis=1)
df2
df2 = pd.get_dummies(df2, prefix=['Index'] ,columns=['Index'])
df2
```
# OUTPUT
## For encoding.csv file
### Initial data:
![image](https://github.com/Poojariyaa/ODD2023-Datascience-Ex-05/assets/127511817/b85bb104-370b-4673-a93f-8cee7ae799ac)


## Unique value:
![image](https://github.com/Poojariyaa/ODD2023-Datascience-Ex-05/assets/127511817/b8dde99f-262b-4c99-b4a1-d1c6892c7a82)


## Ordinal Encoder:
![image](https://github.com/Poojariyaa/ODD2023-Datascience-Ex-05/assets/127511817/96659ab1-9e8d-46f8-bd4d-198ef6bd35d1)


## Label Encoder:
![image](https://github.com/Poojariyaa/ODD2023-Datascience-Ex-05/assets/127511817/b38e8e8d-acc2-446b-a8ea-4ef8c37218e0)


## Binary Encoder:
![image](https://github.com/Poojariyaa/ODD2023-Datascience-Ex-05/assets/127511817/d76de1a2-3a75-4413-af14-262a6d665768)


![image](https://github.com/Poojariyaa/ODD2023-Datascience-Ex-05/assets/127511817/1fde4a38-8dbc-4201-90b7-125e5cf5ecbb)


# For Data.csv file
## Initial data:
![image](https://github.com/Poojariyaa/ODD2023-Datascience-Ex-05/assets/127511817/129e2013-490b-48bf-93fd-2fe4ae7329b7)


## Unique data:
![image](https://github.com/Poojariyaa/ODD2023-Datascience-Ex-05/assets/127511817/ee8f56ec-42a0-4e8d-a595-c38ffeb7e256)


## Ordinal Encoder:
![image](https://github.com/Poojariyaa/ODD2023-Datascience-Ex-05/assets/127511817/1c76c15a-290d-4755-8bd7-35846e0212c7)


![image](https://github.com/Poojariyaa/ODD2023-Datascience-Ex-05/assets/127511817/90b00f57-335f-494b-b5b7-121ea93b1e96)


## Label Encoder:
![image](https://github.com/Poojariyaa/ODD2023-Datascience-Ex-05/assets/127511817/d79ba3ce-a0ec-428b-a39c-f5425ef669de)

## Binary Encoder:
![image](https://github.com/Poojariyaa/ODD2023-Datascience-Ex-05/assets/127511817/d5669ef4-2e2b-40b3-aa61-da4f0b85bc8f)

![image](https://github.com/Poojariyaa/ODD2023-Datascience-Ex-05/assets/127511817/95a18998-e2ae-472e-b33c-df12216c6691)

# For bmi.csv file
## Initial data:
![image](https://github.com/Poojariyaa/ODD2023-Datascience-Ex-05/assets/127511817/1caa8036-0d31-4b66-b60b-c3e5b5c731d5)

## Binary Encoders:
![image](https://github.com/Poojariyaa/ODD2023-Datascience-Ex-05/assets/127511817/d6335bcb-68c3-4cf2-9a0d-6737e09ac133)


## Dummies:
![image](https://github.com/Poojariyaa/ODD2023-Datascience-Ex-05/assets/127511817/6f3b1921-6e88-421f-b865-41c3bd9cbbc5)


# RESULT:
The Feature Generation process was performed and saved the data to a file.
