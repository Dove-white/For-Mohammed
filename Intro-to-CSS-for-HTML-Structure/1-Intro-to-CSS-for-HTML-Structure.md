## Intro to CSS for HTML Structure

CSS (Cascading Style Sheets) lets you control how your HTML structure looks — things like color, font size, and spacing — without touching the HTML itself. Below are the main ways to add CSS and how they differ.

---

## ✏️ Inline CSS

Inline CSS is when you put the style directly on an HTML element using the `style` attribute. This is very specific — it only affects that one tag.

```html
<!DOCTYPE html>
<html>
  <body style="background-color:black;">
    <h1 style="color:white; padding:30px;">My Title</h1>
    <p style="color:white;">A paragraph with inline style.</p>
  </body>
</html>
```

**Pros:**

* Quick to test or apply a single style.
* No separate CSS file is needed.

**Cons:**

* Gets messy if used everywhere.
* Harder to maintain for larger sites.

---

## 🧩 Internal Styles (Embedded CSS)

Internal CSS lives inside a `<style>` tag in the `<head>` section of your HTML.

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      body {
        background-color: blue;
      }
      h1 {
        color: red;
        padding: 60px;
      }
    </style>
  </head>
  <body>
    <h1>My Heading</h1>
    <p>This is a paragraph.</p>
  </body>
</html>
```

You can use **basic selectors** here like:

* **Element selector** (`body`, `h1`)
* **Class selector** (`.my-class { … }`)
* **ID selector** (`#my-id { … }`)

**Pros:**

* Good for styling a single HTML page.
* You still get the power of selectors (class, ID).

**Cons:**

* If every page has its own styles embedded, it's a pain to update.
* Increases HTML file size, which may slow down page load.

---

## 📁 External CSS

External CSS lives in its own `.css` file, which you link to from your HTML.

1. Create a file named `style.css` (or any name).
2. Add CSS rules there, e.g.:

```css
.left-col {
  float: left;
  width: 33%;
  background: #809900;
}
.middle-col {
  float: left;
  width: 34%;
  background: #eff2df;
}
```

3. In your HTML `<head>`, include:

```html
<link rel="stylesheet" type="text/css" href="style.css" />
```

**Pros:**

* Keeps your HTML clean and small.
* You can reuse the same CSS file on many pages.

**Cons:**

* The page might render weirdly until the CSS file finishes loading.
* More HTTP requests (if you have many CSS files).

---

## 🎨 Adding Color, Font Size & Spacing

Once you know how to include CSS (inline, internal, or external) and how to use selectors, you can start styling:

* **Color**: `color`, `background-color`
* **Font size**: `font-size`
* **Spacing**: `margin`, `padding`

**Example in CSS:**

```css
body {
  background-color: #f5f5f5;
}
h1 {
  color: #333333;
  font-size: 32px;
  margin-bottom: 20px;
}
p {
  color: #666666;
  font-size: 18px;
  line-height: 1.5;
  padding: 10px;
}
```

---

## 💡 Basic Selectors

* **Element selector**: Targets HTML tags directly.

```css
p { … }
```

* **Class selector**: Targets any element with a class.

```css
.highlight { … }
```

* **ID selector**: Targets a single, unique element.

```css
#main-header { … }
```

These let you apply different styles to different parts of your HTML.

---

## 🌐 Why External CSS Matters

Using external CSS is often the best choice for real-world projects because:

* **Reusability**: One CSS file can style many pages.
* **Maintainability**: You make changes in one place, and they apply everywhere.
* **Clean structure**: HTML stays focused on structure, CSS stays focused on design.

---

## 📚 Summary

* **Inline CSS**: Fast for single elements, but messy for lots of styling.
* **Internal Styles**: Good for single-page styles with selectors.
* **External CSS**: Best for scalable, maintainable style across a site.
* Use **element**, **class**, and **ID** selectors to target HTML.
* Control appearance using color, font, and spacing.
* External CSS matters for maintainability, performance, and site-wide consistency.
