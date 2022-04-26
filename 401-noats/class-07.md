# Class 07

## ****The Global Statement****

To make a function have global scope in Python, the Global Statement can be used.

All the names that you list in a global statement will be mapped to the global or module scope in which you define them.

The use of global is considered bad practice in general. If possible, stop and think if there is a better way to write your code.

You can also use a global statement to create lazy global names by declaring them inside a function. However, this should be avoided.

Using a global statement at the top level of a module is legal, but it doesn’t make much sense because any name assigned in the global scope is already a global name by definition

## ****The Nonlocal Statement****

Similarly to global names, nonlocal names can be accessed from inner functions, but not assigned or updated. If you want to modify them, then you need to use a nonlocal **statement**. With a nonlocal statement, you can define a list of names that are going to be treated as nonlocal.

The nonlocal statement consists of the nonlocal keyword followed by one or more names separated by commas. These names will refer to the same names in the enclosing Python scope.

With the nonlocal statement, you tell Python that you’ll be modifying an object
 inside a nested function.

Unlike global, you can’t use nonlocal outside of a nested or enclosed function. To be more precise, you can’t use a nonlocal statement in either the global scope or in a local scope.

Here, you first try to use a nonlocal statement in the global Python scope. Since nonlocal only works inside an inner or nested function, a syntax error will be raised telling you that you can’t use nonlocal in a module scope.  In addition, nonlocal doesn’t work inside a local scope either.

## [BIG O VIDEO](https://youtu.be/5Uqawfl0VHQ)