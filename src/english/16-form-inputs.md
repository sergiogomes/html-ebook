# Form Inputs

## The input tag

The `input` field is one of the most widely used form elements. It's also a versatile element and can change its behavior based on the `type` attribute.
The default behavior is to be a single-line text input control:

```html
<input>
```

Equivalent to using:

```html
<input type="text">
```

As with all the other fields that follow, we need to give the field a `name` for its content to be sent to the server when the `form` is submitted:

```html
<input type="text" name="username">
```

We use the `placeholder` attribute to show some text in light gray when the field is empty. Useful to add a hint to the user for what to type in:

```html
<input type="text" name="username" placeholder="Your username">
```

## Email

Using `type="email"` will validate client-side (in the browser) an email for correctness (semantic correctness, not ensuring the email address exists) before submitting.

```html
<input type="email" name="email" placeholder="Your email">
```

## Password

Using `type="password"` will make every key entered appear as an asterisk (`*`) or dot, useful for fields that host a password.

```html
<input type="password" name="password" placeholder="Your password">
```

## Numbers

We can have an `input` element accept only numbers:

```html
<input type="number" name="age" placeholder="Your age">
```

We can specify a `minimum` and `maximum` value accepted:

```html
<input type="number" name="age" placeholder="Your age" min="18" max="110">
```

The `step` attribute helps identify the steps between different values. For example, this accepts a value between 10 and 50 in steps of 5:

```html
<input type="number" name="a-number"  min="10" max="50" step="5">
```

## Hidden field

We can hide fields from the user. The `form` will submit them along with the other visible fields:

```html
<input type="hidden" name="some-hidden-field" value="some-value">
```

We commonly use it to store values like a CSRF token for security and the user identification or even to detect robots sending spam using special techniques.
We can also use it to identify a `form` and its action.

## Setting a default value

All those fields accept a predefined value. If the user does not change it, this will be the `value` sent to the server:

```html
<input type="number" name="age" value="18">
```

If you set a `placeholder`, it will only appear if the user clears the input field `value`:

```html
<input type="number" name="age" placeholder="Your age" value="18">
```
