# Class 02 *Reading Notes*

## *-HTML & CSS-*

## Chap. 2 *Text*

### Html pages are text documents that contain elements denoted by tags

    - Markup Types

        * Structural: Headings and Paragraphs
            - Headings use <h1> through <h6> (H1 being the largest, H6 the smallest)
            - Paragraphs use the <p> tag
            - Bold and italics use <b> and <i> tags respectively
            - Superscript and Subscript use <sup> and <sub> tags respectively
            - Break and Horizontal Rule use <br> and <hr> respectively

        * Semantic: Extra Information
            - Content that has strong imprtance can be marked with the <strong> tag and will be displayed in bold
            - Content that needs to be emphasized can be marked with the <em> tag and will be displayed in italics
            - Paragraphs that need quotation marks can be marked with the <blockquote>; <q> can also be used, but doesn't display in IE
            - Abbreviations and acronyms can use the <abbr> element to make a pop-up with the full term to be displayed
            - References can be marked with the <cite> tag and will be displayed in italics; This should not be used for names
            - Definitions can be marked with the <dfn> tag the on their defining instance

## Chap. 10 *Introducing CSS*

### CSS associates style rules that govern how HTML elements should be displayed

    - CSS Rules contain two parts : a selector and declaration

        * Declarations sit inside of curly brackets and is made up of:
            - properties
            - values
        - One declaration can contain multiple properties as long as they are separated by a semicolon
        - Html pages and the CSS file can be linked using the <link> element
        - Internal styling can be placed in an HTML file using the <style> element

        - Selectors:
            - Universal Selector : Applies to all elements * {}
            - Type Selector : Matches element names h1 {}
            - Class Selector : Matches the element specified after the period .note {}
            - ID Selector : Matches the element specified after the hash #intro {}
            - Child Selector : Matches an element that is a child of another li>a {}
            - Descendant Selector : Matches an element that is a descendant of another p a {}
            - Adjacent Sibling Selector : Matches an element that is the next sibling of another h1+p {}
            - General Sibling Selector : Matches an element that is the sibling of another regardless of order h1~p {}

        
        * 

## *-JavaScript and JQuery-*

## Chap. 2 *Basic JavaScript Instructions*

### Variables

    Variables contain information that are necessary for scripts to run
        - Necessary parts of a variable are:
            - Variable keyword i.e. var, let
            - Variable name or identifier
            - Value or information contained within the variable
        - Data Types
            - Numbers : numberOfFingers = 11
            - Strings - text contained within single or dubble quotes : let myName = 'D'squarius"
            - Boolean - True/False values roomsAvail= true

#### *Arrays*

    - An array is a variable that stores a list of values. The data in an array do not have to be of the same data type

    - Values in an array
        - Items are numbered starting from zero
        - Items are retrieved by calling the array name and the item number
        - The length of an array can be determined by calling the array name plus ".length"

#### *Expressions*

    - Expressions result in a single value by"
        - Assigning a single value to a variable using the assignment operator ' = '
        - Using two ore more values to return a sinlgle value
            - Such as using an arithmatic operator ' + 'or ' - ', etc.
            - Or using comparison (>) or logical (&&) operators

## Chap. 4 *Decisions and Loops*

### *Decisions*

    - Decisions are made in code as a result of evaluations
        - Evaluating conditions - the code checks to see if the value of the script is true or false (often by using a comparative)
        - Conditional Statements - if/then/else statements check if the condition is met, then executes a function
        - Conditions are evaluated by using operands and operators
        - Operands can contain multiple values or variable names
