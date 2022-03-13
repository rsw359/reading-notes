# Class 01 *Reading Notes*

## *HTML & CSS*

## Chap. 1 *Html Structures*

       - Html pages are text documents that contain elements denoted by tags

        * Tags use angled brackets that describe the content writen between them. An opening <"_"> and closing </"_"> tag is usually necessary
        
        * The tags often contain attributes that can help with styling and identification of elements

## Chap. 8 *Extra Markup*

    - There have been several different versions of HTML. Attrributes and Elements vary</summary>
        - HTML4, XHTML, HTML5(current)
        - Doctype at the tope of the page indicates the version (this is not viewable by the user)

### Comments

    - HTML comments can are indicated by <!--"text"-->
        - Can be used to give helpful information about the code that follows, or to hide code from the browser 

### Attributes

#### *Global Attributes - ID & Class*

    - Used to identify particular elements
    - Allows for identification for use in CSS or JavaScript
    - Useable on any element in HTML (global attributes)

### Elements

    - Block Elements always start on a new line
        - <h>, <p>, <ul>, <li>
    - Inline Elements always continue the same line as the previous element
        - <a>, <b>, <em>, <img>
    - DIV element is used to organize groups of block elements
    - Span is used to organize groups of inline elements
    - Iframes are used to imbed content in the page (like maps)\
    - Meta is used to describe the page content to search engines 

### Escape Characters

    - Characters that have a purpose in the syntax of the code have a specific code assigned to them for use in the content of a page
        - < = &lt
        - " = &ldquo  (left quote)  
        - " = &rdquo (right quote)   

## Chap. 17 *HTML 5*

HTML 5 is the current version of HTML in 2022

### HTML 5 Elements

    - Headers and footers (top and bottom elements of a page) can include important information for the page
    - Nav is used for primary site navigation; Can be included in the header or footer of a page
    - Article and Aside are used for organizing content on the page
    - Section is used to group elements
    - Hgroup is used for grouping headers
    - Figure is used for images, videos, graphs, etc. (supporting content)

#### Note! : Blocks of text can be wrapped in the link attribute to turn the entire block into a link

## Chap. 18 *Process & Design*

Principle Ideas for the Design Process

## *Who:*

    - Keep the site's target audience in mind
        - Think about the demographics of potential visitors 
        - Come up with imaginary people using the appropriate demographics

## *Why:*

    - Think of the REASON users visit the site
        - What are the user's motivations and goals 
        - Use the imaginary visitors as examples 

## *What:*

    - Determine the most relevant information for the users
    - Prioritize levels of information > identify ESSENTIAL and NON-ESSENTIAL info 
      
       * If users don't view the site as relevant, they will move on

## *How:*

    - How often will a user visit the site?
    - How often does the site need to be updated to stay relevant?
    - How often are products/services updated?
       
        * These things will vary depending on the part of the site in question

## *Sitemaps*

    - Drawing a diagram to visualize the layout of a webpage can be helpful
                 [Main]
                    |        
        [About]  [Visit]  [Shop]
        |   |      |    |     |
      [So] [On] [And] [So] [Forth]

## *Wireframes*

        - These are a sketch of key info as it will apear on the site.
            - Should not contain style info - these are only a representation of the heirarchy of content
            - CAN be shown to clients to insure that all the desired functions are present

   *Online wireframe tools are available
    *see page 463 in HTML and CSS by Jon Duckett

## *Design Principles*

### *Visual Hierarchy:*

    - Helps to guide the viewer using:
        - SIze: large elements that draw the users attention
        - Color: bright colors also draw attention
        - Style: differentiating elements with styling helps them to stand out
        - Images: attract the eye 

### *Grouping:*

    - Helps to make the site easy to comprehend
        - Consistency is important the styling of specific types of information
        - Headings help users determine if blocks of information are relevant to them

### *Navigation:*

    - Primary navigation should be:
        - Concise: quick and easy to read
        - Limited in the number of options 
        - Interactive: responding to user interaction, i.e mouse hovering
        - Consistent in Style

## *JavaScript and JQuery*

 *Introduction*
JavaScript Makes The Web More Interactive

    - JavaScript makes webpages more interactive by allowing for
        
        - Allowing for the selection of content within an HTML page by id or class
        - Modification of content in an HTML page 
        - Specification of program rules by using scripts
        - Reaction to specified events such as a buttonpress, cursor behavior, intervals of time, etc.

## Chap. 1 *The ABC of Programming*

What Are Scripts and How Do I Write Them

### Scripts

    - A Script is a series of instructions that a computer can follow to accomplish a task or set of tasks
        - Computers can only understand scripts that use vocabulary they can understand
        - Computers can only understand scripts written using the correct syntax
        - Computers follow instructions in order, so the order of tasks is important

### How Do I write a script?

## *Objects and Properties*

    - Objects are representaions of real things
        - They can have their own:
            * Properties
            * Events
            * Methods
    - Properties are the characteristics of an object
        They have their own names and values

### *Example:*

| Object Type: Road Bike |
| ---------------------- |
| Maker: BMC             |
| Gears: 11 Speed        |
| Color: Black           |
| Wheels: Mavic          |
| Dopeness Scale: EXTRA DOPE|  |

## Methods

    - Methods contain the instructions that make the interaction with objects possible 
        - Methods tell the computer what to do with the object and can contain lots of instructions

### *Script Example:*

Console.log(value)

- the object is the Console
- the period is called the member operator
- log is the method: tells the computer to log, or write the following value to the console
- the value is what should be logged to the console.  

*Note:  The Computer would print the word "value" to the console
