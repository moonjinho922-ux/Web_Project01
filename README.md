# T&J Recipe Studio

T&J Recipe Studio is a simple recipe website made with HTML and CSS.
This project helps users look at recipes, see cooking steps, and move between pages easily.

## Features
- Home page
- Recipes page
- Recipe detail pages
- About page
- Hover effects and animations
- Light and dark mode
- Responsive layout

## File Structure
- `index.html` - home page
- `recipes.html` - recipes list page
- `about.html` - about page
- `sandwich.html` - egg sandwich page
- `spaghetti.html` - spaghetti page
- `pasta.html` - chicken alfredo pasta page
- `mac.html` - mac and cheese page
- `style.css` - CSS file for all pages
- `assets/` - images for the project

## Implementation Decisions
- We used separate HTML files for each page to keep the project simple and organized.
- We used one CSS file for all pages so the design stays consistent.
- We added hover effects and animations to make the website look more interactive.
- We used basic HTML tags like header, nav, main, section, and footer to organize the pages.
- We tried to make the layout easy to read on different screen sizes.

## Note
We received some AI assistance when working on the light/dark mode feature.
The final code was reviewed, edited, and used in our project by our team.

## Dark Mode Toggle
- The dark mode works using just a hidden checkbox and some CSS selectors.
- In the HTML there is only one line for it, a checkbox with the id dark-toggle. It has to be placed before the header, main, and footer in the HTML file. This part is important because the CSS trick only works if the checkbox is a sibling to those elements.
- The checkbox itself is hidden using display: none, so users don’t actually see it. Instead, they click on a label (like a button or icon) that is connected to it with for="dark-toggle". When the label is clicked, it checks or unchecks the box even though the box is hidden.
- To switch icons or text, elements with the class .light-mode start visible and .dark-mode start hidden. When the checkbox gets checked, they switch. This lets the page show different icons or text for light mode and dark mode without using JavaScript.
- The main idea uses the ~ CSS sibling selector. Something like #dark-toggle:checked ~ header means when the checkbox is checked, the header that comes after it will get new styles. That is how the background colors, text colors, and borders on the page change.
- One small issue is the <body> element. The checkbox is inside the body, so it cannot be a sibling of it. Because of that, ~ does not work there. Instead we use body:has(#dark-toggle:checked) which means if the body contains a checked dark-toggle, then apply these styles.
- For deeper elements like cards, nav links, or buttons, we use ~ *. The * means any descendant inside the siblings. This lets the dark mode styles reach elements that are further inside the page structure.

## Team Members
- Trinh Bui
- Jinho Moon