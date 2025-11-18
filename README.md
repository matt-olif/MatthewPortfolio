# MatthewPortfolio

Short portfolio site showcasing education, skills, certificates and projects.

## Contents
- [index.html](index.html)
- [style.css](style.css)
- [script.js](script.js)
- [README.md](README.md)

## Project overview
This is a static portfolio site built with plain HTML, CSS and JavaScript. It includes:
- A fixed navigation with smooth scrolling.
- A hero section with profile image and CTA.
- Education, Certificates, Skills and Projects sections.
- Scroll-based reveal animations using the Intersection Observer API.

## How to run
1. Open [index.html](index.html) in any modern browser (no build step required).
2. Ensure the images referenced in the HTML (e.g., `profilePic.jpeg`, `HTML_CSS_certificate.jpg`) exist in the same folder.

## Key implementation details

Files:
- Main HTML: [index.html](index.html)
- Styles: [style.css](style.css)
- Scripts: [script.js](script.js)

Important code symbols referenced:
- Smooth scroll initialization in [script.js](script.js): the `document.querySelectorAll('a[href^="#"]')` click handler.
- Intersection Observer config: [`observerOptions`](script.js) and the created [`observer`](script.js).
- Animated elements targeted: CSS classes [`.education-card`](style.css), [`.certificate-card`](style.css), [`.skill-item`](style.css), [`.project-card`](style.css) (class usages shown in [index.html](index.html)).

How features work:
- Smooth scrolling: anchor click handlers (in [script.js](script.js)) call element.scrollIntoView({ behavior: 'smooth', block: 'start' }).
- Nav background change on scroll: the `scroll` event listener in [script.js](script.js) toggles `nav.style.background` at `window.scrollY > 100`.
- Reveal animations: [`observerOptions`](script.js) configures the IntersectionObserver; when an element intersects, [`observer`](script.js) sets `opacity` and `transform` to animate items into view. The observed selectors are `.education-card, .certificate-card, .skill-item, .project-card` (defined/used in [style.css](style.css) and [index.html](index.html)).

## Structure (high level)
- Navigation located in `<nav>` inside [index.html](index.html).
- Sections have IDs: `#home`, `#education`, `#certificates`, `#skills`, `#projects`, `#contact` (anchor links in [index.html](index.html)).
- Visual styling and layout in [style.css](style.css).
- Interactivity (scroll, observer) in [script.js](script.js).

## Accessibility & performance notes
- Use semantic headings and alt attributes for images (add `alt` to your `<img>` tags).
- Consider lazy-loading large images (`loading="lazy"`).
- Avoid duplicate class names on elements (e.g., remove duplicate `profile-img` class usage on both wrapper and img element).

## Suggested improvements / TODO
- Replace inline SVG icons with accessible <svg> elements + aria-labels or use icon fonts properly.
- Add alt text to images and `rel="noopener noreferrer"` to external links.
- Add a simple build step only if you plan to use bundlers or preprocessors.
- Add meta description and OG tags for sharing.
- Consider extracting repeated content into components if you migrate to a framework (React/Vite).

## Contact
Author: Matthew Olifant  
Email: matthew.olifant2@icloud.com

License: MIT (or add your preferred license)