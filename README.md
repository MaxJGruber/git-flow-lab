# Theme Toggle (Light/Dark Mode)

This project demonstrates how to toggle between **light** and **dark** themes using a `data-theme` attribute on the `<body>` element. The toggle is handled in JavaScript, while styles are applied conditionally in CSS.

---

## How it works

1. **HTML**
   Add a button to trigger theme changes:

   ```html
   <button id="theme-toggle">Toggle Theme</button>
   ```

2. **JavaScript (`script.js`)**

   * Listens for clicks on the toggle button.
   * Reads the current `data-theme` value on `<body>`.
   * Switches between `"light"` and `"dark"`.

   ```javascript
   document.addEventListener("DOMContentLoaded", () => {
     const body = document.body;
     const toggleBtn = document.getElementById("theme-toggle");

     toggleBtn.addEventListener("click", () => {
       const currentTheme = body.getAttribute("data-theme");
       const newTheme = currentTheme === "dark" ? "light" : "dark";
       body.setAttribute("data-theme", newTheme);
     });
   });
   ```

3. **CSS (`styles.css`)**

   * Default (light theme) styles are applied to `body`.
   * Dark mode styles are applied when `body` has `data-theme="dark"`.
   * Smooth transitions improve user experience.

   ```css
   /* Default light theme */
   body {
     background-color: #ffffff;
     color: #000000;
     transition: background-color 0.3s, color 0.3s;
   }

   /* Dark theme */
   body[data-theme="dark"] {
     background-color: #121212;
     color: #ffffff;
   }
   ```

---

## Usage

1. Open `index.html` in a browser.
2. Click the **Toggle Theme** button to switch between light and dark modes.

---
