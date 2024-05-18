
# Python Data Analysis Tutorial

## Introduction

Python is a powerful language for data analysis due to its vast range of libraries and simplicity. This tutorial will guide you through some essential commands and libraries to get started with data analysis in Python.

### Table of Contents
1. [Libraries to Import](#libraries-to-import)
2. [Reading Data](#reading-data)
3. [Exploring Data](#exploring-data)
4. [Data Cleaning](#data-cleaning)
5. [Data Visualization](#data-visualization)
6. [Aggregation and Grouping](#aggregation-and-grouping)
7. [Exporting Data](#exporting-data)
8. [Additional Tips](#additional-tips)

## Libraries to Import

First, import the essential libraries that are commonly used for data analysis:

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```

## Reading Data

### Read CSV File

```python
df = pd.read_csv('data.csv')
```

### Read Excel File

```python
df = pd.read_excel('data.xlsx', sheet_name='Sheet1')
```

## Exploring Data

Once you've loaded your data into a DataFrame, you can begin exploring and analyzing it. Here are some initial steps you can take after reading the data:

### Display First 5 Rows

```python
print(df.head())
```

### Display Column Names

```python
print(df.columns)
```

### Display Summary Statistics

```
python
print(df.describe())
```

### Display Information About the DataFrame

```python
print(df.info())
```

## Data Cleaning

### Handle Missing Values

#### Drop rows with missing values:


```python
df.dropna(inplace=True)
```


#### Fill missing values with a specified value:

```python
df.fillna(0, inplace=True)
```

### Remove Duplicates

```python
df.drop_duplicates(inplace=True)
```

### Convert Data Types

```python
df['column_name'] = df['column_name'].astype('int')
```

## Data Visualization

### Histogram

```python
df['column_name'].hist()
plt.show()
```

### Scatter Plot

```python
df.plot.scatter(x='column1', y='column2')
plt.show()
```

### Bar Plot

```python
df['column_name'].value_counts().plot.bar()
plt.show()
```

### Correlation Heatmap

```python
sns.heatmap(df.corr(), annot=True, cmap='coolwarm')
plt.show()
```

## Aggregation and Grouping

### Group By and Aggregate

```python
grouped_df = df.groupby('column_name').mean()
print(grouped_df)
```

### Pivot Table

```python
pivot_table = df.pivot_table(values='value_column', index='index_column', columns='column_name')
print(pivot_table)
```

## Exporting Data

### Export to CSV

```python
df.to_csv('output.csv', index=False)
```

### Export to Excel

```python
df.to_excel('output.xlsx', index=False)
```

## Additional Tips

### Display All Rows and Columns in DataFrame

```python
pd.set_option('display.max_rows', None)
pd.set_option('display.max_columns', None)
```

### Reset Options to Default

```python
pd.reset_option('display.max_rows')
pd.reset_option('display.max_columns')
```

This completes the tutorial document for basic Python data analysis commands. 
