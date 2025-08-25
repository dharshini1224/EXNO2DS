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
import pandas as pd
pd=pd.read_csv("C:\\Users\\admin\\Downloads\\titanic_dataset.csv")
pd
```

<img width="1371" height="445" alt="image" src="https://github.com/user-attachments/assets/4ea28a51-b82a-4874-813b-1b39ac6b0703" />

```
pd.shape
```
<img width="212" height="37" alt="image" src="https://github.com/user-attachments/assets/fa09667e-011b-401a-8b96-20e001505812" />

```
pd['Survived'].value_counts()
```
<img width="440" height="87" alt="image" src="https://github.com/user-attachments/assets/bbbd76ca-2495-4469-8a04-fa1cdba7d898" />

```
pd.nunique()
```
<img width="346" height="302" alt="image" src="https://github.com/user-attachments/assets/895cd7c6-fea5-4f82-80f7-05d2ae8710d8" />

```
pd.Pclass.unique()
```
<img width="401" height="60" alt="image" src="https://github.com/user-attachments/assets/2a5ff248-6073-45fe-a3b5-98286f116c2b" />

```
pd.Survived.unique()
```
<img width="380" height="38" alt="image" src="https://github.com/user-attachments/assets/2184a2fb-6658-4a61-9d20-c5548ecd54ee" />

```
sns.countplot(data=pd)
```
<img width="867" height="568" alt="image" src="https://github.com/user-attachments/assets/9b42ea5c-ad6f-4bd5-b195-7b0a378f54aa" />

```
sns.countplot(x="Survived",hue="Gender",data=pd)
```
<img width="901" height="591" alt="image" src="https://github.com/user-attachments/assets/ceab9f48-b43d-40ca-80b1-983ff689e957" />

```
sns.catplot(x="Survived",hue="Gender",data=pd,kind="count")
```
<img width="783" height="665" alt="image" src="https://github.com/user-attachments/assets/3317067d-c177-4cc0-904d-22d591dbbd1f" />

```
sns.boxplot(data=pd)
```
<img width="855" height="570" alt="image" src="https://github.com/user-attachments/assets/66b84c27-2592-4931-9eba-16acf52914c2" />

```
pd.boxplot(column="Survived",by="Gender")
```
<img width="722" height="625" alt="image" src="https://github.com/user-attachments/assets/dbb0be7d-6128-4d45-bcb2-d4ef011d10c4" />

```
sns.scatterplot(data="pd")
```
<img width="848" height="600" alt="image" src="https://github.com/user-attachments/assets/12beb39d-ccbc-4e9a-a9bf-b7d618395fb7" />

```
sns.scatterplot(x=pd['Age'],y=pd['Fare'])
```
<img width="872" height="771" alt="image" src="https://github.com/user-attachments/assets/fc10a282-6273-4310-921b-5467ef9a928f" />

```
sns.jointplot(x='Age',y='Fare',data=pd,kind="hist")
```
<img width="1721" height="1721" alt="image" src="https://github.com/user-attachments/assets/011fc6ae-d1f8-418f-9048-b60dc4c1b3ae" />

```
sns.pairplot(data=pd)
```
<img width="911" height="657" alt="image" src="https://github.com/user-attachments/assets/71bbb439-ab86-4e4e-aa04-4fc0d0652442" />

```
corr1=pd.select_dtypes(include=['number']).corr()
sns.heatmap(corr1,annot=True)
```
<img width="822" height="572" alt="image" src="https://github.com/user-attachments/assets/3db97794-0357-4abb-8c05-d8a95d7a699b" />

```
cols = ['Survived', 'Pclass', 'Age', 'Fare']
corr1 = pd[cols].corr()
sns.heatmap(corr1, annot=True)
```

<img width="527" height="418" alt="image" src="https://github.com/user-attachments/assets/d3b0410b-b7d9-432a-8e5d-dcebd149cec4" />


# RESULT
        Thus, the Exploratory Data Analysis on the given data set was performed successfully.
