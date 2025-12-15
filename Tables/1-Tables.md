## 📊 HTML Tables: Building Blocks

HTML tables are made with a few core tags: `<table>`, `<tr>`, and `<td>`.

* `<table>`: wraps the whole table.
* `<tr>` (table row): defines a row.
* `<td>` (table data): defines a cell in a row.

```html
<table>
  <tr>
    <td>Mood</td>
    <td>Color</td>
    <td>Weather</td>
  </tr>
  <tr>
    <td>Happy</td>
    <td>Yellow</td>
    <td>Sunny</td>
  </tr>
  <tr>
    <td>Sleepy</td>
    <td>Gray</td>
    <td>Cloudy</td>
  </tr>
</table>
```

---

## 🧱 Adding Structure: `<thead>`, `<tbody>`, `<tfoot>`

To make your tables more semantic and accessible, use grouping tags:

* **`<thead>`** — for header rows (usually contains `<th>` cells)
* **`<tbody>`** — for the main part of the table
* **`<tfoot>`** — for footer rows (summaries, notes, attributions)

```html
<table>
  <thead>
    <tr>
      <th>CMS</th>
      <th>Usage</th>
      <th>Change Since Jan 1</th>
      <th>Market Share</th>
      <th>Change Since Jan 1</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>WordPress</td>
      <td>25.8%</td>
      <td>+0.2%</td>
      <td>59.1%</td>
      <td>+0.3%</td>
    </tr>
    <tr>
      <td>Joomla</td>
      <td>2.8%</td>
      <td>No Change</td>
      <td>6.4%</td>
      <td>No Change</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td>Totals</td>
      <td>33.3%</td>
      <td></td>
      <td>76%</td>
      <td></td>
    </tr>
    <tr>
      <td colspan="5">
        * <strong>Usage</strong> is % of surveyed websites using the CMS.  
        <strong>Market Share</strong> is % of CMS-powered sites using that CMS.
      </td>
    </tr>
    <tr>
      <td colspan="5">
        Data from W3Techs (Feb 2016).  
        <a href="http://w3techs.com" target="_blank">w3techs.com</a>
      </td>
    </tr>
  </tfoot>
</table>
```

---

## 🧷 Adding Borders & Spacing

To make your table visually clear, you can style it using CSS:

```css
table {
  border-collapse: collapse; /* ensures borders are not doubled */
  width: 100%;
}

th, td {
  border: 1px solid #ddd;
  padding: 8px;
  text-align: left;
}

thead {
  background-color: #f2f2f2;
}
```

This CSS:

* collapses borders so they look clean,
* adds borders around each cell,
* gives padding for readability,
* styles the header row so it's distinguished.

---

## 📝 Best Practices: When *Not* to Use Tables

While tables are great for structured data, **don’t use them for layout**. Here are some guidelines:

1. **Use tables for tabular data only** — Tables should represent data with a logical grid.
2. **Avoid using tables for page layout** — Use CSS **Flexbox** or **Grid** instead.
3. **Accessibility matters** — Use `<th>`, `<caption>`, `<thead>`, `<tbody>`, and `<tfoot>`.
4. **Keep mobile in mind** — Make wide tables scrollable or reformat for small devices.
