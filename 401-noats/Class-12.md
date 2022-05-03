# Class 12

pandas is part of the Anaconda distribution and has many features handling data.

## **Object creation**

Creating a **`[Series](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.html#pandas.Series)`** is possible by passing a list of values, letting pandas create a default integer index.

```python
In [3]: s = pd.Series ([1, 3, 5, np.nan, 6, 8])

In [4]: s
Out[4]:
0    1.0
1    3.0
2    5.0
3    NaN
4    6.0
5    8.0
dtype: float64 # series and data type is returned
```

# **Viewing data**

Viewing data is possible by calling for the node head or the tail

```python
In[13]: df.head()#call the head to view the top of a series
Out[13]: 
                   A         B         C         D
2013-01-01  0.469112 -0.282863 -1.509059 -1.135632
2013-01-02  1.212112 -0.173215  0.119209 -1.044236
2013-01-03 -0.861849 -2.104569 -0.494929  1.071804
2013-01-04  0.721555 -0.706771 -1.039575  0.271860
2013-01-05 -0.424972  0.567020  0.276232 -1.087401

df.tail(3)#call the tail to view the bottom of a series
Out[14]: 
                   A         B         C         D
2013-01-04  0.721555 -0.706771 -1.039575  0.271860
2013-01-05 -0.424972  0.567020  0.276232 -1.087401
2013-01-06 -0.673690  0.113648 -1.478427  0.524988

In [15]: df.index#to view the index
Out[15]: 
DatetimeIndex(['2013-01-01', '2013-01-02', '2013-01-03', '2013-01-04',
               '2013-01-05', '2013-01-06'],
              dtype='datetime64[ns]', freq='D')

df.columns#to view the columns
Out[16]: Index(['A', 'B', 'C', 'D'], dtype='object')
```

**`[DataFrame.to_numpy()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.to_numpy.html#pandas.DataFrame.to_numpy)`**gives a NumPy representation of the underlying data. A key difference between numpy and pandas is that ***NumPy arrays have one data type for the entire array, while pandas DataFrames have one data type per column***

When you call **`[DataFrame.to_numpy()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.to_numpy.html#pandas.DataFrame.to_numpy)`**, pandas will find the NumPy dtype that can hold *all*
 of the dtypes in the DataFrame. This is pretty cool!

```python
In [17] df.to_numpy()
Out[17]: 
array([[ 0.4691, -0.2829, -1.5091, -1.1356],
       [ 1.2121, -0.1732,  0.1192, -1.0442],
       [-0.8618, -2.1046, -0.4949,  1.0718],
       [ 0.7216, -0.7068, -1.0396,  0.2719],
       [-0.425 ,  0.567 ,  0.2762, -1.0874],
       [-0.6737,  0.1136, -1.4784,  0.525 ]])
#this array contains all floating values, 
#doesnt require copying return a valid dtype

In [18] df2.to_numpy()
Out[18]: 
array([[1.0, Timestamp('2013-01-02 00:00:00'), 1.0, 3, 'test', 'foo'],
       [1.0, Timestamp('2013-01-02 00:00:00'), 1.0, 3, 'train', 'foo'],
       [1.0, Timestamp('2013-01-02 00:00:00'), 1.0, 3, 'test', 'foo'],
       [1.0, Timestamp('2013-01-02 00:00:00'), 1.0, 3, 'train', 'foo']],
      dtype=object)
#this arary contains integers, strings, and floats; 
#each column contains the same dtype, this is an expensive operation
```

DataFrame to numpy does not include labels or indexes.

Pandas allows for many more operations including merging, selection, grouping, reshaping, and more. All detailed on [PANDAS](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html) website.

## Things I would like to know more about:

What are the real world applications for using Pandas and Numpy?