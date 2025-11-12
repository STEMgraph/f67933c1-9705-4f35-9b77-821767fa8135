<!---
{
  "id": "f67933c1-9705-4f35-9b77-821767fa8135",
  "teaches": "Using Character Entities in HTML",
  "depends_on": ["3ee0acd9-0f99-4423-b4f3-a0ca84a16422"],
  "author": "Stephan Bökelmann",
  "first_used": "2025-04-13",
  "keywords": ["HTML", "character entities", "vim", "special characters", "escaping"]
}
--->

# Using Character Entities in HTML

> In this exercise you will learn how to use HTML character entities to display special symbols that cannot be typed directly or would otherwise be interpreted as HTML code. Furthermore we will explore how escaping characters is essential for writing clean, readable, and accurate HTML content.

### Introduction

In HTML, certain characters are reserved for specific syntactic purposes. For example, the less-than sign `<` is used to open tags, and the ampersand `&` begins character references. If you try to write these directly in an HTML document, the browser may interpret them as part of the code rather than as literal text.

To solve this problem, HTML provides *character entities*—special sequences that begin with `&` and end with `;`—to safely represent these symbols in text. For example, `&lt;` renders `<`, `&gt;` renders `>`, and `&amp;` renders `&`.

Character entities also allow you to insert special symbols like `©`, `€`, and `✓` that might not be available directly on your keyboard. This capability is crucial when writing content that includes legal symbols, non-ASCII text, or code snippets.

Mastering the use of character entities improves the quality of your HTML and ensures consistent rendering across browsers and devices.

### Further Readings and Other Sources

- [MDN Web Docs: HTML character references](https://developer.mozilla.org/en-US/docs/Glossary/Entity)
- [W3Schools: HTML Entities](https://www.w3schools.com/html/html_entities.asp)
- [HTML Entity List](https://dev.w3.org/html5/html-author/charref)

---

## Tasks

### Task 1: Create an HTML File with Text That Uses Special Characters

This task shows what happens when special characters are not escaped properly.

1. Open a new HTML file:
   ```sh
   vim entities_demo.html
   ```

2. Start with this basic structure:
   ```html
   <!DOCTYPE html>
   <html>
   <head>
       <title>HTML Entities Demo</title>
   </head>
   <body>
       <p>This is 5 < 10 and 10 > 5.</p>
       <p>Use & in HTML & programming.</p>
   </body>
   </html>
   ```

3. Save and open the file in your browser. You'll likely see issues with how the symbols display.

### Task 2: Fix the Text Using Character Entities

Now you’ll replace problematic characters with their correct HTML entities.

1. Reopen the file in vim:
   ```sh
   vim entities_demo.html
   ```

2. Modify the `<body>` content like so:
   ```html
   <body>
       <p>This is 5 &lt; 10 and 10 &gt; 5.</p>
       <p>Use &amp; in HTML &amp; programming.</p>
   </body>
   ```

3. Save and reload the page. You should now see the characters rendered correctly.

### Task 3: Add Special Symbols Using Named Entities

In this task, you will add a few common symbols using named character entities.

1. Still in the same file, add the following lines below your paragraphs:
   ```html
   <p>Copyright &copy; 2025</p>
   <p>Price: 50 &euro;</p>
   <p>Success: &#10004;</p>
   ```

2. Save and open the file in your browser again.

You should see the © symbol, the euro sign, and a checkmark.

---

## Questions

1. Why do `<` and `&` cause problems when written directly in HTML?
2. What is the difference between a named character entity (e.g., `&copy;`) and a numeric one (e.g., `&#169;`)?
3. Find and add one more character entity to your page. What does it represent?
4. What would happen if you wrote `&copy` (without the semicolon)?
5. Why are character entities important for accessibility and internationalization?

---

## Advice

Character entities are essential tools for anyone writing HTML. They allow you to safely include code-like content and symbols that otherwise wouldn’t be possible to display properly. Whenever you see weird rendering in your HTML output, especially involving `<`, `>`, or `&`, your first move should be to check whether an entity is needed. Keep a reference list handy, and over time, you’ll remember the most common ones like `&lt;`, `&gt;`, and `&amp;` by heart. Practice using both named and numeric forms—they’re both useful, especially when dealing with unique or Unicode-specific characters.
