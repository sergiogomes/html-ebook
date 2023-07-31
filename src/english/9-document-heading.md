# The Document Heading

The head tag contains unique tags that define the document properties.
It's always written before the body tag, right after the opening html tag:

```html
<!DOCTYPE html>
<html>
  <head>
    ...
  </head> 
  ...
</html>
```

We never use attributes on this tag. And we don't write content in it.
It's just a container for other tags. Inside it, we can have a wide variety of tags, depending on what you need to do:

- title
- script
- noscript
- link
- style
- base
- meta

## The title tag

The title tag determines the page title. The browser displays it, and it's essential as it's one of the critical factors for Search Engine Optimization (SEO).

## The script tag

We use the script tag to add JavaScript to the page.
You can include it inline, using an opening tag, the JavaScript code, and then the closing tag:

```html
<script> 
  some JS ...
</script> 
```

Or you can load an external JavaScript file by using the src attribute:

```html
<script src="file.js"></script>
```

The default attribute for type is text/javascript, so it's completely optional.

There is something essential to know about this tag. Sometimes this tag is used at the bottom of the page, just before the closing </body> tag. Why? For performance reasons. Loading scripts, by default, block the rendering of the page until the script is parsed and loaded.
By putting it at the bottom of the page, the script is loaded and executed after the whole page is already parsed and loaded, giving a better user experience. This is now bad practice. Let the script live in the head tag.
In modern JavaScript, we have an alternative that is more performant than keeping the script at the bottom of the page: the defer attribute. Here we have an example that loads a file.js relative to the current URL:

```html
<script defer src="file.js"></script>
```

The defer attribute triggers the faster path to a fast-loading page and fast-loading JavaScript.

> Note: the async attribute is similar but a worse option than defer. I describe it in more detail in the Javascript Ebook.

## The noscript tag

The noscript tag detects when scripts are disabled in the browser.

> Note: users can choose to disable JavaScript scripts in the browser settings. Or the browser might not support them by default.

It is used differently depending on whether placed in the document head or the document body. We're talking about the document head now, so let's first introduce this usage.
In this case, the noscript tag can only contain other tags:

- link tags
- style tags
- meta tags

To alter the resources served by the page, or the meta information, if scripts are disabled.
In this example, I set an element with the no-script-alert class to display if scripts are disabled, as it was display: none by default:

```html
<!DOCTYPE html>
<html>
  <head>
    ... 
    <noscript>
      <style>
        .no-script-alert {
          display: block;
        } 
      </style>
    </noscript>
    ... 
  </head> 
  ... 
</html> 
```

Let's solve the other case: if put in the body, it can contain content, like paragraphs and other tags, and renders in the UI.

## The link tag

We use the link tag to set relationships between a document and
other resources, mainly used to link an external CSS file to be loaded. This element has no closing tag.
Usage:

```html
<!DOCTYPE html>
<html>
  <head>
    ... 
    <link href="file.css" rel="stylesheet">
    ... 
  </head> 
  ... 
</html> 
```

The media attribute allows the loading of different stylesheets depending on the device's capabilities:

```html
<link href="file.css" media="screen" rel="stylesheet">
<link href="print.css" media="print" rel="stylesheet">
```

We can also link to resources other than stylesheets. For example, we can associate an RSS feed using

```html
<link rel="alternate" type="application/rss+xml" href="/index.xml">
```

Or we can associate a favicon using:

```html
<link rel="apple-touch-icon" sizes="180x180" href="/assets/apple-touch-icon.png">
<link rel="icon" type="image/png" sizes="32x32" href="/assets/favicon-32x32.png">
<link rel="icon" type="image/png" sizes="16x16" href="/assets/favicon-16x16.png">
```

We could also use the link tag for multi-page content indicating the previous and next page with rel="prev" and rel="next", primarily for Google. As of 2019, Google announced it does not use this tag anymore: <https://twitter.com/googlewmc/status/1108726443251519489> because it can find the correct page structure without it.

## The style tag

We can use the style tag to add styles to the document rather than loading an external stylesheet. Usage:

```html
<style> 
  .some-css {} 
</style>
```

As with the link tag, you can use the media attribute to use that CSS only on the specified medium:

```html
<style media="print">
  .some-css {}
</style>
```

## The base tag

We can use the base tag to set a base URL for all relative URLs contained in the page.

```html
<!DOCTYPE html>
<html>
  <head>
    ... 
    <base href="https://www.sergiogomes.com/">
    ... 
  </head> 
  ... 
</html>
```

## The meta tag

Meta tags perform various tasks, and they are significant, especially for SEO. Meta elements only have the starting tag. The most basic one is the description meta tag:

```html
<meta name="description" content="A nice page">
```

Google might use this to generate the page description in its result pages if it finds it better describes the page than the on-page content.
We can use the charset meta to set the page character encoding. UTF-8 in most cases:

```html
<meta charset="utf-8">
```

The robots meta tag instructs the Search Engine bots whether to index a page or not:

```html
<meta name="robots" content="noindex">
```

Or if they should follow links or not:

```html
<meta name="robots" content="nofollow">
```

You can combine them:

```html
<meta name="robots" content="noindex, nofollow">
```

The default behavior is index, follow.
You can use other properties, including nosnippet, noarchive, noimageindex and more.
You can also tell Google instead of targeting all search engines:

```html
<meta name="googlebot" content="noindex, nofollow">
```

Other search engines might have their own meta tag, too.
Speaking of which, we can tell Google to disable some features. The notranslate meta tag prevents the translation functionality in the search engine results:

```html
<meta name="google" content="notranslate">
```

We can use the viewport meta tag to tell the browser to set the page width based on the device width.

```html
<meta name="viewport" content="width=device-width, initial-scale=1">
```

See more on this tag: <https://developer.mozilla.org/en-US/docs/Mozilla/Mobile/Viewport_meta_tag>.

Another rather popular meta tag is the http-equiv="refresh" one. This line tells the browser to wait 3 seconds, then redirect to that other page:

```html
<meta http-equiv="refresh" content="3;url=http://www.sergiogomes.com/another-page">
```

Using 0 instead of 3 will redirect as soon as possible.

After this document's introduction, we can start diving into the document's body.
