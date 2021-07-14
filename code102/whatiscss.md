# CSS: Cascading Style Sheets

- A language used for specifying how documents are visually presented, styled, and laid out
- HTML resorts to a browser’s default styles using an internal stylesheet
- Can be used for text styling - color or size of headings, links, etc.
- Layout and animation

## Syntax - rule based language

- You define rules specifying groups of styles applied to elements or groups of elements
- Style sheet rules are written one after the other.
- The language is broken down into *modules*

```
h1 {
  color: red;
  font-size: 5em;
}
```

- This example would make main heading large red text.

- ***selector*** which selects the HTML element to style, in this case `<h1>`.
- ***declarations*** - Inside curly braces { } - specify `property:` and `value;`

- Colors can either be a keyword or hexadecimal value (#RRGGBB) 0-f

CSS is developed by a group within the W3C called CSS Working Group. Resources for published specifications include W3C, WHATWG, ECMA, Khronos

- The language is constantly developing
- Only useful in developing web pages if one or more browsers have implemented it.
- Browser support status can be found under “browser compatibility” (check for use)

## ***Box model:***

- Margin >> Border >> Padding >> Content
(Top right bottom left)

## CSS can be inserted:

- internally (in the head section)
- externally (in head, link href separate file, or stylesheet)
- or inline (unique style for single element)
- Inline takes highest priority, then external and internal, followed by browser default

In the case of multiple style sheets, if some properties have been defined for the same selector (element) in different style sheets, value from last read style sheet will be used. 

## CSS Color usage examples:

- `color: red`
- `color: #00ff00` - hex value RRGGBB
- `color: rgb(0,0,255)` - red green blue
- `color: rgba(201, 76, 76, 0.6)` - last value is alpha/transparency (or opacity)
- `color: hsl(89, 43%, 51%)` - hue, saturation, lightness
- `color: hsla(89, 43%, 51%, 0.6)` - hue, saturation, lightness, alpha/transparency (or opacity)`

Many CSS properties are animatable

Syntax Property Values:

- Initial sets property to default value
- Inherit inherits property from parent element

[back](../README.md)
