# Tags that Interact with Text

## The p tag

This tag defines a paragraph of text.

```html
<p>Some text</p>
```

It's a block element.
Inside it, we can add any inline element, like `span` or `a`. We cannot add block elements.
We cannot nest a `p` element into another one.
Browsers style a paragraph with a margin on top and at the bottom by default (16px in Chrome, but the exact value might vary between browsers). The margin causes space between two consecutive paragraphs, replicating what we think of as a "paragraph" in a printed text.

## The span tag

The `span` is an inline tag used to create a section in a paragraph that we can target using CSS:

```html
<p>A part of the text <span>and here another part</span></p>
```

## The br tag

The `br` tag represents a line break. It's an inline element and does not need a closing tag.
We use it to create a new line inside a `p` tag without creating a new paragraph. And compared to creating a new paragraph, it does not add additional spacing.

```html
<p>Some text<br>A new line</p>
```

## The heading tags

HTML provides us with 6 heading tags. From most important to least important, we have `h1`, `h2`, `h3`, `h4`, `h5`, and `h6`.
Typically a page will have one `h1` element, the page title. Then you have one or more `h2` elements depending on the page content.
Headings, especially the heading organization, are also essential for SEO, and search engines use them in various ways.
The browser will render the `h1` tag bigger and will make the elements size smaller as the number near `h` increases by default

```html
<h1>h1</h1>
<h2>h2</h2>
<h3>h3</h3>
<h4>h4</h4>
<h5>h5</h5>
<h6>h6</h6>
<p>p</p>
```

All headings are block elements. They cannot contain other elements, just text.

## The strong tag

We use the `strong` tag to mark the text inside it as strong, which is essential, as it's not a visual hint but a semantic one. Depending on the medium used, its interpretation will vary.
Browsers make the text in this tag `bold` by default.

```html
<p>This paragraph is very <strong>important!</strong></p>
```

## The em tag

We use the `em` tag to mark the text inside it as emphasized. Like with strong, it's not a visual but a semantic hint. Browsers make the text in this `italic` by default.

```html
<p><em>Status quo</em> is a Latin phrase that means the existing state of affairs</p>
```

## Quotes

The `blockquote` tag helps insert citations in the text.
Browsers apply a margin to the `blockquote` element by default (Chrome applies a 40px left and right margin and a 10px top and bottom margin)

```html
<blockquote>
  Most people spend more time and energy going around problems than in trying to solve them.<br>
  - Henry Ford
</blockquote>
```

And we use the `q` tag for inline quotes.

```html
<p>Henry Ford said <q>Most people spend more time and energy going around problems than in trying to solve them.</q> in the 20th century</p>
```

## Horizontal line

Not really based on text, but we can use the `hr` tag inside a page. It means horizontal rule and adds a horizontal line to the page.
Useful to separate sections on the page.

```html
<hr>
```

## Code blocks

The `code` tag is especially useful to show code because browsers give it a monospaced font.
That's typically the only thing that browsers do. Here is the CSS applied by Chrome:

```css
code {
  font-family: monospace;
}
```

This tag is typically wrapped in a `pre` tag because the code element ignores whitespace and line breaks like the `p` tag.
Chrome gives `pre` this default styling to prevent white space from collapsing and makes it a block element.

```css
pre {
  display: block;
  font-family: monospace;
  white-space: pre;
  margin: 1em 0px;
}
```

## Lists

We have three types of lists:

- unordered lists
- ordered lists
- definition lists

We create unordered lists using the `ul` tag. Each item in the list with the `li` tag:

```html
<ul>
  <li>eggs</li>
  <li>bacon</li>
</ul>
```

Ordered lists are similar, just made with the `ol` tag:

```html
<ol>
  <li>First</li>
  <li>Second</li>
</ol>
```

The difference is that ordered lists have a number before each item.
Definition lists are different. You have a term and its definition:

```html
<dl>
  <dt>Sergio</dt>
  <dd>The name</dd>
  <dt>Gomes</dt>
  <dd>The surname</dd>
</dl> 
```

You rarely see them in the wild, for sure not much as `ul` and `ol`, but sometimes they might be helpful.

## Other text tags

There are several tags with presentational purposes:

- the mark tag
- the ins tag
- the del tag
- the sup tag
- the sub tag
- the small tag
- the i tag
- the b tag

Here is an example of the visual rendering of them, which is applied by default by browsers:

```html
<mark>mark</mark>
<ins>ins</ins>
<del>del</del>
<sup>sup</sup>
<sub>sub</sub>
<small>small</small>
<i>i</i>
<b>b</b>
```

You might wonder, how is `b` different than `strong`? And how `i` is different than `em`?
The difference lies in the semantic meaning. While `b` and `i` are a direct hint at the browser to make a text bold or italic, `strong` and `em` give the text a special meaning. It's up to the browser to provide the styling, which is the same as `b` and `i`, by default. Although you can change that using CSS.

There are many other, less-used tags related to text. I just mentioned the ones that I see used the most.
