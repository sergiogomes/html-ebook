# Attributes

The starting tag of an element can have particular snippets of information we can attach called attributes.
Attributes have the key="value" syntax:

```html
<p class="a-class">A paragraph of text</p>
```

You can also use single quotes, but using double quotes in HTML is an excellent convention.
We can have many of them:

```html
<p class="a-class" id="an-id">A paragraph of text</p>
```

And some attributes are boolean, meaning you only need the key:

```html
<script defer src="file.js"></script>
```

The class and id attributes are the most common you will find used.
They have a special meaning and are helpful in both CSS and JavaScript.
The difference between the two is that an id is unique in the context of a web page; we cannot duplicate it.
On the other hand, classes can appear multiple times on multiple elements. Plus, an id is just one value. A class can hold multiple values separated by a space:

```html
<p class="a-class another-class">A paragraph of text</p>
```

It's common to use the dash - to separate words in a class value, but it's just a convention.
Those are just two of the possible attributes you can have. Some attributes are only used for one tag and are highly specialized.
You just saw id and class, but we have other ones, like style. We can use style to insert inline CSS rules on an element.
