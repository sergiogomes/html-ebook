# HTML Page Structure

Let's make an example of a proper HTML page. Things start with the Document Type Declaration, a way to tell the browser this is an HTML page and which version we are using.
Modern HTML uses this doctype:

```html
<!DOCTYPE html>
```

Then we have the html element, which has an opening and closing tag:

```html
<!DOCTYPE html>
<html> 
  ...
</html> 
```

Most tags come in pairs with an opening tag and a closing tag. We write the closing tag the same as the opening tag but with a / (forward slash)

```html
<sometag>some content</sometag>
```

There are a few self-closing tags, meaning they don't need a separate closing tag as they don't contain anything. Example img:

```html
<img />
```

We use the html as the starting tag at the beginning of the document, right after the document type declaration. The html ending tag is the last thing present in an HTML document. Inside the html element, we have two elements: head and body:

```html
<!DOCTYPE html>
<html>
  <head>
    ... 
  </head>
  <body>
    ...
  </body>
</html> 
```

Inside the head, we will have tags essential to creating a web page, like the title, the metadata, and internal or external CSS and JavaScript. Mostly things that do not directly appear on the page but only help the browser (or bots like the Google search bot) display it correctly.
Inside the body, we will have the content of the page.
