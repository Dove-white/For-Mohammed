## Forms & the `<form>` Tag 🧾

A **form** in HTML is a container for collecting user input. You wrap input elements inside a `<form>` tag, which defines where and how the data gets sent to the server.

```html
<form action="/submit" method="post">
  <!-- form inputs go here -->
  <button type="submit">Submit</button>
</form>
```

The `<form>` element can contain:

* `<input>` — for text, email, number, etc.
* `<label>` — to give input fields a name / description
* `<select>` — dropdowns
* `<textarea>` — for multi-line text
* `<button>` — submit, reset, etc.
* `<fieldset>` & `<legend>` — for grouping related controls
* `<datalist>`, `<option>`, `<optgroup>`, `<output>` — for extra input-related behavior.

---

## Input Types (Text, Email, Password, Number, Date, etc.) ✍️

The `<input>` tag is super versatile. What it does depends on its `type` attribute. Here are some common input types:

```html
<form>
  <input type="text" id="name" name="name" placeholder="Enter your name" required>
  <input type="email" id="email" name="email" placeholder="Enter your email" required>
  <input type="password" id="pw" name="password" placeholder="Enter your password">
  <input type="number" id="age" name="age" min="1" max="120">
  <input type="date" id="dob" name="dob">
</form>
```

Other helpful input attributes:

* `name`, `id`, `value`, `placeholder`, `required`, `disabled`, `readonly`

---

## Labels and Accessibility 🔖

Labels are super important for usability and accessibility. The `<label>` element connects descriptive text to a form control.

```html
<form>
  <label for="username">Username:</label>
  <input type="text" id="username" name="username">
</form>
```

* Use `for="id"` to link label to input for accessibility.

---

## Radio Buttons, Checkboxes, Dropdowns ✅/◯/▼

### Checkboxes & Radio Buttons

```html
<form>
  <input type="checkbox" id="subscribe" name="subscribe" value="yes">
  <label for="subscribe">Subscribe to newsletter</label>

  <input type="radio" id="male" name="gender" value="male">
  <label for="male">Male</label>

  <input type="radio" id="female" name="gender" value="female">
  <label for="female">Female</label>
</form>
```

### Dropdowns

```html
<form>
  <label for="numbers">Choose a favorite number:</label>
  <select name="numbers" id="numbers" size="5" multiple>
    <option value="" disabled selected>Select a number</option>
    <option value="one">1</option>
    <option value="two">2</option>
    <option value="three">3</option>
  </select>
</form>
```

---

## Bringing It All Together: Accessible, Validated, and Well‑Structured Forms

```html
<form action="/submit" method="post">
  <label for="name">Name:</label>
  <input type="text" id="name" name="name" placeholder="Your name" required>

  <label for="email">Email:</label>
  <input type="email" id="email" name="email" placeholder="you@example.com" required>

  <label for="gender">Gender:</label>
  <input type="radio" id="male" name="gender" value="male">
  <label for="male">Male</label>
  <input type="radio" id="female" name="gender" value="female">
  <label for="female">Female</label>

  <label for="subscribe">Subscribe to newsletter:</label>
  <input type="checkbox" id="subscribe" name="subscribe" value="yes">

  <label for="age">Age:</label>
  <input type="number" id="age" name="age" min="0" max="120">

  <label for="bio">Tell us about yourself:</label>
  <textarea id="bio" name="bio" rows="5" cols="30"></textarea>

  <label for="country">Country:</label>
  <select id="country" name="country">
    <option value="" disabled selected>Select your country</option>
    <option value="ghana">Ghana</option>
    <option value="usa">United States</option>
    <option value="uk">United Kingdom</option>
  </select>

  <button type="submit">Submit</button>
</form>
```
