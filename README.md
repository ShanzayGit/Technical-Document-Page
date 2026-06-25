# HTML Basics — Technical Documentation Page

A responsive technical documentation page covering the fundamentals of HTML, built with plain HTML and CSS.

---

## Project Structure

```
project/
├── index.html       # Main documentation page
└── styles.css       # Stylesheet
```

---

## Sections Covered

1. **Introduction to HTML** — What HTML is, key facts and history
2. **Basic HTML Document Structure** — The standard boilerplate structure
3. **HTML Elements and Tags** — Standard and self-closing elements, attributes
4. **Text and Heading Elements** — Headings h1–h6, paragraphs, links, bold, italic
5. **Lists in HTML** — Unordered, ordered, and definition lists
6. **HTML Forms and Input Elements** — Form inputs, labels, selects, buttons

---

## Features

- Fixed sidebar navbar on desktop (768px and above)
- Smooth scroll navigation via anchor links
- Responsive layout — stacks on mobile, sidebar on desktop
- Syntax-highlighted code blocks using escaped HTML entities
- Styled inline code using `.code` class (orange-red color)
- Justified text for clean readability

---

## How to Run

No build tools or dependencies required. Just open the file in a browser:

```bash
# Option 1 — Open directly
open index.html

# Option 2 — Use a local server (recommended)
npx serve .
# or
python -m http.server 8000
```

Then visit `http://localhost:8000` in your browser.

---

## Responsive Behaviour

| Screen Size | Layout |
|---|---|
| Mobile (< 768px) | Navbar stacks at the top, content below |
| Tablet / Desktop (≥ 768px) | Navbar fixed on the left, content on the right |

---

## CSS Highlights

- `position: fixed` on `#navbar` keeps the sidebar always visible while scrolling
- `padding-top: 70px` on `#navbar` pushes links below the fixed "Basics of HTML" header
- `overflow-x: auto` on `pre` prevents code blocks from breaking the layout on small screens
- `#navbar header` is fixed at the top-left with a matching `width: 250px`
- `#main-doc` has `margin-left: 270px` on desktop to prevent content hiding behind the navbar

---

## Known Gotchas

- HTML code inside `<pre><code>` must be escaped using HTML entities (`&lt;` for `<`, `&gt;` for `>`) — otherwise the browser renders it instead of displaying it as text
- `height` on the global `a` tag can conflict with `.nav-link` styles — keep height only on `.nav-link` inside the media query


---

## Technologies Used

- HTML5
- CSS3 (Flexbox, Media Queries, Position Fixed)
