# Form Submit

The type="submit" field is a button that, once pressed by the user, submits the form:

```html
<input type="submit">
```

The value attribute sets the text on the button, which, if missing, shows the "Submit" text:

```html
<input type="submit" value="Click me">
```

## Form validation

Browsers provide client-side validation functionality to forms.
We can set fields as required, ensuring they are not empty, and enforce a specific format for the input of each field.
Let's see both options.

### Set fields as required

The required attribute helps us with validation. If the user doesn't fill out the field, client-side validation fails, and the browser does not submit the form:

```html
<input type="text" name="username" required>
```

### Enforce a specific format

I described the type="email" field above. It automatically validates the email address according to a format set in the specification.
In the type="number" field, I mentioned the min and max attribute to limit values entered to an interval.
We can do more.
We can enforce a specific format on any field.
The pattern attribute allows us to set a regular expression to validate the value.
I recommend reading my Regular Expressions Guide at <https://www.sergiopgomes.com/javascript-regular-expressions/>.
pattern="https://.*"

```html
<input type="text" name="username" pattern="[a-zA-Z{8}">
```
