# CLASS 01 NOTES - Introductory HTML and JavaScript

## **Reading Notes from Jon Duckett's "HTML&CSS - design and build websites"**

- *Code examples referenced from the text*

- - -

## ***Introduction***

### **How People Access the Web**

- Through the use of *browsers* (e.g.: Chrome, Safari, Firefox, Brave, etc.)
- When you type in a webpage, the browser sends a request to a *web server*, or host
  - Web servers - special computers constantly connected to the Internet
    - Optimized to send web pages out to people who request them
  - There are *web hosting* companies that typically charge a fee to host sites
- *Screen readers* - programs that read out contents of a screen, commonly for those with visual impairments

### **How Websites Are Created**

- All websites use HTML and CSS, the browser interprets this code to create the page that you see
  - HTML5 and CSS3 are the latest versions of these languages
  - JavaScript is a more advanced programming language that can also be used for user interactivity
- Larger websites that are updated regularly may use more complex technologies on the web server
  - CMS (content management systems), blogging tools, e-commerce software
  - Databases and additional programming languages (`PHP, ASP.Net, Java, Ruby`, etc.)

### **How the Web Works**

- An *Internet Service Provider* (ISP) connects you to the web
- To find the location of a website hosted by a web server, the browser will first connect to a *Domain Name System* (DNS)
- The DNS server (could be anywhere in the world) tells your computer the IP address associated with the requested domain name
- This information then tells your browser how to find the website, sending you the page you requested.

- - -

## ***Chapter 1 - Structure***

HTML pages are text documents - they describe the structure of pages

- Headings and subheadings show a hierarchy of information
- Sections and paragraphs will typically follow

HTML uses tags (or angled brackets) - often referred to as elements

Tags usually come in pairs, opening and closing, acting like containers

- Opening tags can carry attributes `<>`
  - Tell us more info on the content (inside the tags) of the element
  - Attributes require a name and a value
- Closing tags have a forward slash `</>`

Simple example of page structure:

```html
<html> 
    <body>
        <h1>Main Heading</h1>
        <p>A paragraph of text<p>

        <h2>Sub-Heading</h2>
        <p>Another paragraph.</p>

        <h2>Another Sub-Heading</h2>
        <p>And another paragraph.</p>
    </body>
</html>
```

Simple example of an attribute:

```html
<p lang="en-us">Paragraph in English</p>
```

`lang` is the attribute **name**
`en-us` is the attribute **value**

### **Body, Head, & Title**

- `<body>` - everything inside the body is shown inside the main browser window
- `<head>` - comes before body, contains info about the page, will not appear in browser
- `<title>` - placed inside head, displayed in the tab (or at top of browser)

### **HTML stands for HyperText Markup Language**

- HyperText - you can create links to allow users to move from one page to another quickly and easily
- Markup - you can annotate text (tags), which provides additional meaning to the documents’ contents

Web pages can be created easily with minimal tools

- Text editor such as NotePad or TextEdit
- Code Management system such as WordPress
- Additional tools and more complex code editors enable developers to work more efficiently

Source code for other websites can be easily accessed by right clicking on a page and selecting ‘View Source’

- This is a good way to further understand how code works

- - -

## ***Chapter 8 - Extra Markup***

`DOCTYPES` tell browsers which version of HTML you are using

- HTML5 is most recent, released in 2000
  - `<!DOCTYPE html>` must be declared at the beginning of every page

You can add comments to your code - `<!-- . . . -->`

- Content between markers is not visible in browser, only visible to those viewing the code
- Good practice to communicate what’s what within the code
- Blocks of code can also be commented out to stop them from being displayed

The `id` and `class` attributes allow you to identify particular elements

- This becomes important when we begin to incorporate CSS and JavaScript
- Id ex: `<p id=“pullquote”>`Body of text.`</p>`
  - This particular paragraph could have a unique style different from others on the page
- Class attributes can be used to identify several elements that you want to change as opposed to just one
  - Class ex: `<p class=“important”>`Body of text`</p>`
    - Can be applied to multiple elements

