# 🧾 Joola Invoice PDF Integration Guide

This guide explains how to properly implement header and footer templates for the Joola invoice using your backend PDF rendering library.

---

## 🧑‍💻 Backend Developer Instructions

### ✅ Header, Template

- Use your PDF library’s **`headerTemplate, footer`** feature.
- **Important:** Remove any duplicated header content from the `<body>` of the HTML.

> 🔍 Search for:  
> `<!-- header start -->`  
> This marks the beginning of the header section that should be used as the template.

---

## 🧾 Footer Template

Use the following HTML structure as the footer in your PDF rendering setup:

```html
<table class="layout-table" style="width: 100%;">
  <tr>
    <td style="width: 70%;">
      <p style="margin: 0; font-size: 11px; font-weight: bold;">
        DISCLAIMER
      </p>
      <p style="margin: 5px 0 0 0; font-size: 10px; line-height: 1.3;">
        Anything contained in this document would not lead to any legal claim on the part of any individual for any purpose.
      </p>
    </td>
    <!-- Footer page number -->
    <td style="text-align: right; font-size: 10px;">
      1 of 2
    </td>
  </tr>
</table>