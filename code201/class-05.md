# CLASS 05 NOTES - Images, Color, Text

## **From Jon Duckett's "HTML&CSS"**

- *Code examples referenced from the text*

- - -

## ***Chapter 5 - Images***

### Images can consist of logos, photos, illustrations, diagrams, or charts

They should be relevant, convey info and the right mood, be instantly recognizable, and fit the color pallette

It is good practice to create a folder for all images used

The `<img>` element is used to add images to a web page

You must always specify a `src` source attribute - indicates source of an image

- `alt` attribute describes content of an image
- `title` provides addition info
- `height` and `width` specify size

Place images before a paragraph, inside the beginning of a paragraph, or in the middle of a paragraph

- block elements always appear on a new line
- inline elements sit within block elements and stay on same line

`align` - used in older versions of code - left, right, top, middle, bottom

- CSS is now used instead

Save images at the size you will be using them on the page and in appropriate format

- Adobe Photoshop is most common tool

Do not crop out valuable information

- images can be better suited for portrait or landscape

Photographs are best saved as JPEGs

Use GIF or PNG format when saving images with few colors or flat color - large areas of the same color.

Images with transparency will use GIF or PNG

Correct Resolution should also be used - 72 ppi

Vector images differ from bitmap images

- Are resolution-independent, commonly created in programs such as Adobe Illustrator.

Animated GIFS contain several frames to create an animation

`<figure>` and `<figcaption>` are new elements used to associate captions to images

- - -

## ***Chapter 11 - Color***

### Color brings your site to life

- It helps to convey the mood
- Evokes reactions

Foreground `color` is for text, as opposed to `background-color`

Three ways to specify colors in CSS

- RGB values (red, green, blue - `rgb(102,205,170)`)
- Hex codes - `#66cdaa`
- Color names - `MediumAquaMarine`

Color pickers can help you find the color you want

There should be enough contrast between text and background color for readability

CSS3 has an extra value (RGBA) to indicate opacity

CSS3 also allows you to specify colors as HSL values

- Hue - angle/degree on a color wheel (0-360)
- Saturation (0%-100%)
- Lightness aka luminosity (0%- black, 100% - wh
ite, 50% is normal)
- HSLA gives optional opacity value

- - -

## ***Chapter 12 - Text***

There are properties to control the choice of font, size, weight, style, and spacing

Typefaces

- Serif (extra details)
- Sans-Serif (cleaner design)
- Monospace (ex: Courier, Courier New)
- Cursive (ex: COMIC SANS!)
- Fantasy (ex: Impact)

Weight - can add emphasis and contrast

- light, medium, bold, black

Style - Normal, Italic, Oblique (angle)

Stretch (letter width) 

- Condensed (narrow), Regular, Extended (thicker and further apart)

Limited Choice of fonts that one can assume most people will have installed

- `font-family`
- `font-face`
- service based font-face

- You need to have the right license to use them

### Specifying typefaces

- `font-size` - pixels, percentages, or ems
  - defualt for browsers is 16px
  - SEE PAGE 276 for a detailed table

For a wider range of typefaces there are several options

- `@font-face` - can be used if not installed
- `font-family` - specifies name
- `src` - specifies path, a few versions may be needed
- `format` - eot, woff, ttf / otf, svg
  - SEE PAGE 278 for browser compatibility table

`text-transform` - `uppercase;`, `lowercase;`, `capitalize;`

`text-decoration` - none, underline, overline, line-through, blink (causes text to flash on/off)

You can control the space between lines of text, individual letters, and words

- Text can be aligned ro the left, right, center, or justified, as well as indented
- `line-height` - use `em` for spacing relativity as opposed to `px`
- `letter-spacing`, `word-spacing` - kerning -space between letters

Pseudo classes can be used to change style of an element when a user hovers over or clicks on text

- also applies to visited links
- `:link :visited :hover :active :focus`

SEE PAGE 292 for Atribute Selector Table

###### (I'm going to use comic sans and blink on every single page that I make)

- - -

## ***JPEG vs PNG vs GIF***

### ***Which image format to use and when?***

- Use JPEG format where variation in colour and intensity is smooth
- Use PNG format for any image that needs transparency 
  - or for images with text & objects with sharp contrast edges like logos
- Use GIF for images that contain animations

### Compression

Reduces size of data to ensure faster transmission

- lossless and lossy (irreversible)
  - quality reduction in lossy known as compression artefact

JPEG is lossy

- compression ratios of 1:10
- best for photos, bad for text, lines, sharp contrast

PNG is lossless

- retains higher quality and sharpness
- good for hi res , images with text, logos, sharp edges
- 5-25% better compression that GIFS

GIF are lossless

- mainly only used for animations now

### Transparency

- JPEG - no
- PNG - yes, use PNG
- GIF - yes, but poor edge details

### Colours

- JPEG - 16 million colours
- PNG
  - PNG8 - 256 colours - use for simple shapes, fewer colors
  - PNG24 - 16 million colours - use for high quality
- GIF - 256 colors

### Animation

Only supported by GIF







































[back](../README.md)
