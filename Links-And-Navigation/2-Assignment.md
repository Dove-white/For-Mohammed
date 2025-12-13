# 📝 HTML Links & Navigation Practical Assignment

**Objective:**
To practice creating internal links, external links, anchor links, and using the `target` attribute in HTML. Students will also implement accessibility best practices.

---

## Task 1: Basic Anchor Tags

**Instructions:**
1. Create a simple HTML page named `index.html`.
2. Add a heading: `Welcome to My Website`.
3. Add a paragraph describing your website.
4. Create a clickable link to `https://example.com` with the text “Visit Example Site”.

**Expected Output:**
- Clicking the link opens the external website.
- Use proper `<a>` syntax.

---

## Task 2: Internal Links

**Instructions:**
1. Create another page named `about.html`.
2. Add a heading: `About Us`.
3. On `index.html`, add a link to `about.html` with the text “Learn More About Us”.

**Expected Output:**
- Clicking the link navigates to `about.html` within the same website.

---

## Task 3: Anchor Links (In-Page Navigation)

**Instructions:**
1. On `index.html`, create 3 sections with headings: `Home`, `Services`, `Contact`.
2. Assign `id` attributes to each section: `home`, `services`, `contact`.
3. Add the style below to each section and change the background color.
```html
<section style="background-color: #f2f2f2; padding: 20rem;">...</section>
```
3. Create a navigation menu at the top of the page linking to each section using anchor links.

**Expected Output:**
- Clicking a menu item scrolls smoothly to the relevant section.

---

## Task 4: External Links & Open in New Tab

**Instructions:**
1. Add a link to an external website (e.g., `https://openai.com`) on `index.html`.
2. Ensure the link opens in a new tab safely.

**Expected Output:**
- Clicking the link opens the website in a new tab without security issues.

---

## Task 5: Accessibility Best Practices

**Instructions:**
1. Make sure all links have descriptive text.
2. Add `aria-label` attributes if needed for clarity.
3. Wrap the navigation menu in a `<nav>` element.

**Expected Output:**
- Navigation is semantic and accessible.
- Screen readers can identify and describe links correctly.

---

## Bonus Challenge

- Add an internal link in `about.html` that takes the user back to a specific section in `index.html`.
- Add an image next to each link with a relevant icon using `<img>`.

---

## Submission Guidelines

- Zip the folder containing your HTML files (`index.html`, `about.html`, etc.).
- Ensure all links work correctly.
- Share your results with your instructor for review.

Happy coding🚀!

