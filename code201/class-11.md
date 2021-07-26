# CLASS 11 NOTES - Audio, Video, Images

## **From Jon Duckett's "HTML&CSS"**

- *Code examples referenced from the text*

- - -

## ***Chapter 16 - Images***

You can specify the dimensions of images using CSS

- Helpful when you use the same sized images on several pages of your site

```css
img.large {
  width: 500px;
  height: 500px;}
img.medium {
  width: 250px;
  height: 250px;}
img.small {
  width: 100px;
  height: 100px;}
```

Class sizes can be referred to as `small`, `medium`, or `large`

Images can be aligned both horizontally and vertically using CSS

```css
img.align-left {
  float: left;
  margin-right: 10px;}
img.align-right {
  float: right;
  margin-left: 10px;}
img.medium {
  width: 250px;
  height: 250px;}
```

```css
img.align-center {
  display: block;
  margin: 0px auto;}
img.medium {
  width: 250px;
  height: 250px;}
```

You can use a background image behind the box created by any element on a page

```css
body {
  background-image: url("images/pattern.gif");
}
```

Background images can appear just once or be repeated across the background of the box

- `repeat`, `repeat-x`, `repeat-y`, `no-repeat`, `fixed`, `scroll`
- `background-position` can also be used for alignment

This can all be done in Shorthand

You can create image rollover effects by moving the background position of an image

- a third can even be used when a user clicks

To reduce the number of images your browser has to load, you can create image sprites

A ***sprite*** is a single image used for several different parts of an interface

- Logo, interface elements, and buttons can be added to the interface
- Improves loading speed

Gradients can be added to background-images

Low contrast backgrounds should be used for text to be legible
- - -

## ***Chapter 19 - Practical Information***

Search engine optimization (SEO) helps visitors find your sites when using search engines

- On-Page techniques - methods you can use on your web pages to improve their rating in search engines
- Off-Page techniques - getting other sites to link to your site

Identify key words and phrases through brainstorming, organization, research, comparing, refining, and mapping

Analytics tools such as Google Analytics allow you to see how many people visit your site, how they find it, and what they do when they get there

- The overview page gives a snapshot of key info about visitors and how to use this info
  - Visits, unique visits, page views, pages per visit, average time on site
- Can tell us what our visitors are looking at, and where they are coming from
  - Referrers, direct URL, search terms

To put your site on the web, you will need to obtain a domain name and web hosting

- Hosting can be limited by disk space, bandwidth, and backups

FTP programs (File Transfer Protocol) allow you to transfer files from your local computer to your web server

- Many programs allow you to simply drag and drop files from your computer to the server
  - FileZilla, FireFTP, CuteFTP, SmartFTP, Transmit

Many companies provide platforms for blogging, email newsletters, e-commerce, and other popular website tools to save you writing them from scratch

- wordpress, tumblr, posterous, shopify, bigcartel, go.megento, campaignmonitor, mailchimp, addthis, addtoany

- - -

## ***Video and Audio APIs***

- *Code examples referenced from MDN Web Docs*

- - -

HTML5 has elements to embed rich media in documents
- `<video>` and `<audio>`
- These tags come with their own APIs for controlling playback

```html
<video controls>
  <source src="rabbit320.mp4" type="video/mp4">
  <source src="rabbit320.webm" type="video/webm">
  <p>Your browser doesn't support HTML5 video. Here is a <a href="rabbit320.mp4">link to the video</a> instead.</p>
</video>
```

Playback `controls` should be specified
- But they are different in each browser
- Instead, playback can be improved improved through HTML, CSS, and JavaScript

### HTMLMediaElement API

- Features allow you to control video and audio players programmatically

Wrapping in a `<div>` element, the entire player can be styled as one unit

```html
<div class="player">
  <video controls>
    <source src="video/sintel-short.mp4" type="video/mp4">
    <source src="video/sintel-short.webm" type="video/webm">
    <!-- fallback content here -->
  </video>
  <div class="controls">
    <button class="play" data-icon="P" aria-label="play pause toggle"></button>
    <button class="stop" data-icon="S" aria-label="stop"></button>
    <div class="timer">
      <div></div>
      <span aria-label="timer">00:00</span>
    </div>
    <button class="rwd" data-icon="B" aria-label="rewind"></button>
    <button class="fwd" data-icon="F" aria-label="fast forward"></button>
  </div>
</div>
```

Implementing JavaScript enables us to wire up all the buttons to get controls working properly

- Playing and Pausing
- Stopping
- Seeking back and forth
- Updating the elapsed time

- - -

## ***Chapter 9 - Flash, Video, & Audio***

### *- Flash is no longer supported by many browsers but is an important part of history.*

Up until recently, Flash was a popular tool since the late 1990s

- Used for creating animations, and playing audio and video in websites

In 2005-6, a set of JavaScript libraries were launched which made it easier for people to create animated effects with JS

- Prototype, script.aculo.us, and JQuery

Apple decided not to support flash when releasing the iPhone and iPad in 2007 and 2010

In 2008, browswers started to support HTML5 `<video>` and `<audio>`


[back](../README.md)
