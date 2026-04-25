# Technical Documentation

Project: 202282700-HussainAlsadah-assignment4

Date: 2026-04-25

Repository: https://github.com/HussainAlsadah/202282700-HussainAlsadah-assignment4.git

## Overview

This document describes the final personal portfolio web application submitted for Assignment 4. The project continues the earlier portfolio work and refines it into a more polished final product with improved layout, stronger presentation, interactive features, and clearer documentation.

The website is a static single-page application built with:

- HTML for structure
- CSS for styling, layout, responsiveness, and dark mode
- JavaScript for interactivity, validation, state persistence, and API integration

## Repository Structure

```text
202282700-HussainAlsadah-assignment4/
├── README.md
├── index.html
├── css/
│   └── styles.css
├── js/
│   └── script.js
├── assets/
│   └── images/
├── docs/
│   ├── ai-usage-report.md
│   └── technical-documentation.md
├── presentation/
│   ├── slides.pdf
│   ├── demo-video.mp4
│   └── .gitkeep
└── .gitignore
```

## Page Structure

The page is organized into the following sections:

1. Header and navigation
2. Welcome banner
3. Visitor timer bar
4. Hero section
5. About section
6. Projects section
7. Hobbies section
8. Interactive section
9. Contact section
10. Footer
11. Login modal

## Key Files and Responsibilities

### `index.html`

Contains the full structure of the portfolio page.

Important parts:

- Sticky navigation with desktop and mobile support
- Personalized login area in the navbar
- Hero section with portfolio introduction and highlight cards
- Tabbed About section with About, Skills, and Experience panels
- Projects section with filter controls, sort control, and spotlight button
- Hobbies section with personal interest cards
- Interactive section with trivia and quote widgets
- Contact form with custom validation feedback
- Login modal for session personalization

### `css/styles.css`

Contains all visual styling for the website.

Important responsibilities:

- Global reset and base typography
- Hero section layout and card styling
- Responsive layouts for mobile screens
- Navigation, modal, and form styling
- Project card styles, tags, and spotlight highlight state
- Dark mode styles for all major sections
- Visual consistency across content cards and widgets

### `js/script.js`

Contains all client-side interactive behavior.

Important responsibilities:

- Smooth scrolling for internal links
- Dark mode toggle and saved preference using `localStorage`
- Mobile menu open/close logic
- Visitor timer update logic
- Login/logout behavior with saved session
- Live avatar preview in the login modal
- Tab switching for the About section
- Skill bar animation
- Project filtering and sorting
- Project spotlight logic
- Trivia API integration
- Quote API integration with fallback quotes
- Contact form validation and success handling

## Implemented Features

### 1. Responsive navigation

- Sticky navigation bar
- Mobile hamburger menu
- Smooth scrolling between page sections

### 2. Theme system

- Light and dark themes
- Theme preference is saved in `localStorage`

### 3. Personalized visit flow

- Login modal accepts a visitor name
- Navbar updates with initials and display name
- Welcome banner appears after login
- Session persists after refresh using `localStorage`

### 4. About section interactions

- Tabbed content panels
- Skills tab includes animated progress bars

### 5. Project browsing tools

- Filter projects by category
- Sort projects by name or date
- Highlight a random project with the spotlight button
- Allow clicking a project card to apply the same highlight effect
- Prevent the spotlight button from choosing the same project twice in a row when more than one choice is available

### 6. Interactive widgets

- Tech trivia uses Open Trivia DB
- Quote widget uses Quotable API
- Quote widget falls back to local quote data if the API is unavailable
- Trivia widget shows a visible error message if loading fails

### 7. Contact form validation

- Required field checking
- Email format validation
- Inline error messages
- Success message after valid submission

## Data and State Management

This project uses browser-side state only. No backend or database is used.

Saved data in `localStorage`:

- selected theme
- saved visitor name

Temporary runtime state includes:

- current project filter
- current project sort option
- last spotlighted project
- trivia queue and answer state
- timer count

## Assets

Current image assets in use:

- `assets/images/AI-ProjectPlaceHolder.png`
- `assets/images/task-manager-placeholder.png`
- `assets/images/computer-stuff.jpg`

These images are used as previews inside the Projects section.

## How to Run Locally

1. Clone the repository:
   `https://github.com/HussainAlsadah/202282700-HussainAlsadah-assignment4.git`
2. Open `index.html` in a browser.
3. Test desktop and mobile layouts using browser resizing or device emulation.
4. Keep internet enabled if you want live trivia and quote API responses.

## Testing and Verification Checklist

- Check all navbar links
- Test mobile menu open and close behavior
- Test dark mode toggle and refresh persistence
- Test login, logout, and refresh persistence
- Test tab switching in the About section
- Test skill bar animation
- Test project filtering and sorting
- Test project spotlight button multiple times
- Test clicking project cards to trigger spotlight
- Test trivia loading and answer flow
- Test quote refresh behavior
- Test contact form validation and success state
- Test layout in both desktop and mobile widths

## Known Remaining Submission Tasks

The project code is ready for final submission polish, but the following submission items still depend on final preparation outside this document:

- live deployment link
- presentation slides
- presentation video