Block elements always start on a new line in the browser window (ex: `<h1>, <p>, <ul>, <li>`)
Inline elements continue on the same line as neighboring elements (ex: `<a>, <b>, <em>, <img>`)

- `<div>` and `<span>` elements allow you to group block-level and inline elements together
  - `<span>` inside `<div>`, never vice-versa
  - `<span>` is often used with a `class` or `id` attribute to apply CSS styles

```html
<p>Anish Kapoor won the Turner Prize in 1991 and exhibited at the <span class="gallery">Tate Modern</span> gallery in London in 2003.</p>
```

`<iframes>` (or inline frames) cut windows into your web pages, displaying other pages

- `src` attribute specifies URL

```html
<iframe
  src="http://maps.google.co.uk/maps?q=moma+new+york
  &amp;output=embed"
  width="450"
  height="350"
  frameborder="0"
  scrolling="no">
</iframe>
```

`<meta>` tag is used to supply all kinds of info about a web page

- Description - used by search engines, 155 character max
- Keywords - list of words seperated by commas that a user may search
- Robots - determines whether or not the page should be added to a search engine
- Author - defines author of the web page
- Pragma - prevents browser from caching page (storing locally to save time downloading it in the future)
- Expires - when a page should no longer be cached, date format is specific

```html
<!DOCTYPE html>
<html>
<head>
<title>Information About Your Pages</title> <meta name="description"
      content="An Essay on Installation Art" />
    <meta name="keywords"
      content="installation, art, opinion" />
    <meta name="robots"
      content="nofollow" />
    <meta http-equiv="author"
      content="Jon Duckett" />
    <meta http-equiv="pragma"
      content="no-cache" />
    <meta http-equiv="expires"
      content="Fri, 04 Apr 2014 23:59:59 GMT" />
  </head>
<body>
  </body>
</html>
```

Escape characters (aka escape codes or entity references) are used to include special characters - `&...;`

