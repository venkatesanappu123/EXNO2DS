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



# RESULT
        <<INCLUDE YOUR RESULT HERE>>
