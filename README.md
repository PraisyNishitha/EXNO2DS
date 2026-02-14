# EXNO2DS
# NAME : Praisy nishitha
# ref no : 212224100042
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
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```


<img width="1433" height="658" alt="image" src="https://github.com/user-attachments/assets/3f40df62-3ad1-4566-b295-c45269e179ca" />


```
dt.info()
```

<img width="1020" height="497" alt="image" src="https://github.com/user-attachments/assets/2e7d96d7-d3d2-43e2-9f4e-b9ee517693db" />

```
dt.shape
```

<img width="1575" height="162" alt="image" src="https://github.com/user-attachments/assets/b550a894-f311-40ff-99d0-6706fc72b5d6" />

```
dt.describe()
```

<img width="1516" height="454" alt="image" src="https://github.com/user-attachments/assets/19b97c7e-adc6-436d-9842-9ab253380987" />

```
dt.nunique()
```


<img width="1421" height="815" alt="image" src="https://github.com/user-attachments/assets/73d808e9-6720-4d3f-8f7b-6bf290bc3682" />


```
dt["Survived"].value_counts()
```


<img width="1361" height="584" alt="image" src="https://github.com/user-attachments/assets/ed0f65db-6df7-49d1-ad41-10ab897d7854" />

```
per=(dt["Survived"].value_counts()/dt.shape[0]*100).round(2)
per

```


<img width="1123" height="319" alt="image" src="https://github.com/user-attachments/assets/94dccb32-c823-4ab5-8461-873ff9fd8818" />


```
sns.countplot(data=dt,x="Survived")
```


<img width="1290" height="661" alt="image" src="https://github.com/user-attachments/assets/e9049a26-218f-4079-b9ee-718d2b8a6f7d" />

```
dt
```


<img width="1463" height="683" alt="image" src="https://github.com/user-attachments/assets/3e57e6a2-2a58-4cae-abef-a434fb4256b5" />

```
dt.Pclass.unique()
```

<img width="1536" height="133" alt="image" src="https://github.com/user-attachments/assets/ce1ea0f0-e734-4a0f-bc27-ed9560283ac7" />


```
dt.rename(columns={'Sex':'Gender'},inplace=True)
dt
```


<img width="1559" height="713" alt="image" src="https://github.com/user-attachments/assets/8a18bfb7-36e1-4a62-817f-3412d0db0cc1" />

```
sns.catplot(x="Gender",col="Survived",kind="count",data=dt,height=5,aspect=.7)
```

<img width="1008" height="691" alt="image" src="https://github.com/user-attachments/assets/0345a8d0-c425-49ba-826a-6fd43af15827" />

```
sns.catplot(x='Survived',hue="Gender",data=dt,kind='count')
```


<img width="1234" height="719" alt="image" src="https://github.com/user-attachments/assets/45f47747-2c09-40a5-b68f-8f4afff54bd9" />


```
dt.boxplot(column="Age",by="Survived")
```

<img width="1147" height="698" alt="image" src="https://github.com/user-attachments/assets/d13ed908-0a32-4ea6-8d1f-1a23f4de9ba2" />

```
sns.scatterplot(x=dt["Age"],y=dt["Fare"])
```

<img width="1010" height="672" alt="image" src="https://github.com/user-attachments/assets/7bc72592-a0d2-45d9-8791-59cf254ca103" />


```

sns.jointplot(x="Age",y="Fare",data=dt)
```

<img width="1240" height="813" alt="image" src="https://github.com/user-attachments/assets/b627ea97-89cb-4fdc-ab2c-58bee4304911" />


```
fig,ax1=plt.subplots(figsize=(8,5))
sns.boxplot(ax=ax1,x="Pclass",y="Age",hue="Gender",data=dt)
```


<img width="1119" height="708" alt="image" src="https://github.com/user-attachments/assets/74b9fcd3-f783-4625-885b-4cbe2e16667a" />

```
sns.catplot(data=dt,col="Survived",x="Gender",hue="Pclass",kind="count")
```


<img width="1549" height="794" alt="image" src="https://github.com/user-attachments/assets/506c8acb-deb1-49e6-99c6-8cd7f999f6ed" />

```
corr=dt.corr(numeric_only=True)
sns.heatmap(corr,annot=True)
```



<img width="527" height="418" alt="download" src="https://github.com/user-attachments/assets/020e1b8f-ca55-425a-b778-c8406febcc5c" />

```
sns.pairplot(dt)
```
<img width="1476" height="1476" alt="download" src="https://github.com/user-attachments/assets/7379d019-0262-427f-8367-f26ab3763a19" />



        

# RESULT
Thus,the Exploratory Data Analysis on the given data set was performed successfully
     >
