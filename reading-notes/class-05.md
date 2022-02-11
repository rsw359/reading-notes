# Class 02 *Reading Notes*

## *-HTML & CSS-*

## Chap. 5 *Images*

- site organiztion is important, it is recommended to keep images in a separate folder for quick access

        * Images use the `<img>` tag (this is an empty tag)
        
        * the `<img>` tag must have the src attribute with a URL; it also can hold the 'title', 'height', and 'width' attributes

        * As the `<img>` tag is an inline element, the position of the tag in the document is important since block level elements, such as `<p>` content will flow around it

        * The align property align images by pixels. They can be aligned left, top, right, middle, and bottom 

        * Images should be saved in the right format (jpg, png, and gifs), size in pixels for the inteded screen size

        * Captions can be added to images using the `<figcaption>` tag. Images and captions can be stored together inside the `<figure>` element

## Chap. 11 *Color*

Foreground and background colors can be added to a page using CSS in a few ways

        * RGB
        
        * Hex

        * Color names

        * HSL(hue, saturation, lightness)

        - Opacity can also be adjusted in CSS

## Chap. 12 *Text*

Text can be styled in a few ways
        - Font type is specified using the font face property
        - Font sizes can be adjusted using pixels, percentage, or ems
        - Various fonts can be added using @fontface and then specifying the type of font file to be loaded

### Text Styles

        - Text can be styled in many ways. A few are:

        * font-weight (bold)
        * font-style (italic)
        * text-transform (upper and lowercase)
        * text-decoration (underline)

## JPG vs PNG vs GIF

        - There are 3 formats for images
          - Jpg - most useful for natural scenes (lossy)(supports 16 million colors)
          - Png - most useful for images with sharp lines and high contrast, such as logos (lossless)(color support varies depending on the format)
          - Gif - most useful for animated images