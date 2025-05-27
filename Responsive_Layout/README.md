##information reference:
 Curso de Linkedin Education / Clarissa Peterson

[Responsive Layout ](https://www.linkedin.com/learning/responsive-layout/required-css?autoSkip=true&autoplay=true&resume=false)

#Notes:


##DISPLAY PROPERTY:

This has to do with how an element will take up space on the page. 
There are several different possible values, but these are the ones you'll use most often to do layouts, 
display: inline, block, inline-block, flex, and grid. 

-inline:

Inline elements are usually bits of text. 
For example, a span, a strong, an M element. 
Inline means the element is in line with other text and doesn't break the flow of text going from left to right. 
You can add margin and padding to an inline element, but it will remain in line with the other text, and these only effect the horizontal flow of text. 
You can't add vertical margin or padding. An inline element will also ignore a height or width attribute.

-block:

Block elements take up a block of area on the page. 
Examples are a paragraph, a H1, a dib, or structural elements like section or nab. Block elements by default take up the full width of space that's available, whether it's the width of the page or a containing element. 
You can change the width or the height of a block element with CSS. 
Every block element will always start on a new line by default. 

-inline-block:

Inline-block is kind of a combination of the two. The element appears inline like an inline element but you can give it a width or height style which will be followed, although it will stay in line.


-flex, and grid:

The last two values for display are flex and grid. 
These are special because they affect how all the elements inside them are displayed. They're used to create a flex box layout or a grid layout.

##POSITION PROPERTY:

The position property is used to move elements to different locations on a page. 
These are the different options for position that we will look at in this video: static, relative, absolute, fixed, and sticky. 
The default position is static.