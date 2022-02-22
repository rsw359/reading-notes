# Class 12 Reading Notes

## Chart.js API

Chart.js is a JavaScript plugin that allows developers to instantiate charts in an HTML doc using the canvas element

    - It is possible to  create pie charts and line graphs with styling in html with the plugin. There are many options listed in the documentation.

### The Canvas Element

    - The canvas element has only two attributes, height and width. These can be set directly in html
    - The canvas element requires a closing tag
    - Class and id can be specified
    - The canvas element can be styled just like any other without affecting the image contained in the canvas
    - Fallback content can be inserted within the canvas tag so that browsers that dont support canvas have something to render
    - The canvas element is empty by default, and required scripts to render context and draw on it

### Drawing shapes

- fillRect(x, y, width, height) draws a filled rectangle
- strokeRect(x, y, width, height) draws a rectanglular outline
- clearRect(x, y, width, height) makes the specified area fully transparent
- A path is a list of points and is created using these functions:
  - beginPath() creates a new path
  - closePaths() Adds a straight line to the path in the direction of the sub path
  - stroke() draws the outline of the shape
  - fill() fille the paths content area
  - moveTo() moves the pen to specific x,y coordinates
  - lineTo() drawas a line from the current postition to the specified coordinates
- Arc, beziers, curves, and many other shapes can be drawn
- fillStyle() and strokeStyle() can be used to add color
- Line styles and widths can also be applied using various methods
- fillText() and strokeText() can be used to render text. Styles and colors can also be added to these
