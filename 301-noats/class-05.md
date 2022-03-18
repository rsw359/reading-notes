# Class 03 *Reading Notes*

## Thinking in React

1. The single responsibility principle is the idea that  a component should ideally only do one thing.
2. Building a static version of your app means to build a version that takes your data and renders the UI but has no interactivity.
3. After the static version is rendered, add state since it is reserved for the interactivity of the app
4. Three questions to ask about state are :
    - Is it passed in from a parent via props?
    - Does it remain unchanged over time?
    - Can you compute it based on any other state or props  in your component?
5. SOme steps to determine where the state should live in the app are:
    1. identify every component that renders something based on that state.

    2. Find a common owner component (a single component above all the components that need the state in the hierarchy).

    3. Either the common owner or another component higher up in the hierarchy should own the state.

    4. If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.

## Higher Order Functions

1. Higher order functions are functions that operate on other functions by taking them as arguments or by returning them

2. The greater than function in the reading takes in argument that and checks if the argument is greater than a specified number, then returns a true/false result

3. The map method applies a function to each item in an array, and builda a new array. At a higher level the reduce method computes a single value from an array, and combines it to the current value, summing up items in an array.
