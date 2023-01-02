# The Document Body

After the closing head tag, we can only have one thing in an HTML document: the `body` element.

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

Just like the head and html tags, we can only have one body tag on the page.
All the tags that define the page's content are inside the body tag.
Technically, the start and end tags are optional. But it is a good practice to add them.
In the following chapters, we'll define the various tags you can use inside the page body.
But before, we must introduce a difference between block and inline elements.

## Block Elements vs. Inline Elements

Visual elements, the ones defined in the page body, can be generally classified into two categories:

- block elements ( p, div, heading elements, lists, list items, etc...)
- inline elements ( a, span, img, etc...)

What is the difference?
When positioned on the page, block elements do not allow other elements next to them, to the left or the right.
Inline elements instead can sit next to other inline elements.
The difference also lies in the visual properties we can edit using CSS. We can alter block elements' `width`/`height`, `margin`, `padding`, and `border`. We can't do that for inline elements.

> Note that using CSS, we can change the default for each element, setting a p tag to be inline, for example, or a span to be a block element.

Another difference is that block elements can contain inline elements. The reverse is not valid.
Some block elements can contain other block elements, but it depends. The `p` tag, for example, does not allow such a thing.
