# Class 08

## List Comprehension

List comprehension is a powerful and concise method for creating lists in Python that becomes essential the more you work with lists, and lists of lists.

my_new_list = [ *expression* for *item* in *list* ]

## Three necessary ingredients for List Comprehension

1. First is the expression we’d like to carry out. *expression* inside the square brackets.
2. Second is the object that the expression will work on. *item* inside the square brackets.
3. Finally, we need an iterable list of objects to build our new list from. *list* inside the square brackets.

An expression  can be carried out on each item in the list. The expression will determine what item is eventually stored in the output list.

In Python, list comprehensions are a more compact and flexible way of creating lists.

## **Example 1: Creating a list with list comprehensions: *RANGE***

```python
# construct a basic list using range() and list comprehensions
# syntax
# [ expression for item in list ]
digits = [x for x in range(10)]

print(digits)

#output
#[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

Example 1 use the **range()** method to generate a list of numbers. Python iterates through each item in that range, and saves a copy of the item in a new list called digits.

## **Example 2: Comparing list creation methods in Python**

```python
# create a list using a for loop
squares = []

for x in range(10):
    # raise x to the power of 2
    squares.append(x**2)

print(squares)
#Output
#[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```

Create a list and loop through it, and raise x^2

Now using List Comprehension:

```python
# create a list using list comprehension
squares = [x**2 for x in range(10)]

print(squares)
```

List Comprehension can greatly reduce the amount of code necessary to complete tasks in Python, allowing code to be more concise and readable.
