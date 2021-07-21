# CLASS 08 NOTES - CSS Layout

## **From Jon Duckett's "HTML&CSS"**

- *Code examples referenced from the text*

- - -

## ***Chapter 15 - Layout (Continued)***

### How to control where each element sits on a page, making attractive page layouts

## Positioning Elements

CSS treats each HTML element as if it is in its own box.

- Either a block-level box or an inline box
  - Block-level - start on new line, act as main building blocks
  - Inline - flow between surrounding text
- Boxes can be separated with borders, margins, padding, and background colors

Outer Box is **containing** or **parent** element of element inside it

`<div>` often used as containing elements to group together sections of a page

Browsers display pages in *normal flow* unless you specify relative, absolute, or fixed positioning

- Relative - shifts element to top, right, bottom, or left of where it *would have* been placed
- Absolute - does not affect surrounding elements.
  - Moves as users scroll up and down the page.
- Fixed - type of absolute, does not move when scrolling

`float` property moves content to left or right of page

```css
p {
  width: 230px;
  float: left;
}
```

Float can be used to create multi-column layouts

- placing elements side by side
- items require defined width

```css
.column1of2 {
  float: left;
  width: 620px;
  margin: 10px;
}
.column2of2 {
  float: left;
  width: 300px;
  margin: 10px;
}
```

`z-index` controls order of overlapping boxes (which is on top)

```css
h1 {
  position: fixed;
  z-index: 10;
}
```

The clear property allows you to say that no element (within the same containing element) should touch the left or right-hand sides of a box.

- `left`, `right`, `both`, `none`

```css
.clear {
  clear: left;
}
```

Pages are kept within 960-1000 pixels wide

- indicate what the site is about within top 600 pixels
  - this demonstrates the page's relevance without scrolling
  - accounts for different screen sizes and resolutions

## Fixed width layout designs

- Do not change size as browser window increases or descreases
- Measurements tend to be given in pixels.

Pros

- Accurate at controlling size and positioniong of elements
- More control over appearance and position of items
- Length of lines of text can be controlled regardless of window size
- Image size will always remain the same

Cons

- There can be large gaps around edge of page
- Page can look much smaller on higer resolution screens
- Text may not fit if user increases font size
- Takes up more vertical space

## Liquid layout designs

- Stretch and contract depending on browser window size
- Tend to use percentages.

Pros

- Pages expand to fill entire browser window, no space on large screens
- Page can contract to fit on small window without the need to scroll
- Design is tolerant of users changing font size

Cons

- Design can look different than intended, with unexpected gaps if section widths are not controlled
- Lines of text can become long on large windows, hard to read
- Or the other way around on narrow windows
- Image can overflow over text within boxes that are too small

## Grids

Grids help create professional and flexible designs

- They set consistent proportions and spaces between items
- Many different layouts are possible using one versatile grid

Grids create continuity between pages

- Help users predict where to find info
- Easier to add new content in a consistent way
- Collaboration also becomes more consistent

### CSS Frameworks provide rules for common tasks

They save you from repeatedly write code for same tasks
- Tested across different browser versions

Often require the use of class names in HTML

- Often contain more code than you need, ie. *bloat*

You can include multiple CSS files in one page

- In CSS:

```css
@import url("tables.css");
@import url("typography.css");
```

OR in HTML:

```html
<head>
<title>Multiple Style Sheets - Link</title> <link rel="stylesheet" type="text/css"
      href="css/site.css" />
    <link rel="stylesheet" type="text/css"
      href="css/tables.css" />
    <link rel="stylesheet" type="text/css"
        href="css/typography.css" />
  </head>
```

[back](../README.md)