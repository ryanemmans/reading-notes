# CLASS 14 NOTES - CSS Transforms, Transitions, and Animations

- *Code examples referenced from the text*

## ***Transforms***

- https://learn.shayhowe.com/advanced-html-css/css-transforms/

- - -

In CSS3, the `transform` property makes it possible to size, position, and change elements

- 2 different settings, two-dimensional and three-dimensional

`transform` can include multiple vendor prefixes for best support across all browsers

```css
div {
  -webkit-transform: scale(1.5);
     -moz-transform: scale(1.5);
       -o-transform: scale(1.5);
          transform: scale(1.5);
}
```

## 2D Transforms

- Work on the X and Y axes (horizontal/vertical)

2D Rotate - 0 to 360 degrees

2D Scale - `transform: scale(.5, 1.15);`

2D Translate - similar to relative positioning

- `transform: translate(-10px, 25%);`

2D Skew - distorts elements on each axis

- `transform: skew(5deg, -20deg);`

Transforms can be combined on a single line

- `transform: skew(10deg, 20deg) translateX(20px);`

`transform origin` - Exact center of an element, 50% horizontally and vertically

```css
.box-1 {
  transform: rotate(15deg);
  transform-origin: 0 0;
}
.box-2 {
  transform: scale(.5);
  transform-origin: 100% 100%;
}
.box-3 {
  transform: skewX(20deg);
  transform-origin: top left;
}
.box-4 {
  transform: scale(.75) translate(-10px, -10px);
  transform-origin: 20px 50px;
}
```

`perspective` - can be thought of as a vanishing point, gives elements depth in 2D

- `transform: perspective(200px) rotateX(45deg);`
- `origin` can also be applied

## 3D Transforms

- Come with an additional Z axis, giving us depth
- Perspective value is used

3D Rotate

3D Scale

3D Translate

3D Skew - *cannot* be skewed on Z axis

Shorthand 3D Transforms

- `rotate3d`, `scale3d`, `transition3d`, `matrix3d`

## Transform Style

Allows nested elements to transform in their own 3-dimensional plane

`preserve-3d` - allows transformed children elements to appear in their own 3D plane

`flat` - forces transformed children elements to lie flat on the 2D plane

Backface Visibility - `hidden` or `visible`

- - -

## ***Transitions & Animations***

- https://learn.shayhowe.com/advanced-html-css/transitions-animations/

- - -

Transitions - you can alter appearance and behavior of an element whenever a state change occurs

- When it is hovered over, focused on, active, or targeted.
- Change from one state to another

Animations - allow appearance and behavior of an element to be altered in multiple keyframes

- Set multiple points of transitionupon different keyframes

## Transitions

4 properties

- `transition-property` - which property will be altered
- `transition-duration` - uses general time values, seconds (`s`) and milliseconds (`ms`)
  - can also come in decimal measurements
- `transition-timing-function` - speed in which transition will move
  - ex: `linear`, `ease-in`, `ease-out`, and `ease-in-out`
  - Each timing function has a cubic-bezier curve behind it, which can be additionally set
    - `cubic-bezier(x1, y1, x2, y2)`
  - multiple timing functions can be used in a single line
- `transition-delay` - time value that determines a stall before executing

```css
.box {
  background: #2db34a;
  transition-property: background;
  transition-duration: 1s;
  transition-timing-function: linear;
}
```

## Animations

Animations use transitions in multiple states

The `@keyframes` rule includes animation name, breakpoints, and properties intended to be animated

```css
@keyframes slide {
  0% {
    left: 0;
    top: 0;
  }
  50% {
    left: 244px;
    top: 100px;
  }
  100% {
    left: 488px;
    top: 0;
  }
}
```

Animation uses name, `duration`, `timing-function` (easing for example) and `delay`

- Additionally, `iteration-count`, `direction`, `play-state`, and `fill-mode`

```css
.stage:hover .ball {
  animation-name: slide;
  animation-duration: 2s;
  animation-timing-function: ease-in-out;
  animation-delay: .5s;
  animation-iteration-count: infinite;
}
```

All can be written in shorthand

- - -

## ***8 SIMPLE CSS3 TRANSITIONS THAT WILL WOW YOUR USERS***

- https://www.webdesignerdepot.com/2014/05/8-simple-css3-transitions-that-will-wow-your-users

- - -

### Fade In

```css
.fade {
  opacity:0.5;
}
.fade:hover {
  opacity:1;
}
```

### Change Color

```css
.color:hover {
  background:#53a7ea;
}
```

### Grow & Shrink

```css
.grow:hover {
  -webkit-transform: scale(1.3); /* or (0.8) */
  -ms-transform: scale(1.3); /* or (0.8) */
  transform: scale(1.3); /* or (0.8) */
}
```

### Rotate Elements

```css
.rotate:hover {
  -webkit-transform: rotateZ(-30deg);
  -ms-transform: rotateZ(-30deg);
  transform: rotateZ(-30deg);
}
```

### Square to Circle

```css
.circle:hover {
  border-radius:50%;
}
```

### 3D Shadow

```css
.threed:hover {
  box-shadow:
    1px 1px #53a7ea,
    2px 2px #53a7ea,
    3px 3px #53a7ea;
  -webkit-transform: translateX(-3px);
  transform: translateX(-3px);
}
```

### Swing

- Instead of transition, this would use `@keyframes`, `animation` and `animation-iteration`

### Inset Border

```css
.border:hover {
  box-shadow: inset 0 0 0 25px #53a7ea;
}
```

[back](../README.md)
