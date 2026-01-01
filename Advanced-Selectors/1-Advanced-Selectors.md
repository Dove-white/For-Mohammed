# ⚡ Advanced CSS Selectors: A Complete Guide

CSS selectors let you target elements in your HTML for styling. Advanced selectors go beyond simple tag, class, or ID selectors, giving you fine-grained control over your web page’s appearance.

---

## 🔍 Attribute Selectors

Attribute selectors target elements based on their **attributes** or **attribute values**. They are especially useful when you want to style elements dynamically without adding extra classes or IDs.

### Types of Attribute Selectors

| Selector           | Meaning                          | Example                                                                    |                               |                                |
| ------------------ | -------------------------------- | -------------------------------------------------------------------------- | ----------------------------- | ------------------------------ |
| `[attr]`           | Element has the attribute        | `<input required>` → `[required] { border: 2px solid red; }`               |                               |                                |
| `[attr="value"]`   | Exact value match                | `<input type="text">` → `[type="text"] { background: lightyellow; }`       |                               |                                |
| `[attr~="value"]`  | One word in space-separated list | `<div class="card active">` → `[class~="active"] { border-color: green; }` |                               |                                |
| `[attr             | ="value"]`                       | Exact or hyphen-separated match                                            | `<div lang="en-US">` → `[lang | ="en"] { font-weight: bold; }` |
| `[attr^="value"]`  | Starts with                      | `<a href="#top">` → `[href^="#"] { color: blue; }`                         |                               |                                |
| `[attr$="value"]`  | Ends with                        | `<a href="file.pdf">` → `[href$=".pdf"] { color: red; }`                   |                               |                                |
| `[attr*="value"]`  | Contains substring               | `<a href="example.com">` → `[href*="example"] { background: yellow; }`     |                               |                                |
| `[attr="value" i]` | Case-insensitive match           | `<a href="EXAMPLE.com">` → `[href="example.com" i] { color: orange; }`     |                               |                                |

#### Code Example

```html
<a href="#section1">Go to Section 1</a>
<a href="https://example.com">Visit Example</a>
```

```css
/* Links starting with # */
a[href^="#"] { color: blue; }

/* Links containing "example" */
a[href*="example"] { color: green; }
```

---

## 🌐 Universal Selector (`*`)

The universal selector `*` targets **all elements** on the page. It’s often used for:

* Resetting styles
* Applying general properties to every element

```css
/* Reset margins and paddings */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```

---

## 👶 Child, Descendant & Sibling Selectors

These selectors define **relationships between elements**, making your styling more precise.

### 1. Child Selector (`>`)

Selects **direct children** of an element.

```html
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
</ul>
```

```css
ul > li {
  color: blue;
}
```

*Only the `li` elements directly inside `ul` are selected.*

---

### 2. Descendant Selector (space)

Selects **any element inside another element**, no matter how deep.

```html
<div class="container">
  <p>Paragraph</p>
  <span><strong>Text</strong></span>
</div>
```

```css
.container p {
  color: red;
}
```

*All `<p>` elements inside `.container` are selected.*

---

### 3. Adjacent Sibling Selector (`+`)

Selects the **next element** immediately following another element.

```html
<h2>Heading</h2>
<p>Paragraph 1</p>
<p>Paragraph 2</p>
```

```css
h2 + p {
  font-weight: bold;
}
```

*Only the first `<p>` after `<h2>` is bold.*

---

### 4. General Sibling Selector (`~`)

Selects **all siblings** after an element.

```css
h2 ~ p {
  color: green;
}
```

*All `<p>` elements after `<h2>` are green.*

---

## 🧩 Combining Selectors

You can mix attribute selectors with child, descendant, sibling, or universal selectors:

```css
/* All links inside divs that have a data-active attribute */
div[data-active] a {
  text-decoration: underline;
}

/* First list item in every list */
ul > li:first-child {
  font-weight: bold;
}
```

---

## ✅ Summary

* **Attribute selectors**: Target elements by attributes and values
* **Universal selector `*`**: Apply styles to every element
* **Child `>`**: Select direct children
* **Descendant (space)**: Select nested elements at any depth
* **Adjacent sibling `+`**: Select next element only
* **General sibling `~`**: Select all following siblings