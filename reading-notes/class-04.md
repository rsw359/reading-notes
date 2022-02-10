# Class 02 *Reading Notes*

## *-HTML & CSS-*

## Chap. 4 *Links*

- Links are used to take users from one page to another with just a click of the mouse

  - Links can be used to take users to other sites, or other pages within the same site using the `<a>` element and the href attribute

  - When linking to completely different websites the href attribute will need an absolute URL. But if linking to pages in the same site, the attribute can use a relative URL

    - Organization is very important to keep links clear and concise
    - Relative URLs  use directories in a parent/child/granchild arrangement
      - ../ is used to indicate the above folder
      - mailto; can be used to start up the user's email client
      - target_blank can be used to open a link in a new browser window

## Chap. 15 *Layout*

## *Key Concepts*

- Block Level Elements
  - h1, p, and list elements start on a new line and help influence the structure of the page

- Inline Elements
  - Img, b , and i elements flow between surrounding text

- Containing Elements
  - these are elements that contain other elements. they are called parent elements

- Positioning Schemes
  - Normal Flow- every block starts on a new line and never in line with each other
  - Relative positioning- this allows an element to move around without         affecting surrounding elements
  - Absolute positiong- causes an element to always be in the same place without relation to any surrounding content. It remains in place as users scroll
    - box offeset can be used to indicate where the element shoud be placed
  - Fixed positioning- is a for of absolute positioning, but in relation to the page window and not the container
  - Floating elements are taken out of the normal flow and become block level
    - z-index allow control of which element is on top

## *-JavaScript and JQuery-*

## Chap. 3 *Functions, Methods and Objects*

### Functions 

- Functions are a series of statements that are not executed until called for.
- functions consist of
        - A function keyword that is used to declare the function
        - A name or identifier
        - A block of code that resides in curly brackets
- Functions can contain various types of information
        - Some require parameters that may be stored elsewhere in the code
        - Some contain a single value to be used elswhere
        - Some contain arrays
- Functions can be declared by name or stored in a variable
- IIFE functions are executed as soon as the interpreter reaches them and are not given a name
- Functions operate with variables on a local or global scale. Local variable are only used within the function, whereas global variables can be used anywhere in the script
