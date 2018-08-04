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

## What You'll Be Able to Do

- Identify HTML tags and put them together to build a website.
- Understand the Box Model that governs how elements take up space within a web page.
- Read documentation and use what you read to experiment and improve your site with what you learn.
- Build columns with HTML & CSS that will collapse into rows on mobile devices
- Add images to your site by using publically available URLs or by posting images on [postimages.org](https://postimages.org/)
- Use the [codepen.io](https://codepen.io/) editor to build and publish your project to the web


## Adding Photos

To add photos to our app, we'll want to get URLs for all of them. For best performance in this site we're building, the photos should be portrait If they're not currently posted on the int


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
