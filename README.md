# CSSUtils

## ABOUT

CSSUtils is a package of CSS libraries in order to help in building a design website. Sections above present what is handled and how does it work.

## AUTHORS

CSSUtils is maintained by Axel Vaindal.

## Contributors

There is actually no other contributors for this project. If you want to contribute, feel free to make any suggestions you want or to contact me.

## LICENCE

CSSUtils is available under the terms of the GNU GENERAL PUBLIC LICENSE. Check the licence file for more details.

## How does it work ?

CSSUtils is just a package. It provides you complete CSS for the simpliest tasks. For instance, Colors.css provides you classes for coloring functionalities.
To use it, you just have to put this inline in your web project :
	`<link rel="stylesheet" type="text/css" href="/path/to/lib/colors.min.css">`

You should always use the production minified file considering it is smaller and you should'nt add any line in the libraries.
After the file being loaded in your application, you can add a class to any html component you want to change it.

For example :

	`<div class="bg-facebookblue"></div>`
would create a div with a facebookblue background-color.

### Colors.css

As said ahead, colors.css provides you classes for coloring functionalities.
Currently, there are :

- Color (for text)
- Background color
- Stroke color
- Fill color
- Border color

Classes names are normalized :

- Color : just the color name, for instance -> .red, .blue, .green, .salmon, .midnightblue, .darkslategray
- Background color : bg- plus the color name, for instance -> .bg-red, .bg-blue, .bg-green, .bg-salmon, .bg-midnightblue, .bg-darkslategray
- Stroke color : str- plus the color name, for instance -> .str-red, .str-blue, .str-green, .str-salmon, .str-midnightblue, .str-darkslategray
- Fill color : fill- plus the color name, for instance -> .fill-red, .fill-blue, .fill-green, .fill-salmon, .fill-midnightblue, .fill-darkslategray
- Border color : brd- plus the color name, for instance -> .brd-red, .brd-blue, .brd-green, .brd-salmon, .brd-midnightblue, .brd-darkslategray

### Boxes.css

Boxes.css provides you classes for margin and padding for box in an html page.
Classes names are normalized  :

- Margin classes are named .mrg- , then you add the first letter of the direction, then the decades, for instance -> .mrg-b-10, .mrg-l-50
- Padding classes are name .pdg- with the same rules as for margin classes
- Use .auto-mrg- and .auto-pdg- for auto margin or padding in the selected direction
- Une .no-mrg- and .no-pdg- for no margin or padding in the selected direction

### Fonts.css

Fonts.css provides you classes for text such as font classes or text transformation classes.
Classes names are normalized :

- Font classes are name with the font name, for instance -> .times-new-roman, .arial, .helvetica, ...
- Text transformation classes are name with the transformation, for instance -> .capitalize, .underline, ...

### Display.css

Display.css provides you classes for block or inline element in an html page.
Classes names are normalized and named as their CSS equivalent property name, for instance -> .visible, .hidden, .block, ...

Version 1.0.0 (08/08/2015)
----------------------------
Firt release