# Class 09

## ****What Are Dunder Methods?****

In Python, Dunder Methods are special predefined methods start and end with double underscores, for example __init__ and **str__**

Dunder methods let you emulate the behavior of built-in types. For example, to get the length of a string you can call `len('string').`

But an empty class definition doesn’t support this behavior out of the box. To fix this, you can add a `__len__`dunder method to your class:

```python
class LenSupport:
    def __len__(self):
        return 42

>>> obj = LenSupport()
>>> len(obj)
42
```

## ****Object Initialization: `__init__`**

To construct class objects in Python, the  `__init__` dunder is necessary. 

The constructor takes care of setting up the object.

## **Object Representation: `__str__`, `__repr__`**

It’s common practice in Python to provide a string representation of your object for the consumer of your class (a bit like API documentation.) There are two ways to do this using dunder methods:

1. **`__repr__`**: The “official” string representation of an object. This is how you would make an object of the class. The goal of `__repr__` is to be unambiguous.
2. **`__str__`**: The “informal” or nicely printable string representation of an object. This is for the enduser.

## ****Basic Statistics in Python — Probability****

## ****What is probability?****

At the most basic level, probability seeks to answer the question, “What is the chance of an event happening?” An **event** is some outcome of interest. To calculate the chance of an event happening, we also need to consider all the other events that can occur. 

When dealing with data, a good understanding of probability is necessary.

## VIDEO on Probability

[Intro to Statistics](https://www.youtube.com/watch?v=MdHtK7CWpCQ)

Also be careful when choosing people to listen to on the Internet! I suppose the probability of being scammed is high!
