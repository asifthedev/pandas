![SPEAK LIKE A PROsvg](file://C:\Users\asifj\Downloads\SPEAK%20LIKE%20A%20PRO.svg?msec=1720871802332)

Pandas is an open-source Python package used to manipulate and analyze structured data meaning the data in tabular form. For example, we have a CSV file called `data.csv`

| Name | Age | City | Salary | Department |
| --- | --- | --- | --- | --- |
| Alice | 24  | New York | 70000 | HR  |
| Bob | 27  | Los Angeles | 80000 | Finance |
| Charlie | 22  | Chicago | 60000 | IT  |

## read_csv

This method is used to load data from a CSV file. It's not the only method there are plenty of other methods for loading different types of data.

```python
import pandas as pd
df = pd.read_csv('data.csv')
```

**index parameter**

There is an index parameter that is use to specify which colum you want to use for indexing by default it use a column containing integers starting from 0-n.

```python
df = pd.read_csv('data.csv', index_col='Name')
```

Here I'm asking pandas to use `Name` column for indexing. Make sure the indexing colum is uniquly defining every record in the dataset.

**Note:** now this colum is not counted in your data if at this stage if you run `df.shape` it will give you `(3, 4)` as output instead of `(3,5)`

## shape -> attribute

This method returns a tuple where index 0 contains the total number of rows and index 1 contains the total number of columns. For example to check the shape of the `data.csv` file that we have loaded, we can use.

```python
df.shape #Output: (rows: 3, columns: 5)
```

## info -> method
