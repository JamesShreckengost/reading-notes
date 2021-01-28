# Read: 14a - CSS Transforms, Transitions, and Animations
## What Google Learned From Its Quest to Build the Perfect Team
- Study groups carefully engineered by the school to foster tight bonds. Study groups have become a rite of passage at M.B.A. programs, a way for students to practuce working in teams and a reflection of the increasing demand for employees who can adriotly navigate group dynmaics.
- Seems as if people who study together and are genuiely trying to help each other work better than forced study groups.
- Feel like you can say anything to one another
- The bulk of modern work is more and more team-based
- In Silicon Valley, software engineers are encouraged to work together, in part because studied show that groups tend to innovate faster, see mistakes more quickly and find better solutions to problems.
- Google couldnt find matters in study or work groups
- How you treat your teammates matters
- Everyone gets a chance to talk
- good teams had "average social sensitivity"
- Do what you feel is right and be senstive towards others

## Transforms
- The transform property comes in two different settings, two-dimensional and three-dimensional. Each of these come with their own individual properties and values.
### Syntax
- The actual syntax for the transform property is quite simple, including the transform property followed by the value. The value specifies the transform type followed by a specific amount inside parentheses.

```javascript
div {
  -webkit-transform: scale(1.5);
     -moz-transform: scale(1.5);
       -o-transform: scale(1.5);
          transform: scale(1.5);
}
```
- Notice how the transform property includes multiple vendor prefixes to gain the best support across all browsers. 
- The un-prefixed declaration comes last to overwrite the prefixed versions, should a browser fully support the transform property.
### 2D Scale 
- Using the scale value within the transform property allows you to change the appeared size of an element. 
- The default scale value is 1, therefore any value between .99 and .01 makes ane element appear smaller while any value greater than or equal to 1.01 makes an element appear larger.
- It is possible to scale only the height or wdith of an element using the scaleX and scalY values.
- The scaleX value will scale the width of an element while the scaley Value will scale the heigh of an element but at different sizes, the x and y axis values may be set simultaneously. 
- To do so, use the scale transfrom declaring the x axis vlaue first, followed by a comma, and then the y axis.
### 2D Translate
- The translate value works a bit like that of relative positioning, pushing, and pulling an element in different directions without interrupting the normal flow of the document.
- Using the translateX value will change the position of an element on the horizontal axis while using the translateY value will change the position of an element.
- The distance values used within the translate value may be any general length measurement, most commonly pixels or percentages.
### 2D Skew
- The last transform value in the group, skew, is used to distort elements on the horizontal axis, vertical axis, or both.
- Using the skewX value distorts an element on the horitonal axis while the skewY value distorts an element on the vertical axis
- To distort an element on both axes the skew value is used, declaring the x axis value first, followed by a comma, and then the y acis value.
### Combining Transforms
- It is common for multiple transforms to be used at once, rotating and scaling the size of an element at the same time for example. 
- In this event multiple tranforms can be combined together.
- To combine transforms, list the transform values within the transform property one after the other with out the use of commas
- Using multiple transform declarations will not work, as each declaration will overwrite the one above it.
### Transform origin
- The transform origin property can accept one or two values. When only one value is specified, that value is used for both the horizontal and vertical axes. 
- If two values are specified, the first is used for the horizontal axis and the second is used for the vertical axis.
- Individually the values are treated like that of a background image position, using either a length or keyword value.

## Transitions and Animations
- With CSS3 tranisitions you have the potential to alter the appearance and behavoir of an element whenever a state change occurs, such as when it is hovered over, focused on, active, or targeted.
- Animations within CSS3 allow the appearance and behavior of an element to be altered in mulitple keyframes.
- Transitions provide a change from one state to another, while animations can set multiple points of transition upon different keyframes.
### Transitions
- For a transition to take place, an element must have a change in state, and different styles must be indentified for each state. 
- The easiest way for determining styles for different states is by using the :hover, :focus, :active, and :target psuedo-classes
- There are four transition properties in total
  - transition property, transition-duration, transition-timing-function, and transition-delay
### Transitional Property
- The transition-property property determines exactly what properties will be altered in conjunction with the other transitional properties. By default, all of the properties within an elemtent's different states will be altered upon change.
- However, only the properties indentified within the transition-property value will be affected by any transitions.
- Not all properties my be transitioned, only properties that have identifiable halfway points. 

### code examples link
For all code examples go to: 
[transforms](https://learn.shayhowe.com/advanced-html-css/css-transforms/)
              
### 8 simple CSS3 transitions to wow your users
link [8 simple CSS3 transitions to wow your users](http://www.webdesignerdepot.com/2014/05/8-simple-css3-transitions-that-will-wow-your-users)

- CSS3 has introduced countless possibilities for UX designers, and the best thing about them is that the cooelsts parts are really simple to implement.
1. Fade in
  - Having things fade in is a fairly common request from clients. It's a great way to emphasize functionality or draw attention to call to action.
2. Change color
  - Animating a change of color uused to be unbelievably complex, with all kinds of math invloved in calculating seperate RGB values and then recombining them.
3. Grow & Shrink
  - To grow an element, you used to have to use its width and height, or its padding.  But now we can use CSS3's transform to englarge.
4. Rotate Elements
  - CSS tranforms have a number of different uses, and of the best is transforming the rotation of an element.
5. Square to circle
  - A really popular effect at the moment is transitioning a sqaure element into round one, and vice versa. With CSS, it'sa simple effect to achieve, we just transition the border-radius property.
6. 3D Shadow
  - 3D shadows were frowned upon for a year or som becuase they weren't seen as compatible with flat design, wich is of course nonsense, they work fantastically well to give a user feedback on their interactions and work with flat, or fake 3D interfaces
  - This effect is achieved by adding a box shadow, and then moving the element on the x axis using the transform and translate properties so that it appears to grow out of the screen.
7. Swing
  - Not all elements use the transition property. We can also create highly complex animations using @keyframes, animation, and animation-iteration.
8. Inset Border
  - One of the hottest button styles right now is the ghost button; a button with no background and a heavy border.
  - We can of course add a border to an element simply, but that will change the element's position. We could fix that problem using box sizing, but a far simpler solution is the transition in border using an inset box shadow.

### 6 Buttons animated
  - link: (https://codepen.io/retyui/pen/ByoaXV)

### CSS3 Animations: KeyFrames
  - link: (https://codepen.io/akshaychauhan/pen/oAfae)

### 404
  - link (https://codepen.io/kieranfivestars/pen/MYdQxX)

### Pure CSS Bounce Animation
  - link (https://codepen.io/dp_lewis/pen/gCfBv)