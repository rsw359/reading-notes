# *Class 05 Reading Notes*

## Chapter 3: “Object Literals”

### Objects

- Objects group together variable and funtions
  - Within an object, variables are called properties
  - Within an object, functions are called methods
  - The names of properties and methods are called keys and must be unique
  - The value of a property can be a string, number, boolean, array, or another object
  - The value of at method is always a function
  - A 'key/value' pair is the name of an object and the value it holds(`key`age : 40`value`)
  - The object is the data contained within curly braces, var `Jim`{(`key`age : 40`value`)} Jim is the object
  - the properties or methods can be access using dot notation i.e. var jimAge = jim.name;
    - square brackets can also be used i.e. var jimAge = jim['name'];

### DOM

- The Document Object Model specifies how an html page should be represented, and how JavaScript can access and update the data
- It is neither html or javascript
- The DOM uses a model composed of objects called the DOM tree to create a model of the html page
- The DOM is often called an API and allows communication between programs, and allows use of a UI
- The Dom consists of 4 kinds of nodes
  - The Document node, which is added to the top of the tree. every following element has its own node on the Dom tree
  - Element nodes hold the elements on the page
  - Attributes are represented in the Attribute node
      -Text is also stored within its own node
- These nodes can be accessed by locating the desired node, then  using its text, child elements, and attributes

## *Common Methods*

  1. getElementById() - Uses and elements id attribute
  2. querySelector() - Uses a css selector, and returns the first matching element
  3. getElementsByClassName() - Selects all elements of a specific class name
  4. getElementsByTagName() - Selects all elements of a specific tag name
  5. querySelectorAll() - Uses a css selector, and returns all matchinfg elements
  6. parentNode() - Selects the parent of the current element node
  7. previousSibling/nextSibling() - Selects the previous or next sibling from the Dom tree
  8. firstChild/lastChild() - Selects the first or last child of the current element

  A node list is a collection of nodes. Some methods return node lists. The item() method allows a specific element to be selected from a node list. This can also be done using array syntax

- Methods that find elements in the Dom tree are called Dom Queries
- The Dom Tree can inspected in browsers

### These Notes WIll be further updated 
