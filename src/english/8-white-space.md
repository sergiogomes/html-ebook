# White Space

Pretty important. In HTML, even if you add multiple white spaces into a line, it's collapsed by the browser's CSS engine.
For example, the rendering of this paragraph:

```html
<p>A paragraph of text</p>
```

Is the same as this:

```html
<p>        A paragraph of text</p>
```

And the same as this:

```html
<p>A paragraph

of

       text </p>
```

Using the white-space CSS property, you can change how things behave. You can find more information on how CSS processes white space in the CSS Spec.

Use the syntax that makes things visually more organized and easier to read, but you can use any syntax you like.
I typically favor

```html
<p>A paragraph of text</p>
```

or

```html
<p> 
  A paragraph of text
</p> 
```

Nested tags should be indented with 2 or 4 characters, depending on your preference:

```html
<body> 
  <p> 
    A paragraph of text
  </p>
  <ul> 
    <li>A list item</li>
  </ul>
</body> 
```

> Note: this "white space is not relevant" feature means that if you want to add additional space, it can make you mad. I suggest you use CSS to create more space when needed.

> Note: in exceptional cases, you can use the &nbsp; HTML entity (an acronym that means non-breaking space) - more on HTML entities later. We should not use it in excess, though. CSS is always preferred to alter the visual presentation.
