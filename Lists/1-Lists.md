# 📋 Lists in HTML

Lists help organize information clearly on web pages. In HTML, you mainly use three kinds:

- **Unordered lists**  
- **Ordered lists**  
- **Nested lists**

---

## 🔘 Unordered Lists

Unordered lists are used when the order of items doesn’t matter. They use bullet points (or other symbols).

**HTML structure:**

```html
<ul>
  <li>Vegetables</li>
  <li>Eggs</li>
  <li>Bread</li>
</ul>
```

**Rendered output:**

- Vegetables  
- Eggs  
- Bread  

You can also change the bullet style using the `type` attribute:

```html
<ul type="square">
  <li>Milk</li>
  <li>Coffee</li>
</ul>
```

---

## 🔢 Ordered Lists

Ordered lists are for when sequence matters: steps, rankings, or anything with a specific order.

**HTML structure:**

```html
<ol>
  <li>C</li>
  <li>C++</li>
  <li>Java</li>
  <li>JavaScript</li>
  <li>Python</li>
</ol>
```

**Rendered output:**

1. C  
2. C++  
3. Java  
4. JavaScript  
5. Python  

You can customize how the list is numbered using the `type` attribute (`"1"`, `"A"`, `"a"`, `"I"`, `"i"`):

```html
<ol type="A">
  <li>Item 1</li>
  <li>Item 2</li>
</ol>
```

---

## 📂 Nested Lists (Lists Inside Lists)

Nested lists let you group related items under a category. You can mix ordered and unordered lists to represent relationships or subcategories.

**HTML structure example:**

```html
<ol>
  <li>Languages</li>
  <li>Web Development
    <ul>
      <li>HTML</li>
      <li>CSS</li>
      <li>JavaScript</li>
    </ul>
  </li>
  <li>Tools</li>
</ol>
```

**Rendered output idea:**

1. Languages  
2. Web Development  
   - HTML  
   - CSS  
   - JavaScript  
3. Tools  

💡 **Best practice:** Always nest `<ul>` or `<ol>` inside a `<li>` to keep the HTML valid.

---

## 🧭 When to Use Each Type

- Use **ordered lists** when the order is important (e.g., steps in a tutorial, a ranked list).  
- Use **unordered lists** when the order doesn’t matter (e.g., features, shopping items).  
- Use **nested lists** when you need to group items under broader categories (e.g., subtopics).

---

## ✅ Summary

Lists are a simple but powerful way to present content:

- `<ul>` → unordered (bullets)  
- `<ol>` → ordered (numbers or letters)  
- Combine them → **nested lists**  

By using lists properly, your content becomes more structured, readable, and user‑friendly.


