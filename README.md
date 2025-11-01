# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```
Name : HARI PRASATH P
Reg. No : 212224230084
```
```
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
```
<img width="1024" height="170" alt="image" src="https://github.com/user-attachments/assets/8648ebac-c8d5-422d-a12a-0b7a2fa73a43" />

### Line Plot 

```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
<img width="462" height="383" alt="image" src="https://github.com/user-attachments/assets/cd2304a7-da7d-490c-bdc6-08afb8f65a53" />


### MultiLine Plot

```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```
<img width="465" height="387" alt="image" src="https://github.com/user-attachments/assets/3423a5f7-70b2-4bc6-a032-034dce39d684" />

## To visualize relatioships

### Bar Chart

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
<img width="598" height="415" alt="image" src="https://github.com/user-attachments/assets/f260935f-f26d-4e60-8981-6f20194f35f7" />

### Scatter Plot

```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
<img width="495" height="384" alt="image" src="https://github.com/user-attachments/assets/fae8c36e-6621-44a5-bcd9-2ea9c53f2931" />

### Bubble Chart

```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
<img width="495" height="390" alt="image" src="https://github.com/user-attachments/assets/2d0ff2a5-fe55-4cfe-8e91-bc288bfcdde9" />

## To capture distributions

### Histogram
```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
<img width="496" height="371" alt="image" src="https://github.com/user-attachments/assets/2b4432d3-fb10-49bc-ae1e-b66dccbf02e8" />

### Box Plot

```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
<img width="477" height="381" alt="image" src="https://github.com/user-attachments/assets/4a532c72-a4c8-4557-b093-1d3e17bbc18a" />

### Violin Plot

```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
<img width="492" height="388" alt="image" src="https://github.com/user-attachments/assets/591817a5-50fb-4d9b-8400-b788bd0c2e3e" />

### Density Plot

```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
<img width="506" height="403" alt="image" src="https://github.com/user-attachments/assets/f2fb0327-1699-4d97-a231-f2e8121eaa23" />

### Heatmap
```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```

<img width="516" height="432" alt="image" src="https://github.com/user-attachments/assets/31bf59c5-31b7-4458-88d9-c1cfe46d4b91" />

# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
