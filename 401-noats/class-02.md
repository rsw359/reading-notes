# Class-02

## **Testing and Modules**

### I****n Tests We Trust — TDD with Python****

TDD is the acronym for test driven development

- Unit tests are some pieces of code to exercise the input, the output and the behavior of your code. They can be written at anytime, but TDD tests the code from the beginning and throughout the entire coding process
- The tests can be as live documentation. It is necessary to be descriptive about it and to say what is expected and what we are testing. Variable names and test names should be explicit. The test file name should follow the same name of module name.
- It’s ideal to separate the tests folder from production code. A common structuring convention is the AAA convention: *Arrange, Act and Assert*.

The following is taken from [code.likeagirl.io](https://code.likeagirl.io/in-tests-we-trust-tdd-with-python-af69f47e6932):

- **Arrange**: you need to organize the data needed to execute the piece of code (input);
- **Act**: execute the code being tested (exercise the behavior);
- **Assert**: after executing the code, check if the result (output) is the same as expected.

Now you can execute the tests.

The cycle is consists of three steps:

- Write a unit test and make it fail (it needs to fail because the feature isn’t there, right? If this test passes, call the Ghostbusters, really)
- Write the feature and make the test pass! (you can dance after that)
- Refactor the code — the first version doesn’t need to be the beautiful one (don’t be shy)

### Consider **what is needed to make this test pass . Do**n’t think about the whole feature, just about the test

## **TDD is not about the money/tests**

TDD allows the software design to grow consciously.

- The greatest advantage about TDD is to craft the **software design first**
- Your code will be more **reliable**: after a change you can run your tests and be in peace
- Beginning may be hard — and that’s fine. You just need to **practice**!

---

## **What does the if**name**== “**main**”: do?**

Before executing code, Python interpreter reads source file and defines a few special variables/global variables.

If the python interpreter is running that module (the source file) as the main program, it sets the special **name** variable to have a value**“**main**”.**

**Advantages :**

1. Every Python module has its **name** defined and if it is the ‘**main**’, it implies that the module is being run standalone by the user and we can do corresponding appropriate actions.
2. If the script is imported as a module in another script, the **name** is set to the name of the script/module.
3. Python files can act as either reusable modules, or as standalone programs.
4. if **name** == “main”: is used to execute some code **only** if the file was run directly, and not imported.

Notes taken from [geeksforgeeks.com](https://www.geeksforgeeks.org/what-does-the-if-__name__-__main__-do/)

---

## **Recursion**

**Recursion is t**he process in which a function calls itself directly or indirectly. The corresponding function is called a recursive function. Using a recursive algorithm, certain problems can be solved quite easily.

### D**irect and indirect recursion**

A function is called directly recursive if it calls the same function i.e function_1(function_1).

 A function is called indirectly recursive if it calls another function. say function_2and function_3 call function_1 directly or indirectly.

### In recursion a stack is necessary. Each level of the stack depends on the previous level until the base condition is reached

In the Fibonacci sequence, the value of (n) is dependent on the sum of the previous two iterations.

n= (n-2) + (n-1)

If we create a function called fibonacci, we first have to define the base condition. In this sequence, the first two numbers are 0 and 1. Let’s use i for iteration

def fibonacci(i)

If i = 0

return 0

elif i = 1

return 1

(The base conditions are set)

else:

return fibonacci(i - 2) + fibonacci(i - 1)

Fibonacci( i ) refers to the index of the value, not the value itself

We can then recursively call the function

for x in range of (int input)

return fibonacci(int input)

## Things I want to know more about

I want to know how to apply recursion to other use cases. How can I, when see a problem, determine that recursion is necessary? Then, in turn, how do I formulate the function?
