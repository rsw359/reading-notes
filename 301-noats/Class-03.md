# Class 03 *Reading Notes*

## React Lists and Keys

1. The Map() function takes in an array, and returns a new array that has been transformed by the function. It does not alter the original array

2. If we want to loop through an array and display each value in JSX, we can create a function that uses .map() and returns a list of the values cantained within the array that is passed into the function. We would need to use list item tags with the array name in curly braces, i.e `<li>{arrayName}</li>`

3. A key should be provided for each list item in the format: `<li key = {arrayName.toString()}>`. This should be passed as a property on the li tag

4. A key Allows React to keep track of what items have been modified. All items inside the map call need a key

## The Spread Operator

1. The spread operator is a syntax that expands an array into a list of objects. It is composed of an elipsis

2. The Spread operator is used for:
    - Copying an array
    - Concatenating or combining arrays
    - Adding an item to a list
    - Adding a state in React
    - And many other uses

3. In order to concatenate two arrays, this syntax is used:
      1. Declare the arrays : const arr1 = [1,2,3] const arr2 = [3,4,5]
      2. Declare the new array variable and include the array variables preceded by the spread elipsis: newArray = [...arr1, ...arr2]
  
4. In order to add an item to an array, this syntax is used:
      1. Declare the array : const arr1 = [1,2,3]
      2. Declare a new array variable and include new items followed by the original  array variable preceded by the spread elipsis: newArray = [3, 4, ...arr]

5. In order to add an item to an array, this syntax is used:
      1. Declare the objects : obj1 = {'a string'} obj2= {'another string'}
      2. Declare a new object variable and include the objects variables preceded by the spread elipsis: objOfObjs = [...obj1, ...obj2,]

## Passing Functions Between Components

1. The first thing is to create the function where it is going to be used

2. The increment function that the author creates loops through an array of objects and checks if the nmae that is passed as an argument  matches the name property of the item that has been mapped. If it does match, it will incrememnt a count and store the name in a variable that has been declared. It then updates the state of the component

3. In order to pass a function from parent to child using props i.e. (parent)variable={this.functionName}; (call it in the child)  this.props.functionName()

4. Then the function is invoked in the child by calling it using props : this.props.functionName(this.props.affectedProperty)
