# Copilot Instructions - alexpaar.github.io

## Project Overview

This is a personal GitHub Pages portfolio website showcasing Alexander Paar's professional and academic background. It's a single-page application with embedded styling and social media links.

**Stack:** Pure HTML5 + CSS (no build tools, no frameworks)
**Deployment:** GitHub Pages (branch: main)

## Project Structure

- **`index.html`** - Single-page entry point containing all HTML, CSS, and structure
- **`images/alexpaar.jpg`** - Background image displayed full-screen behind the content
- **`README.md`** - Project description (minimal)

## Key Patterns & Conventions

### HTML/CSS Architecture

- **Single-page design:** All styling embedded in `<style>` tag within `<head>`. No external CSS files.
- **Semantic layout:** Uses CSS Flexbox for responsive layout. Three main content containers:
  - `.container` - Centered wrapper with semi-transparent dark backdrop and blur effect
  - `.text-container` - Wraps the biographical card
  - `.text-card` - White text content with semi-transparent background

### Responsive Design

- Mobile-first approach with breakpoint at `768px` (see `@media` rule at end of style block)
- On mobile: reduced font sizes, smaller social buttons (45px vs 50px), adjusted padding
- Uses `width: 90vw` for viewport-relative sizing instead of fixed pixels

### Visual Design Patterns

- **Semi-transparent overlays:** Uses `rgba(0, 0, 0, 0.4)` and `rgba(255, 255, 255, 0.2)` for layered glass-morphism effect
- **Backdrop blur:** `backdrop-filter: blur(10px)` creates frosted glass effect on content
- **Hover animations:** Social buttons use `transition: all 0.3s ease` and `transform: translateY(-3px)` on hover
- **Icons:** Font Awesome 7.0.0 CDN (via `<link>`) for social media icons

### Content Structure

- **Social links:** 10 circular icon buttons linking to social media profiles (X, Instagram, TikTok, YouTube, Twitch, GitHub, Google Developer, LinkedIn, Xing, Email)
- **Biography:** Multi-paragraph text card with inline links to external institutions and projects
- **Fixed background:** `background: fixed` ensures background image stays in place on scroll

## Common Tasks & Modifications

### Adding/Updating Social Links

Social buttons are `<a>` elements with class `social-btn` inside `.social-links`. Each uses Font Awesome icons via `<i class="fab fa-{icon}">`:

```html
<a href="URL" class="social-btn" title="Label" target="_self">
  <i class="fab fa-{icon}"></i>
</a>
```

Update the `href`, `title`, and icon class to add new social profiles.

### Updating Typography

- Main heading: `h1` element styled with `color: white`, `font-size: 2.5rem`, `letter-spacing: 2px`
- Body text: Use `.text-card` for biographical content; links are styled with `color: #333; text-decoration: underline;`
- Responsive: h1 reduces to `1.8rem` on mobile via media query

### Color/Styling Adjustments

- **Dark overlay:** Change `rgba(0, 0, 0, 0.4)` value to adjust backdrop darkness
- **Blur intensity:** Modify `blur(10px)` value in `backdrop-filter` property
- **Button hover:** Change `rgba(255, 255, 255, 0.4)` to adjust button highlight color

## File Editing Notes

- **Single file responsibility:** All changes go into `index.html` (no separate files)
- **Indentation:** Uses 2-space indentation for HTML and CSS
- **External assets:** Background image at `./images/alexpaar.jpg` and Font Awesome CDN are production dependencies
- **No build process:** Changes to `index.html` are immediately visible in browser

## Deployment

Commits to this repository automatically deploy to `https://alexpaar.github.io` via GitHub Pages. No additional build steps required.
