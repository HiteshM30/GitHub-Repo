
# Seaborn Quick Recap

Seaborn is an amazing visualization library for statistical graphics plotting in Python. 
It provides beautiful default styles and color palettes to make statistical plots more attractive. 
It is built on top matplotlib library and is also closely integrated with the data structures from pandas.

-Importing Seaborn

import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

-Reading a csv file

df= pd.read_csv("mtcars.csv")
df.shape

-Using BarPlot from SNS Library

# barplot
sns.barplot(x="cyl", y="mpg", data=df)
plt.show()


-Using CountPlot from SNS Library

# countplot
res= sns.countplot(x="mpg",data=df)
res=sns.countplot(x="gear",hue="cyl",data=df,palette="Set1")

-Using Histplot from SNS Library

# displot,hisplot
sns.histplot(df.cyl,bins=10,color='red')

-Reading a preloaded dataset

iris= sns.load_dataset('iris')
iris.head()
iris['species'].value_counts()


-Using ScatterPlot from SNS Library

# ScatterPlot
sns.scatterplot(x='sepal_length',y='petal_length',data=iris, hue='species',size='species')

-Using PairPlot from SNS Library

# PairPlot
sns.pairplot(data=iris, hue='species',palette='Set1')

-Using LMPlot from SNS Library

# LMPlot
sns.lmplot(x='petal_length',y='petal_width',data=iris,hue="species",markers=["*","o","^"])

-Using JointPlot from SNS Library

# JointPlot

sns.jointplot(x='petal_length', y='petal_width',data=iris,hue="species",palette="Set1")