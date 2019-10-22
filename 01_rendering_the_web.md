# RENDERING THE WEB

## Why should I care about this?

## The http request

1. The browser makes an HTTP GET request to a resource (https://www.w3.org/)

2. The server responds with:
* Status Code: 200
* Header: Content-Type: text/html; charset=UTF-8
* Body: bynary content

3. The browser renders the web

## But this is just an HTML document!

### Translating things to the browser language

1. Parse the HTML and create the DOM
  - The tree
  - It is just an API, not JavaScript
  - [Chrome dev tool](img/DOM.png)

2. Parse the CSS and create the CSSOM
  - The tree
  - Sources
  - inheritance on cascade
  - CSSOM API [How to](https://css-tricks.com/an-introduction-and-guide-to-the-css-object-model-cssom/), [CSS Type API](https://developers.google.com/web/updates/2018/03/cssom)
3. Combine both and create the Render Tree
  - Waiting and filtering
  - [Final Tree](img/render_tree.png)

### Beauty for the eyes

1. Building a layout
  - The reflow, pixels everywhere
2. Drawing something nice
  - The layers, as photoshop
  - Rasterization to bring styles to life
3. Serving web on a plate
  - [The tiles](img/tiles.png)
  - The rendering engine (Webkit, Gecko...)

### Not so beautyful flash of unstyled content (FOUC)

1. My Angular application just says "Loading", What just happened?
2. Render blocked by links and scripts
  * Asynchronous links
  * Synchronous scripts
3. Again the Render Tree
4. Speeding up with [async and defer](https://www.growingwiththeweb.com/2014/02/async-vs-defer-attributes.html)