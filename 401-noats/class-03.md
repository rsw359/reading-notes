# Class-03

## **FileIO & Exceptions**

Files on most modern file systems are composed of three main parts:

1. **Header:** metadata about the contents of the file (file name, size, type, and so on)
2. **Data:** contents of the file as written by the creator or editor
3. **End of file (EOF):** special character that indicates the end of the file

One problem often encountered when working with files. The American Standards Association (ASA)standard states that line endings should use the sequence of the Carriage Return (`CR`
 or `\r`) *and* the Line Feed (`LF` or `\n`) characters (`CR+LF` or `\r\n`).

Character encoding is a translation from byte data to human readable characters. The two most common encodings are the ASCII and UNICODE Formats.

****Opening and Closing a File in Python****

`file = open('file_name')`

When you’re manipulating a file, there are two ways that you can use to ensure that a file is closed properly, even when encountering an error. The first way to close a file is to use the `try-finally` block:

`reader = open('dog_breeds.txt')
try:
    # Further file processing goes here
finally:
    reader.close()`

The second (cleaner) way to close a file is to use the `[with` statement](https://realpython.com/python-with-statement/):

`with open('dog_breeds.txt') as reader:
    # Further file processing goes here`

the most commonly used modes:

| Character | Meaning |
| --- | --- |
| 'r' | Open for reading (default) |
| 'w' | Open for writing, truncating (overwriting) the file first |
| 'rb' or 'wb' | Open in binary mode (read/write using byte data) |

### **Iterating Over Each Line in the File**

A common thing to do while reading a file is to iterate over each line. Here’s an example of how to use the Python `.readline()` method to perform that iteration:

>>> with open('dog_breeds.txt', 'r') as reader:
>>>     # Read and print the entire file line by line
>>>     for line in reader:
>>>         print(line, end='')
Pug
Jack Russell Terrier
English Springer Spaniel
German Shepherd
Staffordshire Bull Terrier
Cavalier King Charles Spaniel
Golden Retriever
West Highland White Terrier
Boxer
Border Terrier

file objects have multiple methods that are useful for writing to a file:

| Method | What It Does |
| --- | --- |
| .write(string) | This writes the string to the file. |
| .writelines(seq) | This writes the sequence to the file. No line endings are appended to each sequence item. It’s up to you to add the appropriate line ending(s). |

### **Working With Bytes**

Sometimes, you may need to work with files using [byte strings](https://docs.python.org/3.7/glossary.html#term-bytes-like-object). This is done by adding the `'b'` character to the `mode` argument. All of the same methods for the file object apply. However, each of the methods expect and return a `bytes` object instead:

>>>

`>>> with open('dog_breeds.txt', 'rb') as reader:
>>>     print(reader.readline())
b'Pug\n'`

Taken from : [https://realpython.com/read-write-files-python/](https://realpython.com/read-write-files-python/)

---

## ****Exceptions versus Syntax Errors****

[S](https://realpython.com/invalid-syntax-python/)yntax errors occur when the parser detects an incorrect statement.

>>> print( 0 / 0 ))
  File "<stdin>", line 1
    print( 0 / 0 ))
                  ^
SyntaxError: invalid syntax

The arrow indicates where the parser ran into the **syntax error**. In this example, there was one bracket too many.

>>> print( 0 / 0)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: integer division or modulo by zero

This time, there was  an **exception error**. This type of error occurs whenever syntactically correct Python code results in an error. The last line of the message indicated what type of exception error you ran into.

Python details what type of exception error was encountered. In this case, it was a ZeroDivisionError.

## **Raising an Exception**

We can use `raise` to throw an exception if a condition occurs. The statement can be complemented with a custom exception.

x = 10
if x > 5:
    raise Exception('x should not exceed 5. The value of x was: {}'.format(x))

## **The try and except Block: Handling Exceptions**

The `try` and `except` block in Python is used to catch and handle exceptions. Python executes code following the `try` statement as a “normal” part of the program. The code that follows the `except` statement is the program’s response to any exceptions in the preceding `try` clause.

## **The else Clause**

In Python, using the `else` statement, you can instruct a program to execute a certain block of code only in the absence of exceptions.

## **Summing Up**

After seeing the difference between syntax errors and exceptions, you learned about various ways to raise, catch, and handle exceptions in Python. In this article, you saw the following options:

- `raise` allows you to throw an exception at any time.
- `assert` enables you to verify if a certain condition is met and throw an exception if it isn’t.
- In the `try` clause, all statements are executed until an exception is encountered.
- `except` is used to catch and handle the exception(s) that are encountered in the try clause.
- `else` lets you code sections that should run only when no exceptions are encountered in the try clause.
- `finally` enables you to execute sections of code that should always run, with or without any previously encountered exceptions.

Notes taken from [https://realpython.com/python-exceptions/](https://realpython.com/python-exceptions/)