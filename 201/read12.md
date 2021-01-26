# Read: 12 - Docs for the HTML <canvas> Element & Chart.js
## Chart.js docs
- Charts are far better for displaying data visually than tables and have the added benefit that no one is ever going to press-gang them into use as a layout tool. They're easier to look at and convey data quickly, but they're not always easy to create.
- a JavaScript plugin that uses HTML5's canvas element to draw the graph onto the page. 
### Setting up
- This first thing we need to do is downlaod chat.js.
```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8" />
        <title>Chart.js demo</title>
        <script src='Chart.min.js'></script>
    </head>
    <body>
    </body>
</html>
```
### Drawing a line on a chart
- To draw a line chart, the first thing we need to do is create a canvas element in our HTML in which Chart.js can draw our chart.
```HTML
<canvas id="buyers" width="600" height="400"></canvas>
```
- We need to write a script that will retrieve the context of the canvas, so add this to the foot of your body element:
```html
<script>
    var buyers = document.getElementById('buyers').getContext('2d');
    new Chart(buyers).Line(buyerData);
</script>
```
### Conclusion
```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8" />
        <title>Chart.js demo</title>
        <!-- import plugin script -->
        <script src='Chart.min.js'></script>
    </head>
    <body>
        <!-- line chart canvas element -->
        <canvas id="buyers" width="600" height="400"></canvas>
        <!-- pie chart canvas element -->
        <canvas id="countries" width="600" height="400"></canvas>
        <!-- bar chart canvas element -->
        <canvas id="income" width="600" height="400"></canvas>
        <script>
            // line chart data
            var buyerData = {
                labels : ["January","February","March","April","May","June"],
                datasets : [
                {
                    fillColor : "rgba(172,194,132,0.4)",
                    strokeColor : "#ACC26D",
                    pointColor : "#fff",
                    pointStrokeColor : "#9DB86D",
                    data : [203,156,99,251,305,247]
                }
            ]
            }
            // get line chart canvas
            var buyers = document.getElementById('buyers').getContext('2d');
            // draw line chart
            new Chart(buyers).Line(buyerData);
            // pie chart data
            var pieData = [
                {
                    value: 20,
                    color:"#878BB6"
                },
                {
                    value : 40,
                    color : "#4ACAB4"
                },
                {
                    value : 10,
                    color : "#FF8153"
                },
                {
                    value : 30,
                    color : "#FFEA88"
                }
            ];
            // pie chart options
            var pieOptions = {
                 segmentShowStroke : false,
                 animateScale : true
            }
            // get pie chart canvas
            var countries= document.getElementById("countries").getContext("2d");
            // draw pie chart
            new Chart(countries).Pie(pieData, pieOptions);
            // bar chart data
            var barData = {
                labels : ["January","February","March","April","May","June"],
                datasets : [
                    {
                        fillColor : "#48A497",
                        strokeColor : "#48A4D1",
                        data : [456,479,324,569,702,600]
                    },
                    {
                        fillColor : "rgba(73,188,170,0.4)",
                        strokeColor : "rgba(72,174,209,0.4)",
                        data : [364,504,605,400,345,320]
                    }
                ]
            }
            // get bar chart canvas
            var income = document.getElementById("income").getContext("2d");
            // draw bar chart
            new Chart(income).Bar(barData);
        </script>
    </body>
</html>
```
## Basic usage of Canvas
- At first sight a <canvas> looks like the <img> element, with the only clear difference being that it doesn't have the src and alt attributes.
- the <canvas> element has only two attributes, width and height. These are both optional and can also be set using DOM properties. 
- The <canvas> element can be styled just like any normal image (margin, border, background...)
### Fallback Content
- The <canvas> element differs from <img> tag in that, for <video> , <audio>, or <picture> elements, it is easy to define some fallback content, to be displayed in older browsers not supporting it, like version of internet explorer earlier than version 9 or textual browsers.
### Required </canvas> tag
- The <canvas> element requires the closing tag (</canvas>). If this tag is not present, the rest of the document would be considered the fallback content and wouldn't be displayed.
  - Rendering context
    - The <canvas> element creates a fixed-size drawing surface that exposes one or more rendering contexts, which are used to create and manipulate the content shown
