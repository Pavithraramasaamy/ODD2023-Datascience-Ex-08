# Ex-08 Data Visualization 
# AIM
To Perform Data Visualization on a complex dataset and save the data to a file.

# Explanation
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Clean the Data Set using Data Cleaning Process

## STEP 3
Apply Feature generation and selection techniques to all the features of the data set

## STEP 4
Apply data visualization techniques to identify the patterns of the data.

# PROGRAM:
```
DEVELOPED BY : PAVITHRA R
REG NO : 212222230106

## Data Visualization using Seaborn :

import seaborn as sns
from matplotlib import pyplot as plt

## 1.Line Plot:

plt.figure(figsize=(9,6))
sns.lineplot(x="Segment",y="Region",data=df,marker='o')
plt.xticks(rotation = 90)

sns.lineplot(x='Ship Mode',y='Category', hue ="Segment",data=df)

sns.lineplot(x="Category",y="Sales",data=df,marker='o')

## 2.Scatterplot :

sns.scatterplot(x='Category',y='Sub-Category',data=df)

sns.scatterplot(x='Category', y='Sub-Category', hue ="Segment",data=df)

plt.figure(figsize=(10,7))
sns.scatterplot(x="Region",y="Sales",data=df)
plt.xticks(rotation = 90)


## 3.Boxplot:

sns.boxplot(x="Sub-Category",y="Discount",data=df)
sns.boxplot( x="Profit", y="Category",data=df)

## 4.Violin Plot :

sns.violinplot(x="Profit",data=df)

## 5.Barplot :

sns.barplot(x="Sub-Category",y="Sales",data=df)
plt.xticks(rotation = 90)

sns.barplot(x="Category",y="Sales",data=df)
plt.xticks(rotation = 90)

## 6.Pointplot :

sns.pointplot(x=df["Quantity"],y=df["Discount"])

## 7.Count plot :

sns.countplot(x="Category",data=df)

sns.countplot(x="Sub-Category",data=df)

## 8.Histogram :

sns.histplot(data=df,x ='Ship Mode',hue='Sub-Category')

## 9.KDE Plot :

sns.kdeplot(x="Profit", data = df,hue='Category')

## Data Visualization Using MatPlotlib :

1.Plot :

plt.plot(df['Category'], df['Sales'])
plt.show()

2.Heatmap :

df.corr()
plt.subplots(figsize=(12,7))
sns.heatmap(df.corr(),annot=True)

3.Piechart :
df1=df.groupby(by=["Ship Mode"]).sum()
labels=[]
for i in df1.index:
    labels.append(i)
colors=sns.color_palette("bright")
plt.pie(df1["Sales"],labels=labels,autopct="%0.0f%%")
plt.show()

df3=df.groupby(by=["Category"]).sum()
labels=[]
for i in df3.index:
    labels.append(i) 
plt.figure(figsize=(8,8))
colors = sns.color_palette('pastel')
plt.pie(df3["Profit"],colors = colors,labels=labels, autopct = '%0.0f%%')
plt.show()


4.Histogram :

plt.hist(df["Sub-Category"],facecolor="peru",edgecolor="blue",bins=10)
plt.show()


5.Bargraph :

plt.bar(df.index,df['Category'])
plt.show()


6.Scatterplot :

plt.scatter(df["Region"],df["Profit"], c ="blue")
plt.show()


7.Boxplot :
plt.boxplot(x="Sales",data=df)
plt.show()


```

# OUTPUT:

## Data Visualization Using Seaborn :

## 1.Line Plot:

![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-08/assets/118596964/daf36f2b-b260-48d1-bdcb-71175b0de972)

![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-08/assets/118596964/35bc8e90-edd9-4e12-945d-236a0602722e)

![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-08/assets/118596964/7ba38255-b64d-4ec0-81e1-a9d5e46d33cb)

## 2.Scatterplot :

![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-08/assets/118596964/0a7cb827-53b5-4faa-b9a8-5b80403b0c3d)

![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-08/assets/118596964/6fe415ca-4fa0-4522-8fd9-ca3e99083d28)

![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-08/assets/118596964/ce2319e5-b42f-4ff7-85c9-0c892a8ca876)

## 3.Boxplot:

![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-08/assets/118596964/12827ca7-6157-46b1-aec2-06a95549d947)

![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-08/assets/118596964/d1e86355-fefb-4893-a8e6-64c8c1de3f0e)

## 4.Violin Plot :

![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-08/assets/118596964/6a74f5f3-72de-4498-8c1e-49355432e225)

## 5.Barplot :

![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-08/assets/118596964/bd1d4b7d-fd8a-4b01-93ef-5fcc22581c7d)

![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-08/assets/118596964/6fd5bf53-1489-4d5a-a339-af23fb20b471)

## 6.Pointplot :

![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-08/assets/118596964/c425bb18-18c3-491b-9b69-d09df6e1a1fd)


## 7.Count plot :

![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-08/assets/118596964/d99cc8e4-e75d-46ff-a541-fe664c0356ca)

![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-08/assets/118596964/6044ceb1-94b7-4422-83e2-1ff065956d15)

## 8.Histogram :

![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-08/assets/118596964/a186107e-844e-4d6f-97eb-a7b66738e626)

## 9.KDE Plot :

![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-08/assets/118596964/631943e3-3ebb-4c1a-b3c7-bc299ec0fd6f)


## Data Visualization Using Matplotlib :

## 1.Plot:

![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-08/assets/118596964/1e8189e5-45f5-4bc8-9d85-651d64cc53de)

## 2.Heatmap :

![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-08/assets/118596964/e19c1c58-8fa8-4cc0-a9a6-1a5e8fd9a52f)


## 3.Piechart :

![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-08/assets/118596964/d97df14d-c519-445e-9f4d-1e31488c7f17)

![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-08/assets/118596964/dd5dfbd7-1472-45b6-a8ee-4eb9a4a1919e)


## 4..Histogram :

![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-08/assets/118596964/997c9443-94bc-4d4c-a3bb-16e073b079a8)


5.Bargraph :
![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-08/assets/118596964/9b9c5691-81da-4895-9fee-2a281813306c)

## 6.Scatterplot :

![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-08/assets/118596964/0b88a352-eb73-4c95-b3ba-788df0678608)

## 7.Boxplot :

![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-08/assets/118596964/3bf0089c-7f2e-453f-97c2-337adf1f3e48)


### Result :
Hence,Data Visualization is applied on the complex dataset using libraries like Seaborn and Matplotlib successfully and the data is saved to file.

