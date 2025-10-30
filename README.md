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
## Name   :  Kishore S
## Reg NO :  212222240050
```
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
```
<img width="1577" height="402" alt="image" src="https://github.com/user-attachments/assets/41bf4d05-a00f-41cc-8a93-0c130eba9425" />

## 1.Line Plot

```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
<img width="1043" height="732" alt="image" src="https://github.com/user-attachments/assets/3e523a73-3772-4900-bdcc-084856800467" />

## 2.Multi Line Plot

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
<img width="932" height="776" alt="image" src="https://github.com/user-attachments/assets/6171344f-56fa-4351-864e-2c12ab71bb0d" />

## TO VISUALIZE RELATIONSHIPS
### 1.Bar Chart

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
<img width="1640" height="741" alt="image" src="https://github.com/user-attachments/assets/2a0d7e8f-5347-4f7b-a484-bec5ba5fa52c" />

## 2.Scatter Plot

```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
<img width="828" height="616" alt="image" src="https://github.com/user-attachments/assets/6beb16e8-c6a3-4f16-a4b7-d3a6c73d3279" />

## 3.Bubble Chart

```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
<img width="883" height="617" alt="image" src="https://github.com/user-attachments/assets/4079f6a7-4cc0-48fb-9434-d49cbca21c22" />

## TO CAPTURE DISTRIBUTIONS
## 1.Histogram
```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
<img width="1025" height="567" alt="image" src="https://github.com/user-attachments/assets/025b235d-41d6-4eb8-bc77-c6d3be63bb53" />

## 2.Box Plot

```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
<img width="1555" height="722" alt="image" src="https://github.com/user-attachments/assets/2918ce11-4217-4fee-8fe5-0d85fc323e44" />

## 3.Violin Plot

```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
<img width="1131" height="612" alt="image" src="https://github.com/user-attachments/assets/a633ece0-7c2e-4f6b-b584-270749ea7450" />

## 4.Density Plot 

```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
<img width="1032" height="743" alt="image" src="https://github.com/user-attachments/assets/52536c4e-836e-4c60-8487-bdef2dd04db4" />

## 5.Heatmap

```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
<img width="1123" height="716" alt="image" src="https://github.com/user-attachments/assets/263cffad-1963-4d72-9082-8c849e35f192" />

# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
