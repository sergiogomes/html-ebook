# Forms

Forms are how we interact with a page or an app built with Web technologies.
We have a set of controls, and when you submit the form, either with a click on a "submit" button or programmatically, the browser will send the data to the server.
By default, this data sending causes the page to reload after sending the data. But using JavaScript, we can alter this behavior using `event.preventDefault()`.
We create a form using the `form` tag:

```html
<form>
  ...
</form>
```

By default, the `form` submits using the `GET` HTTP method. Which has its drawbacks, and usually, we want to use `POST`.
We can set the form to use `POST` when submitted by using the method attribute:

```html
<form method="POST">
  ...
</form>
```

The form is submitted, either using `GET` or `POST`, to the same URL where it resides.
So if the form is on the <https://www.sergiopgomes.com/contacts> page, pressing the "submit" button will request that exact URL which might result in nothing happening.
We need something server-side to handle the request, and typically we "listen" for those form-submit events on a dedicated URL.
You can specify the URL via the action parameter:

```html
<form action="/new-contact" method="POST">
  ...
</form>
```

This will cause the browser to submit the form data using `POST` to the /new-contact URL on the exact origin.
If the `origin` (protocol + domain + port) is <https://www.sergiopgomes.com> (port 80 is the default), the form data will be sent to <https://www.sergiopgomes.com/new-contact>.
I talked about data. Which data?
Users provide data via the set of controls that are available on the Web platform:

- input boxes (single-line text)
- text areas (multiline text)
- select boxes (choose one option from a drop-down menu)
- radio buttons (choose one option from a list always visible)
- checkboxes (choose zero, one, or more options)
- file uploads
- and more!

Let's introduce each one of them in the following form fields overview.
