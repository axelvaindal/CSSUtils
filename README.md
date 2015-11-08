# CSSUtils

## ABOUT

CSSUtils is a compilation of CSS classes designed to help developers in order to create proves of concept.
It provides classes about boxing, text, displaying and color rendering in css.

## AUTHORS

CSSUtils is maintained by Axel Vaindal.

## Contributors

There is actually no other contributors for this project. If you want to contribute, feel free to make any suggestions you want or to contact me.

## LICENCE

CSSUtils is available under the terms of the GNU GENERAL PUBLIC LICENSE. Check the licence file for more details.

## How does it work ?

CSSUtils is just a compilation. It provides you complete CSS for the simpliest tasks. You can use either the minified version for production development or the complete one for test development. In any case, classes provided are the same.

To include CSSUtils in your project, you just have to add the library with a classical `link`tag:

`<link rel="stylesheet" type="text/css" href="/path/to/lib/Utils.min.css">`

After the file being loaded in your application, you can add a class to any html component you want to change it.

For example, the class named `bg-facebookblue`, put a facebook-blue background color on an element:

	`<div class="bg-facebookblue"></div>`
	
The original library was in four parts, which you can find in the src directory. 
Each part has been concatened in one single file (Utils.css).
Sections above describe what you can do with each part of the library.

### Color.css

Color.css provides you classes for coloring functionalities.
You can find inside:

- Color managing, for text and other written element you can see in a html page,
- Background color, for any element, with position, repeat and attachment,
- Stroke color, for element whith edge to be colored
- Fill color, for any element with edge to be filled
- Border color, any border to be colored

Classes name are normalized.
To use color, just add the color name as the class name (see source to complete list of handled colors):

`<p class="red">Red text</p>`

To use background color, just add bg- plus the color name as the class name (all colors can be used as background color):

`<div class="red"></div>`

To use background repeat, attachment, or position, just add bg- plus the needed value as the class name (see source to complete list of handled value):

`<div class="bg-fixed"></div>`

To use stroke, just add str- plus the color name as the class name (all colors can be used as stroke color):

`<div class="str-red"></div>`

To use fill, just add fill- plus the color name as the class name (all colors can be used as fill color):

`<div class="fill-red"></div>`

To use border color, just add brd- plus the color name as the class name (all colors can be used as border color):

`<div class="brd-red"></div>`

Note that you can also set the opacity with the opacity-X class name.
To provide full opacity, use `opacity-full`.
To provide no opacity, use `no-opacity`.
Opacities are provided ten by ten, means that using `opacity-1` will provided a 0.1 opacity value to the element.

### Box.css

Box.css provides you classes for boxes in an html page.
You can find inside:

- Margin and padding classes, in every direction and the global ones,
- Width and height classes, up from 0 to 1000px, max, min and full value,
- Border width and line height classes, style and radius are also included,
- Table managing, vertical align and border appearance.


Classes name are normalized.
To use margin or padding, just add a mrg- or pdg- plus the value (from 0 to 1000, ten by ten).

`<div class="mrg-50 pdg-20"></div>`

You can also remove padding or margin by using `no-mrg` or `no-pdg`classes.
By the way, you can specify the margin or padding direction, by using mrg-X- or pdg-X- plus the value.
Letters are : t for top, l for left, b for bottom and r for right.

`<div class="mrg-l-20 mrg-t-10 pdg-r-60 no-pdg-l"></div>`

Width and weight work in the same way.
You can specify direction, and set to 0 with the same syntax as before.
You can prefix classes name with max- or min- in order to use max-width and max-height classes.

`<div class="max-wth-1000 min-hgt-1000 wth-1000 no-hgt"></div>`

Note that you can provide full width or full height, with the full-[max|min]-wth or full-[max|min]-hgt classes.

`<div class="full-wth full-hgt full-min-wth full-min-hgt"></div>`

Full width or full height provide a 100% width or height to elements.

All border classes start with brd- .
You can set border width, using brd- plus the Xp value, Xp being the width in pixel.
Example above, set a 5 pixel border width (you can up to 50 pixel max).
Note that you can also use brd-rad-Xp to provide a rounded border (up to 50 pixel max again).

`<div class="brd-5p brd-rad-2p"></div>`

You can set border style using, brd- plus the style name you wanna use.

`<div class="brd-10p brd-red brd-rad-3p brd-dashed"></div>`

### Text.css

Text.css provides you classes for text such as font or text transformation.
You can find inside:

- Text sizing, in pixel and em, text-alignment, text-indent
- Line height, in pixel,
- Text decoration, transformation, font-style weight and variant,
- Wrap and white spaces
- Fonts classes

Classes name are normalized.
You can use either txt-Xp or txt-Xv to change text sizing. Xp is the size in pixel (up from 0 to 50, as usual) and Xv is the em factor (from 1 to 10).

`<p class="txt-x2">Double size text.</p>`

`<p class="txt-12p">12 pixel size text.</p>`

You can use, txt- plus position to align the text in a desired position (these are bootstrap equivalent for text-[position]).

`<p class="txt-center">Text is centered.</p>`

You can use txt-ind- plus value to add a text indent, value up from 0 to 1000 px.

`<p class="txt-ind-50">Text is indented up to 50px.</p>`

You can use line-h-Xp, to change line height. Xp is the size in pixel (up from 0 to 50, as usual).

`<p class="line-h-20p">Line height is 20px.</p>`

Text decoration classes are provided as the class name is the decoration you want to apply. The same goes for text transformation, font style weight & variant, wrap & white spaces.

`<p class="underline capitalize bold"> This text is underlined, capitalized and bold.</p>`

Font classes have font name as class name.

`<p class="arial-black">Arial-black text.</p>`

### Display.css

Display.css provides you classes for block or inline element in an html page.
You can find inside:

- Displaying classes, to change element in block, inline, etc.
- Visibility classes, to change element visibility
- Overflow classes, to change element behaviour in overflow,
- Floating classes, to add floating at any element
- Postion classes, to modify element's position (see tutorial above to understand what it really means)
- Z-index classes, to add a z-index value at any element
- Cursor classes, to change cursor appearance

Classes name are normalized.
Displaying classes all start with dsp- followed by the display value.

`<div class="dsp-inline"></div>`

Visibility classes are named as is- plus the visibility. These are NOT aliases for hide and show from the Twitter bootstrap considered that hide and show use display value and visibility is something different. Please, read W3C documentation about differences between display and visibility values.

`<p class="is-hidden">Hidden text</p>`

Overflow classes are named as value-ovf , where value is the overflow behaviour you want. The same goes for float and clear classes (where value is the direction).

`<p class="scroll-ovf min-hgt-500 left-float"></p>`

Position classes are named as is- plus the position type. 
BE CAREFUL WHEN USING THESE CLASSES ! You have to understand completely what relative or absolue positionning mean before trying to dynamically change the position type of the element. See W3C specification before doing this.

`<div class="is-relative"></div>`

You can then use specific position classes to change where elements are rendered in the page.

`<div class="is-relative top-20 left-50 bottom-60"></div>`

You can also specify a Z-index value, using zX, X being the value (from 1 to 99).

`<a href="#" class="btn btn-primary z99">Always on top</a>`

Finally, you can change cursor appearance, using crs- plus the desired appearance.

`<div class="crs-pointer"></div>`

Version 2.0.0 (08/11/2015)
----------------------------
Second release

Version 1.0.0 (08/08/2015)
----------------------------
Firt release
