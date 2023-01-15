# Page Tags

## nav

We can use the `nav` tag to create the page navigation markup. Inside it, we typically add a `ul` or an `ol` list:

```html
<nav>
    <ol> 
        <li><a href="/">Home</a></li>
        <li><a href="/blog">Blog</a></li>
    </ol>
</nav>
```

## aside

We can use the `aside` tag to add extra content related to the main content.
A box where to add a quote, for example. Or a sidebar.
Example:

```html
<div>
  <p>some text..</p>
  <aside>
    <p>A quote..</p>
  </aside>
  <p>other text...</p>
</div>
```

Using `aside` signals that the things it contains are not part of the regular flow of the section it lives.

## header

We can use the `header` tag to represent a part of the page that is the introduction. It can, for example, contain one or more heading tags ( `h1` - `h6` ), the tagline for the article, and an image.

```html
<body>
  <header>
    <h1>Article title</h1>
  </header>
  ...
</body>
```

## main

We can use the `main` tag to represent the main part of a page:

```html
<body> 
  .... 
  <main>
    <p>....</p>
  </main>
  ...
</body>
```

## footer

We can use the `footer` tag to determine the footer of an article or the footer of the page:

```html
<article> 
  ....
  <footer>
    <p>Footer notes..</p>
  </footer>
</article>
```