### A simple example
```html
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8"/>
  <script type="application/javascript">
    function draw() {
      var canvas = document.getElementById('canvas');
      if (canvas.getContext) {
        var ctx = canvas.getContext('2d');

        ctx.fillStyle = 'rgb(200, 0, 0)';
        ctx.fillRect(10, 10, 50, 50);

        ctx.fillStyle = 'rgba(0, 0, 200, 0.5)';
        ctx.fillRect(30, 30, 50, 50);
      }
    }
  </script>
 </head>
 <body onload="draw();">
   <canvas id="canvas" width="150" height="150"></canvas>
 </body>
</html>
```
## Drawing Shapes with Canvas
### The grid
- Before we can start drawing, we need to talk about the canvas grid or coordinate space. 
- Normally 1 unit in the grid correspons to 1 pixel on the canvas. The origin of this grid is positioned in the top left corner at coordinate (0,0). All elements are relative to this position.
### Drawing rectangles
```html
First let's look at the rectangle. There are three functions that draw rectangles on the canvas:

fillRect(x, y, width, height)
Draws a filled rectangle.

strokeRect(x, y, width, height)
Draws a rectangular outline.

clearRect(x, y, width, height)
Clears the specified rectangular area, making it fully transparent.

```
### Rectangular shape example
```html
function draw() {
  var canvas = document.getElementById('canvas');
  if (canvas.getContext) {
    var ctx = canvas.getContext('2d');

    ctx.fillRect(25, 25, 100, 100);
    ctx.clearRect(45, 45, 60, 60);
    ctx.strokeRect(50, 50, 50, 50);
  }
}
```

### Drawing Paths
- 1. First, you create the path
- 2. Then you use drawing commans to draw into the path
- 3. Once the path has been created, you can stroke or fill the path to render it.
- Here are the functions used to perform these steps:
  - beginPath(): Creates a new path. Once created, future drawing commands are directed into the path and used to build the path up.
  - Path methods: Methods to set different paths for objects.
  - closePath(): Adds a straight line to the path, going to the start of the current sub-path.
  - stroke(): Draws the shape by stroking its outline.
  - fill(): Draws a solid shape by filling the path's content area.

## Applying styles and colors
- Up until now we have only seen methods of the drawing context. If we want to apply colors to a shape, there are two important properties we can use: fillStyle and strokeStyle
- fillStyle = color
  - Sets the style used when filling shapes.
- strokeStyle = color
  - Sets the style for shapes' outlines.

- color is a string representing a CSS <color>, a gradient object, or a pattern object. We'll look at gradient and pattern objects - later. By default, the stroke and fill color are set to black (CSS color value #000000).

- The lineCap property determines how the end points of every line are drawn. There are three possible values for this property and those are: butt, round and square. By default this property is set to butt.

- butt: The ends of lines are squared off at the endpoints.
- round: The ends of lines are rounded.
- square: The ends of lines are squared off by adding a box with an equal width and half the height of the line's thickness.
## Drawing Text
- fillText(text, x, y [, maxWidth])
  - Fills a given text at the given (x,y) position. Optionally with a maximum width to draw.
- strokeText(text, x, y [, maxWidth])
  - Strokes a given text at the given (x,y) position. Optionally with a maximum width to draw.
### Styling Text
- font = value
  - The current text style being used when drawing text. This string uses the same syntax as the CSS font property. The default font is 10px sans-serif.
- textAlign = value
  - Text alignment setting. Possible values: start, end, left, right or center. The default value is start.
- textBaseline = value
  - Baseline alignment setting. Possible values: top, hanging, middle, alphabetic, ideographic, bottom. The default value is alphabetic.
-  direction = value
  - Directionality. Possible values: ltr, rtl, inherit. The default value is inherit.
### Advanced text measurements
- measureText()
  - Returns a TextMetrics object containing the width, in pixels, that the specified text will be when drawn in the current text style.
- The following code snippet shows how you can measure a text and get its width.
```javascript
function draw() {
  var ctx = document.getElementById('canvas').getContext('2d');
  var text = ctx.measureText('foo'); // TextMetrics object
  text.width; // 16;
}
```