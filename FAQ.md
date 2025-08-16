# Frequently Asked Questions (FAQ)

This document answers common questions about the Awesome Kartikey Navigation Nation project.

**Q1: What is the main purpose of this project?**

A1: This project demonstrates how to create a modern, animated, full-screen navigation menu using only HTML, CSS, and vanilla JavaScript. It showcases CSS transitions, keyframe animations, and basic JavaScript DOM manipulation for interactive UI development.

**Q2: How do I run this project locally?**

A2: It's very simple:

1.  Clone or download the repository.
2.  Navigate to the project folder in your file explorer or terminal.
3.  Double-click the `index.html` file, or open it using your web browser. No web server or build tools are needed.

**Q3: Can I customize the appearance (colors, fonts)?**

A3: Yes! The project uses CSS custom properties (variables) for easy theming. You can modify the color variables defined in the `:root` section of `style.css` (e.g., `--primaryColor`, `--navColor1`, etc.). The font 'Nunito' is imported from Google Fonts at the top of `style.css`; you can change this import and the `font-family` property in the `body` style rule.

**Q4: How does the slide-in/slide-out animation work?**

A4: The animation is primarily handled by CSS:

- The **overlay** uses CSS `transition` properties. When the `overlay-active` class is added/removed by JavaScript, the `transform: translateX()` property changes, and the transition smoothly animates the overlay sliding in or out.
- The **navigation links** use CSS `keyframes` (`@keyframes slide-in`, `@keyframes slide-out`). JavaScript adds/removes classes like `slide-in-1`, `slide-out-1`, etc., to each link (`<li>`). These classes apply the keyframe animations with staggered `animation-delay` values, creating the sequential effect.

**Q5: Is the navigation menu responsive?**

A5: Basic responsiveness is included via a media query (`@media (max-width: 600px)`) at the end of `style.css`. This query adjusts the positioning of the menu bars and the home link for smaller screens (typically large smartphones in portrait mode). Further enhancements could be added for different screen sizes if needed.

**Q6: How can I add or remove navigation menu items?**

A6: To modify the menu items:

1.  **HTML (`index.html`):** Add or remove `<li>` elements within the `<nav><ul>` structure. Make sure each `<li>` has a unique ID (e.g., `nav-6`) and includes an `<a>` tag for the link.
2.  **CSS (`style.css`):**
    - Define background colors for new items if desired (e.g., `nav li:nth-of-type(6)`).
    - Add corresponding animation classes for new items (e.g., `.slide-in-6`, `.slide-out-6`) with appropriate `animation-delay` values. Create the necessary keyframes if not already covered.
3.  **JavaScript (`script.js`):**
    - Add the new element's ID to the `navItems` array (e.g., `const nav6 = document.getElementById('nav-6');` and add `nav6` to the array).
    - The `navAnimation` function iterates through `navItems` using their index (`i`). Ensure your CSS classes (`slide-in-${i + 1}`) match this pattern. If you add more items, this function should automatically handle them as long as the CSS classes follow the `slide-*-N` pattern numerically.

**Q7: What are the dependencies for this project?**

A7: There are no external JavaScript library dependencies. It relies solely on modern web browser capabilities for HTML5, CSS3, and ECMAScript 6 (JavaScript). It does use Google Fonts for the 'Nunito' font, which requires an internet connection to load initially.

**Q8: Why does clicking a navigation link close the menu?**

A8: The JavaScript code adds an event listener to _each_ navigation item (`navItems.forEach(...)`). When any of these items are clicked, the `toggleNav` function is called, which handles closing the overlay and animating the elements out. This is common usability practice for overlay menus.
