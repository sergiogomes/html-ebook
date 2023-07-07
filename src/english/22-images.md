# Images

Images can be displayed using the `img` tag.
This tag accepts a src attribute, which we use to set the image source:

```html
<img src="image.png">
```

We can use a broad set of images. The most common ones are PNG, JPEG, GIF, SVG, and, more recently, WebP.
The HTML standard requires an `alt` attribute to be present to describe the image. It is used by screen readers and also by search engine bots:

```html
<img src="dog.png" alt="A picture of a dog">
```

You can set the `width` and `height` attributes to set the space the element will take so that the browser can account for it and not change the layout when the image is fully loaded. It takes a numeric value expressed in pixels.

```html
<img src="dog.png" alt="A picture of a dog" width="300" height="200">
```

## The figure tag

We can often use the `figure` tag along with the `img` tag.
`figure` is a semantic tag often used when you want to display an image with a caption. You use it like this:

```html
<figure>
  <img src="dog.png" alt="A nice dog">
  <figcaption>A nice dog</figcaption>
</figure>
```

The `figcaption` tag wraps the caption text.
