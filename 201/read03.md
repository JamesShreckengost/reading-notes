# Reading 03 notes: HTML Lists, CSS Boxes, JS Control Flow
## (HTML) Chapter 3: “Lists” (pp.62-73)
- There are lots of occasions when we need to use lists. HTML provies us with three different types:
  - *Ordered lists* are lists where each item in the list is numbered. For example, the list might be a set of steps for a recipe that must be performed in order, or a legal contract where each point needs to be identified by a section number.
  - *Unordered lists* are lists that began with a bullet point (rather than characters that indicate order.)
  - *Definition lists* are made up of a set of terms along with the definitions for each of those terms.
### Ordered Lists
  - <ol>
    - The ordered list is created with the <ol> element. 
  - <li>
    - Each item in the list is placed between an opening <li> tag and a closing </li> tag. (The li stands for list item) 
### Unordered Lists 
  - <ul>
    - The unordered list is created with the <ul> element.
  - <li>
    - Each item in the list is placed between an opening <li> tag and a closing </li> tag. (The li stands for list item) 
### Definition Lists
  - <dl>
    - The definition lsit is created with the <dl> element and usually consists of a series of terms and their definition.
    - Inside the <dl> element you will usually see pairs of <dt> and <dd> elements.
  - <dt>
    - This is used to contain the term being defined (the definition term).
  - <dd>
    - This is used to contain the definition
    - Sometimes you might see a list where there are two terms used for the same definition or two different definitions for the same term. 
### Nested Lists
  - You can put a second list inside an <li> element to create a sublist or nested list. 
  - Browsers display nested lists indented further than the parent list. In nested ordered lists, the browser will usually change the style of the bullet point too.
### Summary 
- There are three types of HTML lists; ordered, unordered, and definition.
- Ordered  lists use numbers.
- Unordered lists use bullets.
- Definition lists are used to define terminology
- Lists can be nested inside one another.
## (HTML) Chapter 13: “Boxes” (pp.300-329)
- At the beginning of this section on CSS, you saw how CSS treats each HTML element as if it lives in its own box.
### Box Dimensions 
  - By default a box is sized just big enough to hold its contents. To set your own dimensions for a box you can use the height and width properties.
  - The most popular ways to specify the size of a box are to use pixels, percentages, or ems
### Limiting Width
  - Some page designs expand and shrink to fit the size of the user's screen.
  - The min-width property specifies the smallest size a box can be displayed at when the browser window is narrow
  - The max-width property indicates the maximum width a box can stretch to when the browser window is wide.
### Limited Height
  - In the same way that you might want to limit the width of a box on a page, you may also want to limit the height of it.
  - This is achieved using the min-height and max-height properties.
### Overflowing Content
  - The overflow property tells the browser what to do if the content contained within a box is larger than the box itself. 
  - It can have of two values.
  - hidden
    - This property simply hides any extra content that does not fit in the box.
  - scroll
    - This property adds a scrollbar to the box so that users can scroll to see the missing content.
    - Helps prevent overlapping
### Border, Margin & Padding
  - Every box has three available properties that can be adjusted to control its appearance:
    - Border:
      - Every box has a border (even if it is not visible or is specified to be 0 pixels wide). 
      - The border seperates the edge of one box from another
    - Margin:
      - Margin sit outside the edge of the border. 
      - You can set the width of a margin to create a gap between the borders of two adjacent boxes.
    - Padding: 
      - Paddding is the space between the border of a box and any content contained within it.
      - Adding padding can increase the readability of its contents
### White Space & Vertical Margin
  - The padding and margin properties and very helpful in addcing between various items on the page
### Border Width
  - The border-width property is used to control the width of a border.
  - The value of this property can either be given in picels or using on the following values
    - thin 
    - medium
    - thick
  - You can control the individual size of borders using for seperate properties:
    - border-top-width
    - boreder-right-width
    - border-bottom-width
    - border-left-width
  - you can also specify different width for the four border values in one property, like so:
    - border-width: 2px 1 px 1px
      2px:
### Border Style
   - You can control the style of a border using the border-style property. 
   - This property can take the following values:
    - *solid* a single solid line
    - *dotted* a series of square dots
    - *dashed* a series of short lines
    - *double* two solid lines
    - *groove* appears to be carved into the page
    - *ridge* appears to stick out from the page
    - *inset* appears embedded into the page
    - *outset* looks like it is coming out of the screen
    - *hidden/none* no border is shown
### Border Color
  - You can specify the color of a border using either RGB values, hex codes or CSS color names
  - It is possible to individually control the coolors of the borders on different sides of a box using:
    - border-top-color
    - border-right-color
    - border-bottom-color
    - border-left-color
### Shorthand
- The border property allows you to specift the width, style, and color of a border in one property.
### Padding
  - The Padding property allows you to specify how much space should appear between the content of an element and its border.
  - The value of this property is most often specified in pixels.
  - You can specify different values for each side of a box using:
    - padding-top
    - padding-right
    - padding-bottom
    - padding-left
### Margin
  - The margin property controls the gap between boxes.
  - Its Value is commmonly given in pixels.
  - You can specify values for side of a box using:
    - margin-top
    - margin-right
    - margin-bottom
    - margin-left
## (JavaScript) Chapter 2: “Basic JavaScript Instructions” (pp.70-73)
### Arrays
   - An array is a special type of variable.
   - It doesn't just store one value; it stores a list of values.
### Creating an Array
  - You create an array and give it a name just like you would any other variable.
### Values in Arrays
  - Values in an array are accesssed as if they are in a numbered list.
  - It is important to know that the numbering of this list starts at zero (not one).
  - Numbering Items in an Array
  - Accessing items in an Array
  - Number of items in an Array

## (JavaScript) Chapter 4: “Decisions and Loops” from switch statements on (pp.162-182)
### If... Else statements
  - The if..else statement checks a condititon.
  - If it resolves to true the first ode block is executed
  - If the condition resolcea to false the second code block is run instead
### Switch Statements
  - a switch statement starts with a variable called the switch value 
  - Each case indicates a possible value for this variable and the code that should run if the variable matches that value
### Type Coercion & weak typing
  - If you use a data type JavaScript did not expect, it tries to make sense of the operation rather than report an error
  - JavaScript can convert data types behind the scenes to complete an operation
### Type Truthy & False Values 
  - Due to type coercion, every value in JAvaScript can be treated as if it were true or false; and this ahas some interesting side effects
  - Falsy values are treated as if they are false.
  - The opposite would be true for Truthy values
### Loops
  - Loops check a condition. If it returns true, a code block will run. Then the condition will be checked again and if it still returns true, the code block will run again. It repeats tuntil the condition returns false. There are threee types of loops:
    - For: If you need to run code for s specific numnber of times, use a for loop
    - While: If you dont know how many times the code should run, use a while loop
    - Do while: Similary to while loop but condition will run once even if false.
### Summary
  - Conditional statements allow your code to make decisions about to do next.
  - Comparison operators (===, !==, ==, !=, <, >, <=, =>) are used to compare two operands
  - Logical operators allow you to combine more than one set of comparison operators.
  - if...else statements allow you to run one set of code if a ocondition is true, and another if it is false.
  - switch statements allow you to compare a value against possible outcomes(and also provide a default option if none match).
  - Data types can be coerced from one type to another.
  - All values evaluate to ether truthy or false.
  - There are three types of loop: ofr , while, and do...while. Each repeats a set of statements.