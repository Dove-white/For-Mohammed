## 🛠️ HTML-Level Form Validation: Best Practices

### Required Fields

Using the HTML `required` attribute is the simplest way to enforce that a user must fill out a field. 

```html
<input type="text" id="first_name" name="first_name" required>
```

* Ensures the browser blocks form submission until the field has a value.

### Pattern Attributes (Regex Validation)

The HTML `pattern` attribute lets you define a **regular expression** to validate input on the client side.

```html
<input
  type="password"
  name="password"
  id="password"
  required
  pattern="(?=.*\d)(?=.*[a-z])(?=.*[A-Z]).{6,}"
  title="Must contain at least one number, one uppercase and lowercase letter, and at least 6 or more characters"
/>
```

* The `title` attribute provides a human-readable explanation when the pattern doesn't match.
* Helps offload basic validation to the browser without JavaScript.

### Placeholder vs. Label

Always use **real `<label>` elements**, not just placeholders for better HTML-level validation and accessibility.

#### Why Not Use Placeholder as Label?

* Placeholders are suggestions, not permanent labels.
* They disappear when the user starts typing, causing potential confusion.
* Using a `<label>` ensures better accessibility.

#### Label Example

```html
<form>
  <div>
    <input type="text" id="first_name" name="first_name" required placeholder=" ">
    <label for="first_name">First Name</label>
  </div>
</form>
```

* The `<label>` stays semantically connected to the input.

#### Email Field Example

```html
<div>
  <input type="email" id="email" name="email" required placeholder=" ">
  <label for="email">Email</label>
  <div>
    Please enter a valid email address.
  </div>
</div>
```

### ✅ Summary

* Use **`required`** for mandatory fields.
* Use **`pattern`** for specific input formats.
* Prefer **real `<label>`s** over placeholders for accessibility.
