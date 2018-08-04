# HTML & CSS Workshop

## The Web in 3 parts

The code that runs in modern web browsers is primarily built from three components: 1. HTML Markup, 2. CSS Stylesheets, and 3. scripts written in JavaScript. Each of these components has a distinct responsibility. HTML is in charge of storing the content that actually makes up the web page. Any images, text, videos, lists, links or whatever else you might see on a website is built using HTML. 

However, without CSS, the web would be much uglier. Modern CSS takes the responsibility of styling our content so that it contributes to a better user experience on a site. With the prominence of mobile devices on the web, CSS has also been instrumental in making sure that we can build websites that look just as good on a phone as they do in a web browser. 

Finally, JavaScript allows us to build more complex functionality. We can define functions that will run when particular events happen, say clicking a link/button or scrolling to a certain part of a page. JavaScript allows us to add a more dynamic and interactive feel to our site. We can use JavaScript to create lists that will update as we type into a search field. We can use it to trigger requests to our server to load more recent emails into our inbox and other such awesomeness.

## Our Focus Today

Today, we're going to focus mainly on HTML & CSS and a little bit of JavaScript to build our first website. We're going to build out a single page site that has navigation menu fixed to the top of the screen. From that menu, we'll be able to navigate to one of four sections:

- Home
  - a short intro and tagline
- About
  - a photo of us and a bit more detail
- Photos
  - a few photos to show some personality
- Contact 
  - a contact form to allow people to contact us.

Check out an example of the [finished product](https://moderncarpalbooleanvalue--five-nine.repl.co/) on repl.it.

## What You'll Be Able to Do

- Identify HTML tags and put them together to build a website.
- Understand the Box Model that governs how elements take up space within a web page.
- Read documentation and use what you read to experiment and improve your site with what you learn.
- Build columns with HTML & CSS that will collapse into rows on mobile devices
- Change background colors and font colors on a web page.
- Add images to your site by using publically available URLs or by posting images on [postimages.org](https://postimages.org/)
- Use the [repl.it](http://repl.it/languages/html) editor to build and publish your project to the web

## Getting Started

First, you'll want to open the [repl.it editor](http://repl.it/languages/html). Feel free to create an account here so you can keep track of your future projects more easily. Repl.it is an online platform that makes it really easy to get set up with a coding environment where you can apply concepts that you're learning and deploy your pages live to share with friends.CodePen is a social development environment for front-end designers and developers. It's an awesome place to build and deploy your website, show off your work, and find inspiration. Setting up a free acccount will allow you to create a single project like the one we'll build today. After we've opened up codepen.io and started a new project, we can get started. I'll walk through the project creation process with you here.
First, you'll want to open the [repl.it editor](http://repl.it/languages/html). Feel free to create an account here so you can keep track of your future projects more easily. Repl.it is an online platform that makes it really easy to get set up with a coding environment where you can apply concepts that you're learning and deploy your pages live to share with friends. After we've opened up repl.it and started a new project, we can get started. The first time we hit the save button, our project will get a URL that we can share with others. Though it's not required, creating an account makes it easy to keep track of these later on.

## Learning about HTML 

We put an HTML page together by assembling a bunch of elements called tags. Tags look like this `<html>` (an opening html tag) and this `</html>` (a closing html tag). Everything inside of HTML is a box. An HTML document is a set of boxes within boxes. We can style these boxes and describe how they should interact with one another using CSS. We'll be consulting a few resources as we go to see how HTML & CSS work together, so here are some links for your reference:

## Resources 
- [Box model demo](http://guyroutledge.github.io/box-model/)
- [skins (color schemes)](https://tachyons.io/docs/themes/skins/)
- [Jotform (to create forms)](https://www.jotform.com/)
- [HTML tags references](https://www.w3schools.com/tags/default.asp)
- [CSS properites reference](https://www.w3schools.com/cssref/)
- [postimages.org](https://postimages.org/) for image uploading

## Main Concepts of spacing

Margin: the space between html elements
Padding: the space between the content of an element and its border
Height: the height of an element (we can specify pixel widths or percentages or even a unit relative to the height of the viewport)
Width: the width of an element (again, we can specify pixel widths or percentages or even a unit relative to the height of the viewport)

## Home Section

In the home section, we'll want to check out some of the skins and choose a color scheme for the main section. The way that CSS talks to HTML is by using selectors. The main ones we'll be using are class and ID selectors. When we target an element that has a class we use a dot. When we target an element with an id, we use a `#`

```html
<section id="main" class="panel"></section>
```

```css
.panel {
  height: 75vh;
}
#main {
  background: black;
  color: white;
}
```
Both of these CSS declarations will apply to our section we added.
## About Section
For the about section, we're going to deal with images and text alignment.
## Photos Section
For the photos section, we'll be building out columns. We also want to add captions, so we'll need to make sure that the boxes can float along side of each other. We'll also need to upload some images that we can use for this section. So, we can use [postimages.org] for that
### Adding Photos

To add photos to our app, we'll want to get URLs for all of them. For best performance in this site we're building, the photos should be portrait (taller than wide). To make things easier on us here, we'll want to upload our images to [postimages.org](https://postimages.org/). When we do this we'll want to choose the direct link option to get the URLs. They should look something like this: 
```
https://s8.postimg.cc/8zhe8z0s5/ko-headshot.jpg
https://s8.postimg.cc/nb0fu1jvp/crazy-hair-looking-out-small.jpg
https://s8.postimg.cc/bynuc9iwl/creator-state-of-mind-small.jpg
https://s8.postimg.cc/r7drq1kat/masquerade-small.jpg
```
## Contact Section
To add the contact form, we'll need to create an account with [jotform](https://www.jotform.com/)


## Adding Responsive features

We can add media queries to our CSS which specify that we only want certain styles to appear on some size screens. To get a sense of where these breakpoints are, we can add something like this to our css and then play around with resizing the browser to see where everything disappears. We can change the `45` number of ems to adjust where the breakpoint is. When our design starts to break, we call that a breakpoint. We're able to then define styles that only apply to screen sized between two breakpoints.

```
@media screen and (max-width: 65em) {
  body {
    display: none;
  }
}
```

When we resize the browser, some of the sections are running out of space at the bottom. One thing we can do to get around this is to change the way we're setting the height of those containers. Instead of specifying an actual height, we can set a minimum height. This will allow the container to expand in height when the content wraps on smaller screens.

```
/* sections */
.panel {
  min-height: 75vh;
  padding: 10% 20%;
  font-size: 2em;
}
```

When we add photos to our site
