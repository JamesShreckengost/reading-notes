# Read: 01 - SMACSS and Responsive Web Design

## Shay Howe’s intro to RWD
### Responsive Web Design 
- With the growth in mobile Internet usage comes the question of how to build websites suitbale for all users. The industry reponse to this question has become responsive web design, also known as RWD. 
### Responsive Overview
- Responsive web deign is the practice of bulding a website suitable to work on every device and every screen size, no matter how large or small, mobile or desktop.
- Responsive web design is focused around providing an inuituve and gratifying experinece for everyone. 
- No matter how large or small the viewport may be the Food Sense website adjust, creating a natural user experience.
#### Responsive vs Adaptive vs Mobile
- Responsive generally means to react quickly and positvely to any change
- adpative means to be easily modified for a new purpose or situation, such as change. 
- A combination of the two is ideal, providing the perfect formula for functional webites. 
- Mobile generally means to build a seperate website commonly on a new domain solely for mobile  useres.
- Currently the most popular technique lies within responsive web design, favoring design that dynamically adapts to different browser and device viewports changing layour rand content along the way.
### Flexible Layouts
- Responsive web deisgn is broken down into three main components, including flexible layouts, media queries, and flexible media. 
- The first part, flexible layouts, is the practice of building the layout of a website with a flexible grid, capble of dynamically resizing to any widht.
- Flexible grids are built using relative length units, most commonly percentages or em units.
#### Relative Viewport Lengths
- CSS3 introduced some new relative length untis, specifically related to the viewport size of the browser or device. These new units include vw, vh, vmin, and vmax. 
## All About Floats
### What is Float
- Float is a CSS postioning property. 
- In page layout programs, the boxes that hold the text can be told to honor the text wrapm or to ignore it.
- Floated elements remain a part of the flow of the web page.
- Absolutely positoned page elements will not affect the position of other elements and other elemtns will not affect them, whether they touched or not.
- There are four valid values for the floar property.
  - Left and Right float elements those directions respectively
  - None ensures the element will not float and Inherit which will assume the float value from that elements parent element
### What are floats used for?
- Aside from the simple example of wrapping text around images, floats can eb used to creat entire web layouts.
### Clearing the Float
- Float's sister property is clear. 
- An element that has the clear property set on it will not move up adjacent to the float like the float desires, but will move itself down past the float.
### Techniques for clearing floats
- If you are in a situation where you always know what the succeeding element is going to be, you can apply the clear: both; value to that element and go about your business.
  - The Empty Div Method
  - The Overflow Method
  - The Easy Clearing Method
### Problems with Floats 
- Pushdown
- Double Margin Bug 
- The 3px Jog
- Bottom MarginBug 
