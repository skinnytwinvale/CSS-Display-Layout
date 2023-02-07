# CSS-Display-Layout

## Display

display is CSS's most important property for controlling layout. Every element has a default display value depending on what type of element it is. The default for most elements is usually block or inline. A block element is often called a block-level element. An inline element is always just called an inline element.

These are four of the most commonly-used values for display:

- none - An element with a display property of none won't show up on the page.
- block - A block-level element starts on a new line and stretches out to the left and right as far as it
can; that is, by default it takes up all available horizontal space. Common block-level elements are div, p, and form. New in HTML5 are header, footer, section, and more.
- inline - An inline element can wrap some text inside a paragraph without disrupting the flow of that paragraph. span is the standard inline element, but there are others too, like strong, b, and em. The a element is often the most common inline element, since they are used for links. 
- inline-block - this value is sort of a hybrid of block and inline. To see how this works, let's look at an example.

the block-level elements both create new lines; were it not for the fixed width, they'd also take up all available horizontal space.

This is a general feature of inline elements: they don't respect the width and height property. If you set values for these properties on an inline element, those values will simply be ignored.

inline-block elements behave just like inline elements, except for the fact that you can set their width and height.

### Table / Table Cell

One family of values you'll sometimes see relates to table
formatting. Even though tables are supported natively in HTML using table, tr, td, and related elements, sometimes you'll want to position elements as though they were tables without actually using
these elements.

### Vertical Align

Most of the table values for the display property are not used very often.
One possible exception is the table-cell value, which can be used to vertically align an element to the middle of its container. In general, vertical alignment can be kind of a pain.

when an element's display is set to table-cell, it respects a new property, called vertical-align, which lets you adjust the vertical alignment of the element. Try commenting out the display properties in the two divs above, and see how that affects the layout.

## Floats

### Floats + Clearing

Another way to lay out a page, used specifically for moving elements to a certain side of the page, involves floats. 

Clear is an element adjacent to a float to move down to the next line. In other words, you might want the element to be cleared below the float. To see what this looks like, try setting clear: both; on the article.

## Positioning

Positioning allows you to take an element on the page and control where and how it's positioned relative to things such as its original starting position, other elements, or even the window itself. Depending on the type of positioning you use, the element will either remain in the document flow (relative) or be removed from the document flow (absolute, fixed), just like with floats.

Once position is set, offset values can be set for top, right, bottom, left, and z-index

By default, the position of an element is set to static. static positioning and relative positioning are basically the same, but with one important difference: a statically positioned element won't respond to
the offset properties listed above. elements that are positioned statically (which is the default positioning for elements) will not respond to top, left, right, bottom, or z-index.

### Absolute Positioning vs. Relative Positioning

Relative positioning, elements are not removed from the document flow, and any offsets you place on the element will be relative to its default position in the document flow.

Absolute positioning, the situation is a little different. In this case, the element is removed from the document flow, and any offsets you place on the element will be relative to its parent, provided its parent is not statically positioned! 

### Fixed positioning

This behaves similar to absolute positioning, but elements with fixed positioning are ALWAYS positioned relative to the active viewport. If you
position, for example, a fixed element with a top offset of 50 pixels and a right offset of 100 pixels, the top right corner of the element will be positioned 50 pixels over to the left and 100 pixels down. Unlike with absolute positioning, scrolling the page content would not affect this element's position at all.

## Flexbox

The CSS3 Flexible Box, or flexbox, is a layout mode providing for the arrangement of elements on a page such that the elements behave predictably when the page layout must accommodate different screen sizes and different display devices. For many applications, the flexible box model provides an improvement over the block model in that it does not use floats, nor do the flex container's margins collapse with the margins of its contents.

To start using flexbox, you need to set the display property of an element either to 

- flex or inline-flex to make your elements inline. (The distinction here is similar to the distinction between block and inline-block.

- flex-direction - with the row value this will layout items in a row, and with the column value it will lay elements out in a column. The default value is row. These values can also have a -reverse added to them (row-reverse / column-reverse ) to reverse the ordering.

- justify-content - this affects the space along the flex-direction. You can think of this as the horizontal alignment:
- - left -> flex-start
- - center -> center
- - right -> flex-end
- - even amount of space between elements -> space-between - even amount of space around elements -> space-around
- - even amount of space between elements -> space-between - even amount of space around elements -> space-around

Note that when the flex-direction is column or column-reverse, justify-content refers to the vertical axis, not the horizontal.

- align-items - this affects the space perpendicular to flex-direction. You can think of this as the vertical alignment:
- - top -> flex-start - center -> center
- - bottom -> flex-end

<img width="727" alt="Screenshot 2023-02-07 at 6 24 16 PM" src="https://user-images.githubusercontent.com/101606295/217390232-f84ffe9e-5ad7-417d-8317-cb8058954de4.png">



