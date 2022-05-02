# class 11

## [Jupyter Lab](https://www.youtube.com/watch?v=A5YyoCKxEOU)

JupyterLab is a web based UI that enables users to work with documents, code, images, video, and more. It supports many extensions and file formats including Markdown. It also supports kernel backed documents, such as Python. This allows code to be enabled within the notebook.

## Numpy

NumPy is a commonly used Python data analysis package.

NumPy allows us to work with multidimensional arrays that can be indexed by row and column.

We can create a NumPy array using the numpy.array
 function. If we pass in a list of lists, it will automatically create a NumPy array with the same number of rows and columns.

One of the limitations of NumPy is that all the elements in an array have to be of the same type.

The shape property will return the number of rows and columns.

Numpy.random.rand will create an array where each element is a random number.

It’s possible to use NumPy to directly read csv or other files into arrays using the numpy.genfromtxt function

NumPy is zero-indexed, meaning that the index of the first row is 0, and the index of the first column is `0`. If we want to work with the fourth row, we’d use index `3`, if we want to work with the second row, we’d use index `1`, and so on.

****Slicing NumPy Arrays****

The first items from a specific column, can be done using a colon.

A colon indicates that we want to select all the elements from the starting index up to but not including the ending index. This is called a slice.

```python
wines[0:3,3]

or

array([ 1.9, 2.6, 2.3])

"""it’s possible to omit the 0 to just retrieve all the elements from the beginning up to element 3:

wines[:3,3]
```

### **Assigning Values To NumPy Arrays**

We can also use indexing to assign values to certain elements in arrays. We can do this by assigning directly to the indexed value:

```python
wines[1,5] = 10
```

## Data Types

NumPy has several different data types, which mostly map to Python data types (Numpy is written in C). A few important ones are : float, int, string, object.

You can use the numpy.ndarray.astype method to convert an array to a different type. The method will actually copy the array, and return a new array with the specified data type.

Numpy  has many features for dealing with math operations, comparisons,  array methods and more. 

Notes taken from [https://www.dataquest.io/blog/numpy-tutorial-python/](https://www.dataquest.io/blog/numpy-tutorial-python/)
