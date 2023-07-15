# Accessibility

We must design our HTML with accessibility in mind.

Having accessible HTML means that people with disabilities can use the Web. There are totally blind or visually impaired users, people with hearing loss issues, and many other disabilities.

Unfortunately, this topic does not take the importance it needs and seems less cool than others.

What if a person can't see your page but wants to consume its content? First, how do they do that? They can't use the mouse; they use a `screen reader`. You don't have to imagine that. You can try one now: Google provides the free [ChromeVox Chrome Extension](https://chrome.google.com/webstore/detail/screen-reader/kgejglhpjiefppelpmljglcjbhoiplfn). Accessibility must also allow tools to select elements or navigate the pages easily.

We don't always build web pages and Web apps with accessibility as one of our first goals, and maybe version 1 is released not accessible, but it's possible to make a web page accessible after the fact. The Sooner, is better, but there is always time.

It's essential, and in my country, websites built by the government or other public organizations must be accessible.

What does this mean to make an HTML accessible? Let me illustrate the main things you need to think about.

> Note: there are several other things to care about, which might go in the CSS topic, like colors, contrast, and fonts. Or [how to make SVG images accessible](https://css-tricks.com/accessible-svgs/). I don't talk about them here.

## Use semantic HTML

Semantic HTML is fundamental and one of the main things we must take care of. Let me illustrate a few common scenarios.

It's essential to use the correct structure for heading tags. The most important is `h1`, and you use higher numbers for less important ones, but all the same-level headings should have the same meaning (think about it like a tree structure)

```html
<h1 />
  <h2 />
    <h3 />
  <h2 />
  <h2 />
    <h3 />
      <h4 />
```

Use `strong` and `em` instead of `b` and `i`. Visually they look the same, but the first 2 have more meaning associated with them. `b` and `i` are more visual elements.

Lists are important. A screen reader can detect a list and provide an overview, then let the user choose to get into the list or not.

A table should have a `caption` tag that describes its content:

```html
<table>
  <caption>Dogs age</caption>
  <tr>
    <th>Dog</th>
    <th>Age</th>
  </tr>
  <tr>
    <td>Roger</td>
    <td>7</td>
  </tr>
</table>
```

## Use alt attributes for images

All images must have an `alt` tag describing the image content. It's not just good practice; the HTML standard requires it, and your HTML is valid with it.

```html
<img src="dog.png" alt="picture of my dog">
```

It's also good for search engines if that's an incentive for you to add it.

## Use the role attribute

The `role` attribute lets you assign specific roles to the various elements on your page.
You can assign lots of different roles: complementary, list, listitem, main, navigation, region, tab, alert, application, article, banner, button, cell, checkbox, contentinfo, dialog, document, feed, figure, form, grid, gridcell, heading, img, listbox, row, rowgroup, search, switch, table, tabpanel, textbox, timer.

It's a lot, and for the complete reference of each of them, I give you this [MDN link](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles). But you don't need to assign a role to every element on the page. Screen readers can infer from the HTML tag in most cases. For example, you don't need to add a role tag to semantic tags like `nav`, `button`, and `form`.

Let's take the `nav` tag example. You can use it to define the page navigation like this:

```html
<nav>
  <ul> 
    <li><a href="/">Home</a></li>
    <li><a href="/blog">Blog</a></li>
  </ul>
</nav>
```

If it is a requirement that we should use a `div` tag instead of a `nav`, we can use the navigation role:

```html
<div role="navigation">
  <ul>
    <li><a href="/">Home</a></li>
    <li><a href="/blog">Blog</a></li>
  </ul>
</div>
```

So, we use the `role` tag to assign a meaningful value when the tag does not convey the meaning already.
