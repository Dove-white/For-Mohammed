## 🌐 Global Attributes in HTML

Global attributes are special attributes that *every* HTML element can use — even if they don’t always have a visible effect. They help control behavior, styling, and data for elements.

Here we'll focus on:

* **id**, **class**
* **title**, **style**
* **data-***

---

## id & class

### 🆔 **id**

* The `id` attribute gives an element a **unique identifier** in the document.
* Useful for linking (e.g., `href="#my-section"`), styling via CSS (`#my-section { … }`), or selecting via JavaScript (`document.getElementById("my-section")`).

**Example:**

```html
<div id="header">Welcome to My Site</div>
```

---

### 📂 **class**

* The `class` attribute lets you assign **one or more classes** (space-separated) to an element.
* Classes are super useful for applying CSS styles, grouping similar elements, or selecting them in JS.

**Example:**

```html
<button class="btn primary">Click Me</button>
<p class="text small muted">Some subtitle</p>
```

---

## title & style

### 💬 **title**

* The `title` attribute provides **advisory information**, typically shown as a tooltip when you hover over the element.
* Good for giving extra context without cluttering the UI.

**Example:**

```html
<span title="This is a tooltip!">Hover over me</span>
```

---

### 🎨 **style**

* The `style` attribute allows you to apply **inline CSS** directly on the element.
* Useful for quick tests or very specific overrides — but generally, it's better to use an external stylesheet for maintainability.

**Example:**

```html
<div style="background-color: lightblue; padding: 10px;">
  This box has an inline style.
</div>
```

---

## Data Attributes (`data-*`)

### 🔖 **data-***

* Data attributes let you store **custom data** on any HTML element.
* They follow the format: `data-xyz="someValue"`.
* In JavaScript, you can easily read them via the `dataset` property: `element.dataset.xyz`.

**Example:**

```html
<div data-user-id="12345" data-role="admin">Admin Panel</div>

<script>
  const panel = document.querySelector('[data-user-id]');
  console.log(panel.dataset.userId); // "12345"
  console.log(panel.dataset.role);   // "admin"
</script>
```

---

## Why These Attributes Are Important

* **id** + **class**: Essential for styling, selecting, and organizing your HTML.
* **title**: Gives helpful hints / tooltips without affecting layout.
* **style**: Quick inline styling when needed.
* **data-***: A flexible way to attach **metadata** to elements, without messing with HTML semantics.

