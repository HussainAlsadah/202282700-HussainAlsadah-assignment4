# Technical Documentation

Project: 202282700-HussainAlsadah-assignment2

Date: 2026-03-28

Cloning link: https://github.com/HussainAlsadah/202282700-HussainAlsadah-assignment2.git

Overview
--------
This is the documentation for the portfolio assessment (Assignment 2), which builds on Assignment 1 by adding interactivity, dynamic content, API integration, and improved user experience. The site is a static single-page portfolio built with HTML, CSS, and JavaScript.

Repository Structure
--------------------
assignment-2/
- README.md
- index.html
- css/
    - styles.css
- js/
    - script.js
- assets/
    - images/
        - AI-ProjectPlaceHolder.png
        - computer-stuff.jpg
        - CV-Example.png
        - task-manager-placeholder.png
- docs/
    - ai-usage-report.md
    - technical-documentation.md

Key Files & Responsibilities
----------------------------
- `index.html`
    - Contains the page sections: About (tabbed), Projects, Hobbies, Contact, and Footer.
    - The About section is split into three tabs: About, Skills, and Experience.
    - The Hobbies section includes a Tech Trivia widget that fetches questions from an external API.
    - The Contact form uses `novalidate` and custom JavaScript validation with inline error messages.
    - The `<script>` tag is placed at the bottom of `<body>` to ensure the DOM is fully loaded before the script runs.

- `css/styles.css`
    - Global resets and system font stack.
    - Sectioned styles for header, tabs, skill bars, experience timeline, projects, hobbies, trivia widget, contact form, and footer.
    - Tab styles: `.tab-bar`, `.tab-btn`, `.tab-panel` with a fade-in animation on panel switch.
    - Skill bar styles: `.skill-bar` and `.skill-fill` with a CSS transition for animated fill on tab open.
    - Trivia widget styles: `.trivia-widget`, `.trivia-answer-btn`, correct/wrong state styles, error and loading states.
    - Form validation styles: `.input-error` (red border), `.field-error` (inline error text), `.form-success` (green confirmation).
    - Responsive rules under `@media (max-width: 768px)`; navigation collapses to a dropdown panel.
    - Dark mode styles applied by toggling the `dark-mode` class on `<body>`, covering all new and existing components.

- `js/script.js`
    - Wrapped in `DOMContentLoaded` to ensure DOM nodes exist before attaching listeners.
    - Implements:
        - Smooth scrolling for internal navigation links.
        - Theme toggle (adds/removes `dark-mode` on `<body>`, updates SVG icon, saves preference to `localStorage`).
        - Theme persistence via `localStorage`: saved preference is restored on page load.
        - Mobile nav toggle (adds/removes `.open` on `.nav-links` and manages `aria-expanded`).
        - Tab switching: activates the clicked tab panel, deactivates others, triggers skill bar animation when the Skills tab opens.
        - Skill bar animation: resets bar widths to 0% then animates to their `data-level` value using `requestAnimationFrame`.
        - Tech Trivia: fetches 5 questions at a time from the Open Trivia DB API (category: Science & Computers), renders answer buttons, handles correct/wrong selection with visual feedback, shows a "Next Question" button after answering, refetches when the queue is empty, and displays a friendly error message if the API call fails.
        - Contact form validation: checks name, email (including format via regex), and message fields on submit; shows inline error messages and red borders on invalid fields; shows a green success message and resets the form on valid submission.

Assets
------
- `assets/images/AI-ProjectPlaceHolder.png` — used for the AI Study Assistant project card preview.
- `assets/images/task-manager-placeholder.png` — used for the Task Manager project card preview.
- `assets/images/computer-stuff.jpg` — present in assets but not currently used.
- `assets/images/CV-Example.png` — present in assets but not currently used.

How to Run Locally
-------------------
1. Clone the repository:
   https://github.com/HussainAlsadah/202282700-HussainAlsadah-assignment2.git
2. Open `index.html` in a browser (static site, no server required).
3. An internet connection is required for the Tech Trivia widget to fetch questions from the Open Trivia DB API.
4. Test responsive behavior by resizing the window or using DevTools device emulation.

Testing & Verification
----------------------
- Smooth scrolling: click navigation links to confirm smooth scroll to each section.
- Theme toggle: click the round button at bottom-right to switch dark/light mode; refresh the page to confirm the preference is restored from localStorage.
- Mobile nav: at narrow widths (<=768px), use the hamburger button to open/close the navigation dropdown.
- Tabs: click About, Skills, and Experience tabs in the About section; confirm the Skills tab triggers the animated progress bars.
- Tech Trivia: confirm a question loads on page load, answer buttons highlight correctly/incorrectly on click, the Next Question button advances to the next question, and an error message appears if the API is unreachable.
- Contact form: submit with empty fields to confirm inline error messages appear; submit with an invalid email to confirm format validation; submit a valid form to confirm the success message appears and the form resets.