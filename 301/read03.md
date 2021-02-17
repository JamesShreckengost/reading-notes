# Readings: MUSTACHE and FLEXBOX

## Templating with Mustache
### JavaScript Templating
- Fast and effcient way to render client-side view templates with JS by using a JSON data source.
- Template is HTML Markup, with added tags that will either insert variables or run programming logic
- The template engine replaces vars and instances declared in a template file with actual values at runtime, and convert the template into an HTML file sent to the client.
### Mustache
- A logic-less template syntax
- Works by expanding tags in a template using values provided in a hash or object.
- often reffered to as "logic-less" becuase there are no if statements, else clauses, or for loops. There are only tags.
- mustache.js is an implementation of the mustache template system in JS.
```javascript
Mustache.render(“Hello, {{name}}”, { name: “Sherlynn” });
// returns: Hello, Sherlynn
```
- The two braces around {{ name }} show that it is a placeholder
### Mustache Express
- To Configure mustache-express in your server.js/app.js/index.js file:
```js
var mustacheExpress = requre('mustache-express');
// Register '.mustache' extnesion with The Mustache Express
app.engine('html', mustacheExpress());

app.set('view engine', 'html');
app.set('views', _dirname + '/src/views');
```
source: [Templating With Mustache](https://1sherlynn.medium.com/javascript-templating-language-and-engine-mustache-js-with-node-and-express-f4c2530e73b2)
## A Guide to Flexbox
### Properties for the Parent
- Display: This defines a flex container; inline or block depending on the given value. It enables a flex content for all its direct children.
```css
.container {
  display: flex; /* on inline-flex */
}
```
- Order: By default, flex items are laid out in the source order. The order property controls the order in which they appear in the flex container.
```css
.item {
  order: 5; /* defualt is 0 */
}
```
- Flex-direction: This defines the main-axis thus defining the direction flex items are place in the flex container.
- Firebox is a single-direction layout concept.
- Think of it as laying out either in horizontal rows or vertical columns.
```css
.container {
  flex-direction: row | row-reverse | column | column-reverse;
}
```
- Row (default): lef to right in ltr: right to left in rtl
- Column: same as row but top to bottom
### Flex-grow
- Defines the ability for a flex itme to grow if necessary
- Accepts a unitless value that serves as a proportion
- Dictates what amount of the available space inside the flex container the item should take up
- If all items have flex-grow set to 1, remaining space in the container will be spaced equally to all children. If one of the children as a value of 2, the remaining space would try to take twice as much space as the other(or will try to)
```css
.item {
  flex-grow: 4; /* default */
  }
  ```
### Flex-wrap
- Flex items will all try to fit onto one line.
- You can change that and alll items to wrap as needed with this property
```css
.container {
  flex-wrap: nowrap | wrap | wrap-reverse:
}
```
- no wrap: all flex items will be on one line
- wrap: flex items will wrap onto multiple lines, top to bottom
- wrap-reverse: bottom to top
### Flex-shrink
- Defines the ability for a flex item to shrink if needed
```css
.item {
  flex-shrink: 3; /* default */
}
```
### Flex-flow
- Shorthand for the flex-direction and flex-wrap properties, which together define the flex container's main and cross axes. Default Value is row nowrap.
```css
.container {
  flex-flow: column wrap;
}
```
### Flex-basis
- Defines the default size of an element before the remaining space is distributed. 
```css
.item {
  flex-basis: | auto; /* default auto */
}
```
### Justify-content
- Defines the alignment along the main axis.
- Helps distribute extra free space leftover when either all the flex items on a inflexible, or are maximum size. 
- Exerts some control over the alignment of items when they overflow the line
```css
.container {
  justify-content: flex-start | flex-end | center | space-between | space-around | start | end;
} 
```
### Flex 
- Shorthand for flex-grow, flex-shrink and flex-basis combined. 
- The second and third parameters are optional.
- The shorthand sets the other vlaues intelligently
```css
.item {
  flex: none | [<'flex-grow'> <'flex-shrink'>? || <'flex-basis'>]
}
```
source: [A Guide To FlexBox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
## Flexbox Froggy