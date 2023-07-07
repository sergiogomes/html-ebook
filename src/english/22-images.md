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

## Responsive images using srcset

With the `srcset` attribute, we can set responsive images that the browser can use depending on the pixel density or window width, according to your preferences. This way, it can only download the resources it needs to render the page without downloading a larger image if it's on a mobile device, for example.
Here's an example where we give four additional images for four different screen sizes:

```html
<img
  src="dog.png"
  alt="A picture of a dog."
  srcset="
    dog-500.png 500w,
    dog-800.png 800w,
    dog-1000.png 1000w,
    dog-1400.png 1400w
  "
>
```

In the `srcset`, we use the `w` measure to indicate the window width. Since we do so, we also need to use the `sizes` attribute:

```html
<img
  src="dog.png"
  alt="A picture of a dog."
  sizes="(max-width: 500px) 100vw, (max-width: 900px) 50vw, 800px"
  srcset="
    dog-500.png 500w,
    dog-800.png 800w,
    dog-1000.png 1000w,
    dog-1400.png 1400w
  "
>
```

In this example, the `(max-width: 500px) 100vw, (max-width: 900px) 50vw, 800px` string in the sizes attribute describes the size of the image compared to the viewport, with multiple conditions separated by a semicolon.
The media condition `max-width: 500px` sets the image size in correlation to the viewport width. In short, if the window size is `< 500px`, it renders the image at 100% of the window size.
If the window size is large but `< 900px`, it renders the image at 50% of the window size.
And if even larger, it renders the image at 800px.
The `vw` unit of measure can be new to you, and in short, one `vw` is 1% of the window width, so `100vw` is 100% of the window width.
A helpful website to generate the `srcset` and progressively smaller images is <https://responsivebreakpoints.com/>.
