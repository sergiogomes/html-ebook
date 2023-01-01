# HTML Basics

HTML is a standard defined by the WHATWG, an acronym for Web Hypertext Application Technology Working Group, an organization formed by people working on the most popular web browser. Which means Google, Mozilla, Apple, and Microsoft control it. In the past, the W3C (World Wide Web Consortium) was responsible for creating the HTML standard. The control informally moved from W3C to WHATWG when it became clear that the W3C push towards XHTML was not a good idea. If you've never heard of XHTML, here's a short story. In the early 2000s, we all believed the future of the Web would be XML. So HTML moved from an SGML-based authoring language to an XML markup language. It was a significant change.
We had to know and respect more rules. Eventually, browser vendors realized this was not the right path for the Web, and they pushed back, creating what is now known as HTML5. W3C disagreed with giving up control of HTML, and for years we had two competing standards, each one aiming to be the official one. Finally, on 28 May 2019, it was made official by W3C that the "true" HTML version was the one published by WHATWG. I mentioned HTML5. Let me explain this little story. It isn't apparent, as with many things in life when many actors are involved, yet it's also fascinating.
We had HTML version 1 in 1993. Here's the original RFC: <https://tools.ietf.org/html/rfc1983>. HTML 2 followed in 1995. We got HTML 3 in January 1997 and HTML 4 in December 1997. Busy times! 20+ years went by, we had this entire XHTML thing, and eventually, we got to this HTML5 which is not just HTML anymore. HTML5 is a term that now defines a whole set of technologies, including HTML, but adding many APIs and standards like WebGL, SVG, and more. The key thing to understand here is this: there is no such thing as an HTML version now. It's a living standard. Like CSS, which is called "3", but in reality, it is a bunch of independent modules developed separately. Like JavaScript, where we have one new edition each year, but nowadays, the only thing that matters is which engine implements individual features. Yes, we call it HTML5, but HTML4 is from 1997. That's a long time for anything, let alone for the Web. Here is where the standard now "lives": <https://html.spec.whatwg.org/multipage>. HTML is the markup language we use to structure the content we consume on the Web. There are different ways to serve HTML to the browser.

- A server-side application can generate it depending on the request or session data, such as a Rails, Laravel, or Django application.
- A JavaScript client-side application can generate the HTML on the fly.
- In the simplest case, it can be stored in a file and served to the browser by a Web server.

Let's dive into this last case. Although it's probably the least popular way to generate HTML in practice, it's still essential to know the basic building blocks. By convention, an HTML file has a .html or .htm extension. Inside this file, we organize the content using tags. Tags wrap the content, and each tag gives a special meaning to the text it wraps. Let's give a few examples.
This HTML snippet creates a paragraph using the p tag:

```html
<p>A paragraph of text</p>
```

This HTML snippet creates a list of items using the ul tag, which means unordered list, and the li tags, which means list item:

```html
<ul>
  <li>First item</li>
  <li>Second item</li>
  <li>Third item</li>
</ul>
```

When the browser serves an HTML page, it interprets the tags and renders the elements according to the rules that define their visual appearance. Some rules are built-in, such as how a list renders or a link is underlined in blue. You set some other rules with CSS. HTML is not presentational. It's not concerned with how things look. Instead, it's concerned with what things mean. It's up to the browser to determine how things look, with the directives defined by who builds the page with the CSS language. Those two examples I made are HTML snippets taken outside of a page context.
