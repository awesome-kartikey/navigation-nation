# Awesome Kartikey Navigation Nation

A simple, elegant, and animated full-screen navigation menu component built with HTML, CSS, and vanilla JavaScript.

## Description

This project provides a visually appealing, animated navigation experience. When the user clicks the hamburger menu icon, a full-screen overlay slides in from the left, revealing navigation links that animate sequentially. Clicking a link or the menu icon again closes the overlay with reverse animations. The project serves as a demonstration of CSS animations, transitions, and basic JavaScript DOM manipulation for interactive UI elements.

## Features

- **Hamburger Menu Toggle:** Classic three-bar icon that animates into an 'X' when active.
- **Full-Screen Overlay:** Provides an immersive navigation experience.
- **Smooth Animations:** Uses CSS transitions for the overlay and keyframe animations for the navigation items, creating a slick slide-in/slide-out effect.
- **Staggered Link Animation:** Navigation links animate sequentially for a dynamic feel.
- **Section-Based Layout:** Includes distinct colored sections corresponding to menu items (for demo purposes).
- **Responsive:** Basic responsiveness included for smaller screens.
- **Vanilla Stack:** Built purely with HTML, CSS, and JavaScript - no external libraries or frameworks needed.

## Tech Stack

- **HTML5:** Semantic structure for the navigation and content sections.
- **CSS3:**
  - Flexbox for layout.
  - CSS Custom Properties (Variables) for easy theming.
  - Transitions for smooth overlay movement.
  - Keyframe Animations for staggered link effects and menu bar transformation.
  - Media Queries for basic responsiveness.
- **JavaScript (ES6):**
  - DOM Manipulation to select elements.
  - Event Listeners to handle clicks.
  - Class Toggling to trigger CSS animations and state changes.

## Setup Instructions

No complex setup is required. Simply clone or download the repository and open the `index.html` file in your web browser.

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/awesome-kartikey/navigation-nation.git
    ```
2.  **Navigate to the directory:**
    ```bash
    cd navigation-nation
    ```
3.  **Open the HTML file:**
    Open `index.html` directly in your preferred web browser (e.g., Chrome, Firefox, Safari).

## Usage

This component is designed as a standalone demonstration but can be adapted for use in other projects.

1.  **Integrate HTML:** Copy the `overlay` div and the `menu-bars` div into your project's HTML structure.
2.  **Link CSS:** Include the `style.css` file or copy its contents into your project's stylesheet. Adjust CSS variables (`:root` section) and styles as needed to match your design.
3.  **Link JavaScript:** Include the `script.js` file or integrate its logic into your project's JavaScript codebase. Ensure the element IDs match those in your HTML.
4.  **Customize Links:** Modify the `<a>` tags within the `<nav>` element in `index.html` to point to your desired pages or sections. Update the corresponding IDs (`nav-1`, `nav-2`, etc.) if necessary and ensure the JavaScript `navItems` array is updated accordingly.
