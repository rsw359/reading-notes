# Class 02 *Reading Notes*

## *-HTML & CSS-*

## Chap. 3 *Lists*

There are 3 kinds of lists
    - Ordered lists <ol> ordered by number
    - Unordered lists <ul> not ordered with bullets
        - List items are nested using the <li> tag for each item
    - Definition lists <dl> 
        - nested definition terms <dt>
        -nested definitions <dd>


## Chap. 13 *Boxes*

CSS treats HTML elements as if they live in their own individual box
    - The width and height of the boxes can be controlled by percentage and pixels, among other methods
    -If content is too large to fit into the box, the overflow property can be used to instruct the browser how to display the content
    - Every box has three properties that can be used to style its appearance:
        -A border that exists outside the box
        - Margins that sit outsidre the border
        - Padding between the border and the content within
            *These can be displayed with various styles and colors in CSS
            *There are inline and block properties that can change the behavior of the element
            *Visibility can also be manipulated using the visibility property
            *Shapes around the corners can also be manipulated using the border-radius property
            *Images can also be created around the borders

## *-JavaScript and JQuery-*

## Chap. 4 *Decisions and Loops*

### *Switch Statements*

    - Switch statements differ form if../else statements in that they have multiple possible values that are checked, with different code run for different values
    - Once a match is found the statement stops the code from running, if statements must all be checked regardless of value
       
        1. The switch variable name is called: switch(name)
        2. The cases are evaluated
        3. Once a match is found, the appropriate code is run, then the operators 'short- circuit' (stop)

### Other Stuff

    - Type Coercion 
        - JavaScript has the ability to convert data types in the background, this is called weak type
            - It is good practice to use strict equals operators === and !== when comparing values
            - In Javascript there are some situations when values are treated as false, or falsy
                - Boolean False 
                - Zero
                - Emtpy values 
                - Variables without values
                -NaN (not a number)
            -Everything else is Truthy

    - Loops
        There are 3 types of loops
            - For loops: run code a specified number of times using a counter
                - for ( let i = 0; i < 10; i++ ) { 'do something'}
            - While loops: run the code as long as the condition is present 
                - while (i < 10) { 'do something'}
            - Do..while loops: similar to while loops, but will run all the code
                - do {something}
                    while (1<10)
