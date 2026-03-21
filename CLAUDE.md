# CLAUDE.md

## Project Overview

This is a **static HTML CV/resume website** for Hakim MOUCHQUELITA, a Technical Consultant specializing in Microsoft Dynamics 365 and Power Platform. The entire project is a single-page HTML file with embedded CSS — no JavaScript, no frameworks, no build tools.

## Repository Structure

```
CV-Expert-D365-Power-Platform/
├── CLAUDE.md       # This file — guidance for AI assistants
├── index.html      # The complete CV (HTML + embedded CSS, ~715 lines)
└── style.jpeg      # Profile photo asset
```

## Tech Stack

- **HTML5** — Semantic markup, single-file architecture
- **CSS3** — Embedded in `<style>` tag within `index.html`
  - CSS custom properties (variables) for theming
  - CSS Grid for two-column page layout
  - `@media print` rules for A4 PDF export
- **Google Fonts** — Montserrat and Open Sans (loaded via CDN)
- **SVG icons** — Inline data URIs for scalable icons
- **No JavaScript** — Purely static content

## Key Design Decisions

- **Single-file architecture**: All styles are embedded in `index.html`. There are no external CSS files.
- **Print-first design**: The page is sized to A4 (210mm × 297mm) and optimized for PDF export via browser print.
- **Two-column layout**: Left column holds professional experience (with timeline); right column holds certifications, skills, education, and languages.
- **CSS variables for theming**: Colors are defined in `:root` — modify these to change the palette:
  - `--primary-dark: #1e3a5f`
  - `--primary: #2c5282`
  - `--accent: #00b4d8`
- **Content language**: French

## Development Workflow

There is **no build process**. To work on this project:

1. Edit `index.html` directly
2. Open it in a browser to preview
3. Use browser print (Ctrl+P) to verify PDF output

### No tooling exists for:
- Package management (no `package.json`)
- Linting or formatting
- Testing
- CI/CD pipelines
- Git hooks

## Conventions

- Keep all styles embedded in the `<style>` tag within `index.html`
- Use CSS custom properties for colors and theming
- Use semantic HTML elements (`<header>`, `<section>`, etc.)
- Maintain print compatibility — test any layout changes with `@media print`
- Profile image is hosted externally and referenced via URL in the `<img>` tag
- SVG icons are embedded as base64 data URIs in CSS `background-image` or inline

## Git

- **Default branch**: `main` (remote) / `master` (local)
- **Commit style**: Short imperative messages (e.g., "Update image source to use a URL")
