# *Class 07 Reading Notes*

## *HTML & CSS*

## Tables

- There are for key elements for creating tables
  - The basic structure elements
    - The `<table>` element is used to create the table
    - The `<tr>` tag indicates the start of a table row
    - The `<td>` tag is used for storing the data in the table
  - The `<th>` tag is used for table headings for each column and shoud be used even if there is no content in the column
  - The colspan and rowspan attribute can be used to span  more than one column or row
  - The structure of the table can be built out with `<thead>`,`<tbody>`,and `<tfoot>`, each used for the headings, body, and footer of long tables respectively

## *JS & Jquery*

## Constructors

- Constructor notation can be used to create an empty object which then can be filled with data using dot notaion
  - i.e `let players = new Object();` `players.name = 'Jordan' 'players.team = Bulls'`, etc.
  - functions can be updated by using dot notation and adding a new value, this can also be done using bracket notation, but methods cannot be updated with brackets
  - Object constructors can use a template to create many objects at once using a function
    - i.e. function Players'(name, team, position)'
  - Then, instances of the object can be created using the constructor function and the 'new' keyword
    - i.e let teamPlayers = new Players('Jordan, 'Bulls', 'SG')
