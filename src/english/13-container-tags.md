# Container tags

HTML provides a set of container tags. Those tags can contain an unspecified group of other tags.
We have:

- article
- section
- div

It needs to be clarified to understand the difference between them. Let's see when to use each.

## article

The `article` tag identifies a thing that can be independent of other things on a page.
For example, a list of blog posts on the homepage.
Or a list of links.

```html
<div>
  <article>
    <h2>A blog post</h2>
    <a ...>Read more</a>
  </article>
  <article>
    <h2>Another blog post</h2>
    <a ...>Read more</a>
  </article>
</div>
```

We're not limited to lists: an `article` can be the main element of a page.

```html
<article>
  <h2>A blog post</h2>
  <p>Here is the content...</p>
</article>
```

Inside an article tag, we should have a title ( `h1` - `h6` )

## section

The `section` tag represents a section of a document. Each `section` has a heading tag ( `h1` - `h6` ), then the section body.
Example:

```html
<section>
  <h2>A section of the page</h2>
  <p>...</p>
  <img ...>
</section>
```

It's helpful to break a long article into different sections.
We shouldn't use it as a generic container element because we have the `div` tag.

## div

The `div` tag is the generic container element:

```html
<div>
  ... 
</div>
```

We often add a `class` or an `id` attribute to this element to add styles to it using CSS.
We use `div` in any place where we need a container, and the existing tags are not suited.
