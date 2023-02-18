# Form Other Fields

## File uploads

You can load files from your local computer and send them to the server using a `type="file"` input element:

```html
<input type="file" name="secret-documents">
```

You can attach multiple files:

```html
<input type="file" name="secret-documents" multiple>
```

You can specify one or more file types allowed using the `accept` attribute. This accepts images:

```html
<input type="file" name="secret-documents" accept="image/*">
```

You can use a specific `MIME` type, like `application/json`, or set a file extension like .pdf. Or set multiple file extensions like this:

```html
<input type="file" name="secret-documents" accept=".jpg, .jpeg, .png">
```

## Buttons

We can use the type="button" input fields to add additional buttons to the form that are not submit buttons:

```html
<input type="button" value="Click me">
```

They are used to programmatically do something using JavaScript.
There is a special field rendered as a button, whose special action is to clear the entire form and bring back the state of the fields to the initial one:

```html
<input type="reset">
```

## Radio buttons

We can use Radio buttons to create a set of choices, of which we select one option, and all the others are disabled.
The name comes from old car radios that had this kind of interface.
You define a set of `type="radio"` inputs, all with the same name attribute, and different `value` attribute:

```html
<input type="radio" name="color" value="yellow">
<input type="radio" name="color" value="red">
<input type="radio" name="color" value="blue">
```

Once the form is submitted, the `color` data property will have only one value. There's always one element checked. The first item is the one checked by default. You can set the value that's pre-selected using the `checked` attribute. You can use it only once per radio input group.
