# HNG Stage 1B Task: Testable Profile Card

This project is a responsive, accessible, and highly testable Profile Card created for the HNG Stage 1B Frontend task. It uses semantic HTML, standard CSS, and vanilla JavaScript to render a user profile containing a dynamic timestamp, bio, socials, and lists of hobbies and dislikes.

## Features & Task Fulfillment

This implementation strictly follows all task requirements set forth in the prompt:

### Automated Testing Support (`data-testid`)

Every requested element includes the exact `data-testid` assigned for automated testing:

- **Card Wrapper:** `test-profile-card`
- **Name:** `test-user-name`
- **Bio:** `test-user-bio`
- **Dynamic Time:** `test-user-time`
- **Avatar:** `test-user-avatar`
- **Social Links Wrapper:** `test-user-social-links` (with individual link IDs generated dynamically, e.g., `test-user-social-twitter`)
- **Hobbies List:** `test-user-hobbies`
- **Dislikes List:** `test-user-dislikes`

### Semantic HTML

Modern semantic tags are used to organize content logically:

- `<article>` to enclose the independent card structure.
- `<header>` and heading tags (`<h2>`, `<h3>`) to describe structural sections.
- `<figure>` to wrap the user avatar image.
- `<nav>` for grouping social external links.
- `<section>` for logical breakdowns of the hobbies/dislikes.

### Accessibility (A11y)

- **Screen Reader Announcements:** Added the `aria-live="polite"` attribute to the timestamp element so screen readers gracefully announce time updates.
- **Keyboard Navigation:** Native interactive elements (anchor tags) are fully functional via the `Tab` key and feature distinct focus outlines in CSS.
- **Color Contrast:** The chosen color palette correctly meets WCAG AA standards.
- **Meaningful Images:** The profile avatar includes an `alt` attribute.

### Responsive Layout

Implemented using modern CSS flexbox and media queries:

- **Mobile (`<640px`):** Clean and centralized vertical layout.
- **Desktop/Tablet (`>640px`):** Flexible layout smoothly transitions the picture to the left side and details to the right.

### JavaScript Behavior

- Uses a centralized `profile` object for state, making it highly reusable and scalable.
- Time reflects `Date.now()` and ticks precisely using a robust `setInterval` update of 1000ms.
- Social links natively open in a new tab using secure attributes (`target="_blank" rel="noopener noreferrer"`).

---

## How to Run Locally

Because this project utilizes zero frameworks and vanilla technologies, you can easily test it straight from your local file system.

1. **Clone the Directory:** Download or `git clone` the repository onto your machine.
2. **Open in Browser:** Simply double-click the `index.html` file to open it in your default web browser (Chrome, Firefox, Safari, Edge).
   - _Alternative:_ If using VS Code, you can use the "Live Server" extension for a simulated local dev server.

   or just click this [Live Demo](https://okparahngprofile.netlify.app/)

## File Structure

```text
├── index.html     # Semantic HTML backbone tying the CSS/JS together
├── index.css      # Styling including responsive media queries and focus states
├── index.js       # Profile JSON state and dynamic rendering logic
└── images/        # Folder containing the avatar image (`favour.jfif`)
```
