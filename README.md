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
import seaborn as sns
import matplotlib.pyplot as plt
x=[1,2,3,4,5]
y=[2,3,7,1,5]
sns.lineplot(x=x,y=y)
```
```
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle="solid",legend="auto")
```
![image](https://github.com/swethaselvarajm/EXNO-6-DS/assets/119525603/a38e75ed-9710-441f-8c65-6ad1262d4a76)

```
import matplotlib.pyplot as plt
tips=sns.load_dataset('tips')
avg_total_bill=tips.groupby('day')['total_bill'].mean()
avg_tip=tips.groupby('day')['tip'].mean()

plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index,avg_total_bill,label="Total Bill")
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip')
plt.xlabel('Day of the week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by day')
plt.legend()
```
![image](https://github.com/swethaselvarajm/EXNO-6-DS/assets/119525603/0830a38d-1f41-432d-9e25-67e3b2dfdf9c)

```
sns.barplot(x='day',y='total_bill',hue='sex',data=df,palette='Set2')
plt.xlabel('Day of the week')
plt.ylabel('Total Bill')
plt.title('Total Bill by day and gender')
```
![image](https://github.com/swethaselvarajm/EXNO-6-DS/assets/119525603/ab4987bb-37bd-4545-b690-2783ff2abb56)

```
import seaborn as sns
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill',y='tip',hue='sex',data=tips)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter plot of total bill vd Tip amount')
```
![image](https://github.com/swethaselvarajm/EXNO-6-DS/assets/119525603/a2d3eb3b-dde5-4dc2-b1e5-6057f765abd3)

```
import seaborn as sns
import numpy as np
import pandas as pd
num_var=pd.read_csv("/content/titanic_dataset.csv")
num_var
sns.histplot(data=num_var,x="Pclass",hue="Survived",kde=True)
```
![image](https://github.com/swethaselvarajm/EXNO-6-DS/assets/119525603/65c08724-e3e8-48b4-88e2-300ce0e7f34c)

```
np.random.seed(1)
num=np.random.randn(100)
num=pd.Series(num,name="Numerical Variable")
num
sns.histplot(data=num,kde=True)
```
![image](https://github.com/swethaselvarajm/EXNO-6-DS/assets/119525603/9e7a9d4b-fc72-4b54-bff6-175619ea66c1)

```
import matplotlib.pyplot as plt
np.random.seed(0)
marks=np.random.normal(loc=70,scale=10,size=100)
marks
sns.histplot(data=marks,bins=10,kde=True,stat="count",cumulative=False,multiple="stack",element="bars",palette="Set1",color="black",shrink=0.7)
plt.xlabel('Marks')
plt.ylabel('Density')
plt.title('Histogram of students marks')
```
![image](https://github.com/swethaselvarajm/EXNO-6-DS/assets/119525603/4fa560f6-2045-4713-8a77-7709b992661f)

```
import seaborn as sns
import pandas as pd
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'],y=tips['total_bill'],hue=tips['sex'])
```
![image](https://github.com/swethaselvarajm/EXNO-6-DS/assets/119525603/dcb3df52-d74c-4144-bc39-6000ed3abc16)

```
sns.boxplot(x='day',y='total_bill',hue='smoker',data=tips, linewidth=2,width=0.6, boxprops={'facecolor':'lightblue','edgecolor':'black'},whiskerprops={'color':'blue','linestyle':'--','linewidth':1.5},capprops={'color':'red','linestyle':'--','linewidth':1.5})
```
![image](https://github.com/swethaselvarajm/EXNO-6-DS/assets/119525603/74632279-ba5c-4631-8794-197b21d4f660)

```
import seaborn as sns
import matplotlib.pyplot as plt
tips=sns.load_dataset('tips')
sns.violinplot(x='day',y='total_bill',hue='smoker',data=tips, linewidth=2,width=0.6, palette='Set1',color='blue',inner="quartile")
plt.xlabel('Day of the week')
plt.ylabel('Total Bill')
plt.title('Violin plot of Total bill by day and smoker status')
```
![image](https://github.com/swethaselvarajm/EXNO-6-DS/assets/119525603/d3dd993e-737d-4e64-8d27-4c9c56411f10)


# Result:
Thus, all the data visualization techniques of seaborn has been implemented.
