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

We can use the `type="button"` input fields to add additional buttons to the form that are not submit buttons:

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
You define a set of `type="radio"` inputs, all with the same `name` attribute, and different `value` attribute:

```html
<input type="radio" name="color" value="yellow">
<input type="radio" name="color" value="red">
<input type="radio" name="color" value="blue">
```

Once the form is submitted, the `color` data property will have only one value. There's always one element checked. The first item is the one checked by default. You can set the value that's pre-selected using the `checked` attribute. You can use it only once per radio input group.

## Checkboxes

Like radio boxes, checkboxes can create a set of choices, but we can choose multiple values or none.
You define a set of `type="checkbox"` inputs, all with the same `name` attribute and different `value` attribute:
All those checkboxes are unchecked by default. Use the `checked` attribute to enable them on page load.

```html
<input type="checkbox" name="color" value="yellow">
<input type="checkbox" name="color" value="red">
<input type="checkbox" name="color" value="blue">
```

Since this input field allows multiple values, the form sends the values to the server as an array upon form submission.

## Date and time

We have a few input types to accept date values.
The `type="date"` input field allows the user to enter a date and shows a date picker if needed:

```html
<input type="date" name="birthday">
```

The `type="time"` input field allows the user to enter a time and shows a time picker if needed:

```html
<input type="time" name="time-to-pickup">
```

The `type="month"` input field allows the user to enter a month and a year:

```html
<input type="month" name="choose-release-month">
```

The `type="week"` input field allows the user to enter a week and a year:

```html
<input type="week" name="choose-week">
```

All those fields allow limiting the range and the step between each value. I recommend checking MDN for the little details on their usage.
The `type="datetime-local"` field lets you choose a date and a time.

```html
<input type="datetime-local" name="date-and-time">
```

## Color picker

You can let users pick a color using the `type="color"` element:

```html
<input type="color" name="car-color">
```

You set a default value using the `value` attribute:

```html
<input type="color" name="car-color" value="#000000">
```

The browser will take care of showing a color picker to the user.

## Range

This input element shows a `slider` element. People can use it to move from a starting value to an ending value:

```html
<input type="range" name="age" min="0" max="100" value="30">
```

You can provide an optional `step`:

```html
<input type="range" name="age" min="0" max="100" value="30" step=
"10">
```

## Telephone

We can use the `type="tel"` input field to enter a phone number:

```html
<input type="tel" name="telephone-number">
```

The main selling point for `tel` over `text` is on mobile, where the device can choose to show a numeric keyboard.
Specify a `pattern` attribute for additional validation:

```html
<input type="tel" pattern="[0-9]{3}-[0-9]{8}" name="telephone-number">
```

## URL

We can use the `type="url"` field to enter a URL.

```html
<input type="url" name="website">
```

We can validate it using the `pattern` attribute:

```html
<input type="url" name="website"  pattern="https://.*">
```

## The textarea tag

The `textarea` element allows users to enter multi-line text. Compared to `input`, it requires an ending tag:

```html
<textarea></textarea>
```

You can set the dimensions using CSS, but also using the `rows` and `cols` attributes:

```html
<textarea rows="20" cols="10"></textarea>
```

As with the other form tags, the `name` attribute determines the name in the data sent to the server:

```html
<textarea name="article"></textarea>
```

## The select tag

We can use this tag to create a drop-down menu.
The user can choose one of the options available.
We create each option using the `option` tag. We add a `name` to the select and a `value` to each option:

```html
<select name="color">
  <option value="red">Red</option>
  <option value="yellow">Yellow</option>
</select>
```

You can set an option `disabled`:

```html
<select name="color">
  <option value="red" disabled>Red</option>
  <option value="yellow">Yellow</option>
</select>
```

You can have one empty option:

```html
<select name="color">
  <option value="">None</option>
  <option value="red">Red</option>
  <option value="yellow">Yellow</option>
</select>
```

We can group options using the `optgroup` tag. Each option group has a `label` attribute:

```html
<select name="color">
  <optgroup label="Primary">
    <option value="red">Red</option>
    <option value="yellow">Yellow</option>
    <option value="blue">Blue</option>
  </optgroup>
  <optgroup label="Others">
    <option value="green">Green</option>
    <option value="pink">Pink</option>
  </optgroup>
</select>
```
