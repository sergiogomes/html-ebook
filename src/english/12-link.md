# Links

Links are defined using the `a` tag. We set its destination via the `href` attribute.
Example:

```html
<a href="https://www.sergiopgomes.com">Click here</a>
```

We have the link text Between the starting and closing tags.
The above example is an absolute URL but links also work with relative URLs:

```html
<a href="/about">click here</a>
```

In this case, when clicking the link, the user is moved to the `/about` URL on the current origin.
Be careful with the `/` character. If omitted, the browser will add the test string to the current URL instead of starting from the origin.
For example, I'm on the page <https://www.sergiopgomes.com/axios/>, and I have these links:

- /about once clicked brings me to <https://www.sergiopgomes.com/about>
- about once clicked brings me to <https://www.sergiopgomes.com/axios/about>

Link tags can include other things inside them, not just text. For example, images:

```html
<a href="https://www.sergiopgomes.com/">
  <img src="avatar.jpg">
</a> 
```

Or any other elements except other `a` tags.
If you want to open the link in a new tab, you can use the `target` attribute:

```html
<a href="https://www.sergiopgomes.com/" target="_blank">
  Open in a new tab
</a>
```
