# CLASS 12 NOTES - Chart.js, Canvas

## ***Easily Create Stunning Animated Charts with Chart.js***

- webdesignerdepot.com
- *Code examples referenced from the text*

- - -

Charts are better for displaying data visually than tables

- Easier to look at and convey data quickly

### Chart.js is a JavaScript plugin that usesHTML5's canvas element to draw a graph onto the page

To draw a line chart, one needs to create a canvas element in their HTML where Chart.js can draw

```html
<canvas id="buyers" width="600" height="400"></canvas>
```

A script is then written to retrieve context of the canvas

```js
var buyers = document.getElementById('buyers').getContext('2d');
    new Chart(buyers).Line(buyerData);
```

Options can be added to the chart in JavaScript, similar to CSS styling

Chart.js is simple to use and very flexible

The listed documentation shows the numerous options and possibilities

- - -

## ***Basic Usage of Canvas***

- MDN Web Docs

### The `<canvas>` Element

The `<canvas>` element has only two attributes, width and height

- Optional and can also be set using DOM properties
- 300px wide by 150px high is initial default
- `id` should be applied

The `<canvas>` element can be styled with CSS, but the drawing is not effected by this

A closing `</canvas>` tag is required

`<canvas>` uses a method called `getContext()` to obtain rendering context and drawing functions

```js
var canvas = document.getElementById('tutorial');
var ctx = canvas.getContext('2d');
```

The script includes a function called`draw()` which is executed once the page finishes loading by listening for a load event

- - -

## ***Drawing Shapes With Canvas***

### The Grid

1 unit corresponds to 1 pixel

Origin of the grid is positioned in top left corner at (0,0) (x,y)

Example of rectangles using a fill, transparent, or outline

```js
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

### A path is a list of points connected by segments of lines

- can be different shapes, curved or not, of different widths and colors

Example of a filled triangle using a path

```js
ctx.beginPath();
    ctx.moveTo(75, 50);
    ctx.lineTo(100, 75);
    ctx.lineTo(100, 25);
    ctx.fill();
```

Other methods and drawing commands can be used to draw such as pen, lines, arcs, bezier and quadratic curves

`Path2D` object lets you cache or record drawing commands

- simplifies code and improves performance

SVG path data can be used to initialize paths on your canvas

- allows you to pass around and re-use path data in SVG and canvas

- - -

## ***Applying Styles and Colors***

`fillStyle = color` - sets the style used when filling shapes

`strokeStyle = color` - sets the style for shapes' outlines

CSS color values should be used

```js
// these all set the fillStyle to 'orange'

ctx.fillStyle = 'orange';
ctx.fillStyle = '#FFA500';
ctx.fillStyle = 'rgb(255, 165, 0)';
ctx.fillStyle = 'rgba(255, 165, 0, 1)';
```

We can also draw semi-transparent or translucent shapes using `globalAlpha`

- or by assigning opacity values to fill or stroke styles

### A number of line styles can be used

- This may require a lot of precision
  - `lineWidth = value`
  - `lineCap = type`
  - `lineJoin = type`
  - `miterLimit = value`
  - `getLineDash`
  - `setLineDash(segments)`
  - `lineDashOffset = value`

Example of `lineWidth`

```js
function draw() {
  var ctx = document.getElementById('canvas').getContext('2d');
  for (var i = 0; i < 10; i++) {
    ctx.lineWidth = 1 + i;
    ctx.beginPath();
    ctx.moveTo(5 + i * 14, 5);
    ctx.lineTo(5 + i * 14, 140);
    ctx.stroke();
  }
}
```

### Gradients

Linear, radial, and conic gradients can be applied to fill and stroke

- A `CanvasGradient` object is create

```js
var lineargradient = ctx.createLinearGradient(0, 0, 150, 150);
var radialgradient = ctx.createRadialGradient(75, 75, 0, 75, 75, 100);
```

### Patterns

`createPattern` method creates and returns a new canvas pattern object

### Shadows

Using shadows invloves 4 properties

- `shadowOffsetX = float`
- `shadowOffsetY = float`
- `shadowBlur = float`
- `shadowColor = color`

- - -

## ***Drawing Text***

There are 2 methods to render text using canvas, Fill and Stroke.

- `fillText(text, x, y [, maxWidth])`
- `strokeText(text, x, y [, maxWidth])`

Text can be styled, similar to how we would in CSS

- `font = value`
- `textAlign = value`
- `textBaseline = value`
- `direction = value`

[back](../README.md)
