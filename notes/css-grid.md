CSS Grid is a powerful layout system in CSS that allows you to create responsive, grid-based designs. Let’s explore CSS Grid step-by-step with examples and explanations.

---

### **What is CSS Grid?**
CSS Grid is a two-dimensional system that allows you to arrange elements in rows and columns. It makes creating complex layouts easier compared to older methods like floats or flexbox (which is one-dimensional).

---

### **Basic Grid Structure**

Here’s a simple example:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CSS Grid Example</title>
  <style>
    .grid-container {
      display: grid;
      grid-template-columns: 100px 100px 100px;
      grid-template-rows: 100px 100px;
      gap: 10px;
      background-color: #f0f0f0;
      padding: 10px;
    }

    .grid-item {
      background-color: #4CAF50;
      color: white;
      text-align: center;
      line-height: 100px;
      font-size: 20px;
    }
  </style>
</head>
<body>
  <div class="grid-container">
    <div class="grid-item">1</div>
    <div class="grid-item">2</div>
    <div class="grid-item">3</div>
    <div class="grid-item">4</div>
    <div class="grid-item">5</div>
    <div class="grid-item">6</div>
  </div>
</body>
</html>
```

---

### **Explanation**

1. **`display: grid;`**  
   This turns the `.grid-container` into a grid layout.

2. **`grid-template-columns: 100px 100px 100px;`**  
   Defines three columns, each 100 pixels wide.

3. **`grid-template-rows: 100px 100px;`**  
   Defines two rows, each 100 pixels tall.

4. **`gap: 10px;`**  
   Adds 10px of space between the grid items.

---

### **Making the Grid Responsive**

Instead of fixed sizes, you can use fractions (`fr`) and other responsive units like percentages:

```css
.grid-container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 10px;
}
```

- **`repeat(3, 1fr);`** means three columns, each taking up an equal fraction of the available space.

---

### **Positioning Items in the Grid**

You can control where each item appears using `grid-column` and `grid-row`:

```css
.grid-item:first-child {
  grid-column: 1 / 3; /* Spans from column 1 to 3 */
  grid-row: 1 / 3;    /* Spans from row 1 to 3 */
}
```

---