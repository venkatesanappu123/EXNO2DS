# EXNO2DS
# AIM:
      To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT
```
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
import pandas as pd
df=pd.read_csv('titanic_dataset.csv')
df
```
![Screenshot 2025-03-22 110138](https://github.com/user-attachments/assets/d39d1bee-f994-4237-b52d-3509554edcbb)
```
df.info()
```
![Screenshot 2025-03-22 110308](https://github.com/user-attachments/assets/902ac7f3-5338-42ca-ba66-955f6e81aeda)
```
df.shape
```
![Screenshot 2025-03-22 110422](https://github.com/user-attachments/assets/c76365fd-22ab-47b6-b74f-52f97adf19af)
```
df.head(4)
```
![Screenshot 2025-03-22 110608](https://github.com/user-attachments/assets/2ee2c4eb-4c06-452a-9129-e4515a5f9d54)
```
df.nunique()
```
![Screenshot 2025-03-22 110942](https://github.com/user-attachments/assets/65365f6e-db8f-4bc2-96d1-907f6f4d3ac5)
```
df["Survived"].value_counts()
```
![Screenshot 2025-03-22 111105](https://github.com/user-attachments/assets/cfa5a2b5-6d50-4486-a734-393e5755e860)
```
per=(df["Survived"].value_counts()/df.shape[0]*100).round(2)
per
```
![Screenshot 2025-03-22 111325](https://github.com/user-attachments/assets/92dc625d-5d42-430c-a961-8012ace954a5)
```
sns.countplot(data=df,x="Survived")
```
![Screenshot 2025-03-22 111547](https://github.com/user-attachments/assets/9f0065f1-9daf-420e-99e3-a9e52f981054)
```
df.Pclass.unique()
```
![Screenshot 2025-03-22 111659](https://github.com/user-attachments/assets/6e8ffa88-0576-488f-b274-e5241f0b07a2)
```
df.rename(columns={"Sex" : 'Gender'}, inplace=True)
df
```
![Screenshot 2025-03-22 111908](https://github.com/user-attachments/assets/5f1145e4-51a5-471d-b983-14866220a5d6)
```
sns.catplot(x="Gender",col="Survived",kind="count", data=df,height=5,aspect=.7)
```
![Screenshot 2025-03-22 112329](https://github.com/user-attachments/assets/26b2bcf5-79ff-4ea9-8282-a5f71b1d8471)
```
sns.catplot(x="Survived",hue="Gender",data=df,kind="count")
```
![Screenshot 2025-03-22 112530](https://github.com/user-attachments/assets/90a032f8-4637-4986-a9ed-2237f81cdba8)
```
df.boxplot(column="Age",by="Survived")
```
![Screenshot 2025-03-22 112710](https://github.com/user-attachments/assets/dfd05ad5-100e-4707-9ff3-8e18120a2e66)
```
sns.scatterplot(x=df["Age"],y=df['Fare'])
```
![Screenshot 2025-03-22 112903](https://github.com/user-attachments/assets/17ec5e71-8e43-47ef-92a1-6dc28b642569)
```
sns.jointplot(x="Age",y="Fare",data=df)
```
![Screenshot 2025-03-22 113058](https://github.com/user-attachments/assets/b7bd46a5-43de-4663-a1f3-257bd6707978)
```
fig,ax1=plt.subplots (figsize=(8,5))
pt=sns.boxplot(ax=ax1,x='Pclass', y='Age', hue='Gender', data=df)
```
![Screenshot 2025-03-22 113302](https://github.com/user-attachments/assets/b3a8ace5-8e32-4c7d-9e85-0f125e884ed1)
```
corr = df. select_dtypes (include=['number']). corr()
sns. heatmap(corr,annot=True)
```
![Screenshot 2025-03-22 113547](https://github.com/user-attachments/assets/a6e4c6ed-5f52-4ae2-8b6a-457a9da77051)
```
sns.pairplot(df)
```
![Screenshot 2025-03-22 113739](https://github.com/user-attachments/assets/acf5cafe-6a50-49e3-b987-8b3e63787cf6)
```
sns.catplot(data=df, col="Survived", x="Gender", hue="Pclass", kind="count" )
```
![Screenshot 2025-03-22 113959](https://github.com/user-attachments/assets/a6ec4961-0e45-4996-b506-69489351da78)

# RESULT
To perform Exploratory Data Analysis on the given data set is succesfully completed.