- Not all fonts support these characters
- Visit [http://www.htmlandcssbook.com/extras/html-escape-codes/](http://www.htmlandcssbook.com/extras/html-escape-codes/) for complete list

- - -

## ***Chapter 17 - HTML5 Layout***

The new HTML5 elements indicate the purpose of different parts of a web page and help to describe its structure

- They provide clearer code (compared with using multiple `<div>` elements).
  - `<header>, <footer>` - can be used as top/bottom of every page, as well as individually inside of `<article>` or `<section>` within a page
    - Ex: each post on a blog can be thought of as a separate section, `<header>` could have title and date, `<footer>` may contain links
  - `<nav>` is primary site navigational blocks, oftentimes placed inside page `<header>`
  - `<article>` - container for any standalone section / independent piece of content - can be nested inside each other
  - `<aside>` - often appears as a side bar. When inside an `<article>`, should contain related yet not essential info. When outside an `<article>`, acts as container related to entire page (e.g.: links to other sections, recent posts or tweets by the author, or a search box)
  - `<section>` - groups related content/items together, with own heading
    - May contain several `<article>` elements
    - Not to be used as a wrapper for entire page, use `<div>` or `<main>` instead
  - `<hgroup>` - heading group

```html
<hgroup>
<h2>Title</h2>
<h3>Sub-Title</h3>
</hgroup>
```

- `<figure>` - content referenced from main flow of an article (images, videos, graphs, diagrams, code samples, block quotes)
  - `<figcaption>` - text description of `<figure>` element

Older browsers that do not understand HTML5 elements need to be told which elements are block-level elements

- Include this line of CSS:

```css
header, section, footer, aside, nav, article, figure
{
  display: block;}
```

- `<div>` are sectioning (or grouping) elements, used when no other suitable element is available (such as a “wrapper” for the entire page)
  - Anything that lies outside of `<header>`, `<footer>`, or `<aside>` can be considered main content
- You can link around entire block level elements with `<a>` tag

To make HTML5 elements work in IE8 or older, extra JavaScript (*conditional comment* known as HTML5 shiv or shim) is needed (available from Google, example below…)

```html
<!--[if lt IE 9]>
  <script src="http://html5shiv.googlecode.com/svn/
    trunk/html5.js"></script>
<![endif]-->
```

- - -

## ***Chapter 18 - Process & Design***

Understand your **target audience** (WHO), **why** they would come to your site, **what** information they are looking for, and **when** they are likely to return

- Who:
  - Demographic of Individuals - age range, gender, country, urban vs rural, income, education, marital/family status, occupation, time spent at work, time spent on the web, device type for web access
  - Companies - size of company or department, employee positions, personal use or for someone else, size of budget
- Why:
  - Motivations - general entertainment or specific goal, personal or professional, essential or luxury
  - Specific Goals - general or specific info, already familiar with service/product or need introduction, time sensitive info, discover info to make decisions, need to contact
- What (Key Information):
  - Introduction of subject/brand, background info on product/service, important features, what makes your offering special and different? Common questions
- When (How Often will they visit):
  - Some sites/pages need updating more frequently
  - Set a schedule for updating
  - Goods and Services
    - How often do people return to purchase?
    - How often is stock updated or service changed?
  - Information - What percentage of visitors return for regular updates, how often is subject updated

## Site Maps

- Allow you to plan the structure of your site with a diagram of pages to be used and grouped
- **Card sorting** - placing pieces of info that a visitor may need on separate pieces of paper and organizing them into groups
- Pages (or groups of pages) inform how users navigate through a site
- Site should reflect the public’s understanding of the subject, not the owner’s

## Wireframes

- Allow you to organize info that will go on each page
- A simple sketch of key info, shows hierarchy of info and how much space it may require
- Do not include styling yet, prioritize where info will go
- Can be sketched on paper or using graphics applications such as Illustrator, InDesign, Photoshop, etc. (many online tools available as well)

## **DESIGN = COMMUNICATION**

- **Visual Hierarchy** - the order in which your eyes perceive what they see
  - Helps visitors understand what you’re trying to tell them
    - It must address their needs
  - The effect, if well-designed, is largely subliminal. It requires *balance*.
  - Created by adding *visual contrast* between items being displayed
  - Images often attract the eye first (a picture is worth 1,000 words)

  - Organize and prioritize content to help users understand importance and order
  - Size, Color, And Style can differentiate between pieces of info
    - Headings and key points should be relatively large
    - Brighter sections draw attention first
    - Bold, italic, or all-caps helps content stand out

**Grouping and similarity** (blocks or chunks) helps to simplify the info you present (this is all about targeting perception)

- We tend to organize visual elements into groups when making sense of a design
  - Proximity, closure, continuance, white space, color, borders
    - All help us differentiate, categorize, and prioritize content

“Things that are similar are perceived to be more related than things that are dissimilar.”

- Repetition suggests matching elements have similar importance or meaning. (Consistency!)
- Headings determine relevance for the user

### **Designing Navigation**

- Helps users understand what your site is about and how it is organized. Good navigation should be:
  - Concise, clear, selective, contextual, interactive, consistent (less is more!)

- - -

## **Reading notes from Jon Duckett's "JavaScript&JQuery - interactive front-end web development"**

- *Code examples referenced from the text*

- - -

## ***Introduction***

JavaScript makes web pages more interactive, can respond to what the user does

- Access content by selecting any element, attribute, or text from an HTML page
  - ex: Select elements that have a specific `class` attribute
- Modify content by adding or removing elements, attributes, or text
  - ex: Change the size or position of an `<img>` element
- Program rules - specify a set of steps for the browser to follow, allowing it to access or change content of a page
  - ex: check which image was clicked and display a larger version of it
- React to events - tell a script to run when a specific event has occurred
  - ex: a button/link is pressed/clicked/tapped, a cursor hovers over an element, an interval of time has passed

More examples of JavaScript in the browser

- Image slideshows, forms (validations and calculations), reloading only part of a page, filtering data (using keywords)

- - -

## ***Chapter 1 - The ABC of Programming***

### **1/a - What is a Script and How do I Create One?**

A script is a series of instructions that the computer can follow step-by step in order to achieve a goal

- Example comparisons: recipes, handbooks, manuals (from more simple to more complex)

Each time the script runs, it might only use a subset of all the instructions

Computers approach tasks differently than humans - they are very logical and obedient

- Your instructions must let the computer solve the test *programmatically* (follow series of instructions one after another)
- Vocabulary - The words that computers understand
- Syntax - How you put those words together to create instructions computers can follow

To approach writing a script, break down your goal into a series of tasks

- Then work out each step needed to complete that task (use a flowchart)
  1. Define the goal - a puzzle for the computer to solve
  2. Design the script - series of tasks w/ flowchart, numbered steps and information needed to complete tasks
  3. Code each step
- Flowcharts consist of generic steps, events, input or output, and decisions

- - -

### **1/b - How Do Computers Fit in With the World Around Them?**

Computers create models of the world using **data**

- **Data** is all the computer needs to follow the instructions you give it to carry out its tasks

The models use objects to represent physical things. Objects can have:

- *Properties* - characteristics that tell us about the object
  - Has a name and value, similar to HTML and CSS with attributes and values
    - Ex: object: car, property name: make, property value: BMW
- *Events* - triggered when a user interacts with the computer
  - Scripts often use different events to trigger different types of functionality
    - Ex: `accelerate` and `brake` events would increase or decrease `currentSpeed` property of a car
- *Methods* - perform tasks using the properties of the object, how people or things interact with an object
  - The code can contain a lot of instructions that represent one task
    - Ex: `changeSpeed()` would increase or decrease `currentSpeed` property

***Events trigger (or call) methods, methods can retrieve or update an object’s properties***

  1. Driver speeds up, `accelerate` event fires.
  2. `accelerate` event calls the `changeSpeed()` method, which then increases value of `currentSpeed` property.
  3. Value of `currentSpeed` property reflects how fast car is traveling.

Code is written by programmers to say, “When this event occurs, run that code.”

The *Document Object* (or window) supported by the browser represents an HTML page

- It has Properties, Methods, and Events
- Web browsers use HTML markup to create a model of a web page
- Each element creates its own node (or a kind of object)

1. The browser receives a page as HTML code
2. It creates a model of the page and stores it in memory (nodes that could represent elements, text, and attributes)
3. It shows the page on the screen using a rendering engine

To make web pages interactive, you write code that uses the browser’s model of the web page

When JavaScript is used in the browser, an *interpreter* (or scripting engine) translates instructions so the browser can achieve the tasks it is being asked to perform

- Each line of code is translated one-by-one as the script is run.

- - -

### **1/c - How Do I Write a Script For a Web Page?**

Separation of Concerns

- ***HTML*** - Content layer - structure and semantics
- ***CSS*** - Presentation layer - enhances HTML with rules that state how content is being styled
- ***JavaScript*** - Behavior layer - adding interactivity

Whenever possible, JavaScript code should be kept in it’s own separate `.js` files

- The same rule should also apply to CSS - also lends itself to faster loading, easier maintenance
- Page will still work if JavaScript cannot be loaded

The `<script>` element is used in HTML pages to tell the browser to load the JavaScript file
Example of linking `.css` and `.js` files in an HTML file

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Title Goes Here</ title>
        <link rel ="stylesheet" href="css/ cOl.css" /> <!-- CSS File -->
    </head>
    <body>
        <h1>Heading Example</h1>
        <script src="js/ add-content.js"></ script> <!-- JavaScript File -->
        <p>Body of Text</ p>
    </body>
</html>
```

If you view the source code of a page in a browser, the JavaScript will not have changed the HTML

- Script works with model of the web page that the browser has created

Script can also be run or “called” in an HTML document, such as:

```html
<script>document.write('Welcome !'); </script>
```

`'document'` is the *object*,
`'.'` is the *member operator*,
`'write('Welcome !’)'` is the *method*,
`'’Welcome !’'` is the *parameter*

JavaScript runs where it is found in the HTML.

[back](README.md)
