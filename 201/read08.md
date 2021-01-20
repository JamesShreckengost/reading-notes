# Read: 08 - More CSS Layout
## HTML/CSS book, Ch. 15, “Layout” 
### Key concepts in positioning elements
- Building Blocks
  - CSS treats each HTML as if it is in its own box. This box will eithe be a block-level box or an inline box.
- Containing Elements
  - If one block-level sits inside another block-level element then the outer box is known as the containing or parent element.
### Controlling the poisition of an item
- CSS has the folowing positiong schemes that allwo you to control the layout of the page: normal flow, relative positioning, and absolute positioning. You can specify the positioning scheme using the position property in CSS. You can also float elements using the float property. 
- To indicate where a box should be positioned, you amy also need to use box offset propertues to tell the browser how far from the top or bottom and left or right it should be placed.
### Positioning
- Position: static
- position: relative
  - Relative positioning moves an element in relation to where it would have been in normal flow.
- position: absolute
  - when the position property is given a value of absolute, the box is taken outside of normal flow and no longer affects the position of other elements on the page.
- position fixed: Fixed positioning is a type of absolute positioning that requires that position property to have a value of fixed.
- z-index
  - if you want to control which element sits on top, you can use the z-index property.
### float
- The float property allows you to take an element in normal flow and place it as far to left or right of the containing elment as possible.
- clear
  - The clear propert allows you to say that no element should touch the left or righthand sides of a box. It can take the following values: left, right, both, none.
  - Many web pages use multiple columns in their design. This is achieved by using a <div> element to represent each column. The following are usde to position the column next to each other: width, float, margin.
  - Must think about what your web page is going on: phone, tablet, computer screen, monitor
### Layouts
- Fixed Width
  - Fixed width layout designs do not change size as the user increases or decreases the size of their window. Measurements tend to be given in pixels.
- liquid layouts
  - Liquid layout deisngs stretch and contract as the user increases or decreases the size of their browser window. They tend to use percentages.
- Layout grids 
  - Composition in any visual art is the placement or arrangment of visual elements - how they are orgainzed on a page. Many designers use a grid structure to help them position items on a page, and the same is true for web deisgners.
### CSS Framkeworks 
- Css framkeworks aim to make your life easier by providing the code for common tasks, such as creating layout grids, styling forms, creating printer friednly versions of pages and so on. You can include the CSS framework code in your projects rather than writing the CSS from scratch.
- a popular framework is 960.GS CSS framework
### Multiple Style Sheets 
- Some web pages split their CSS style rules into seperate style sheets. 
### Summary
- <div> elements are often used as containing elements to group together sections of a page.
- Browsers display pages in normal flow unless you specify relative , abssolute, or fixed postioning.
- The float property moves content to the left or right of the page and can be used to create multi-column layouts.
- Pages cane be fixed with or liquid (stretchy) layouts
- Designers keep pages within 960-1000 pixels wide, and indicate what the site is about within the top 600 pixels(to demonstrate its relevance without scrolling)
- Grids help create professional and flexible designs
- CSS Frameworks provide rules for common tasks
- You can include multiple CSS files in one page