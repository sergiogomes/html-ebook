# IFrames

The `iframe` tag allows us to embed content coming from other origins (other sites) into our web page.
Technically, an iframe creates a new nested browsing context. This means that nothing in the iframe interferes with the parent page and vice versa. JavaScript and CSS do not "leak" to/from iframes.
Many sites use iframes to perform various things. You might be familiar with Codepen, Glitch, or other sites that allow you to code in one part of the page, and you see the result in a box. That's an iframe.
You create one this way:

```html
<iframe src="page.html"></iframe>
```

You can load an absolute URL, too:

```html
<iframe src="https://site.com/page.html"></iframe>
```

You can set width and height parameters (or set them using CSS). Otherwise, the iframe will use the defaults, a 300x150 pixels box:

```html
<iframe src="page.html" width="800" height="400"></iframe>
```
