# Repository Guidelines

## Project Structure & Module Organization
- Root HTML: `index.html` (production), `index_local.html` (local preview).
- Shared partials: `nav.html`, `footer.html` (and English versions under `en/`).
- Pages: Korean under `pages/NNN.html`, English under `en/pages/NNN.html`. Use `_base.html` as a reference template.
- Assets: CSS in `css/`, JS in `js/`, images in `images/`, fonts in `fonts/`, vendor theme in `bootstrap4/`, videos in `videos/`.

## Build, Test, and Development Commands
- Serve locally: `python3 -m http.server 8000` then open `http://localhost:8000/index_local.html`.
- Quick preview: open `index_local.html` directly in a browser (AJAX sections may not load).
- Deploy (manual): commit and push to `master`. Example:
  - `git add -A && git commit -m "Update page 207 content" && git push origin master`

## Coding Style & Naming Conventions
- HTML/CSS/JS: 2-space indentation, UTF-8, LF line endings.
- File naming: lowercase with hyphens, e.g., `images/banner-4.png`. For numbered pages, follow `pages/###.html` and mirror in `en/pages/###.html`.
- Paths: production uses root-relative (`/css/...`); local uses relative (`./css/...`) as shown in `index_local.html`.
- Keep vendor files untouched (`bootstrap4/`, minified assets). Edit site-specific styles in `css/style.css` and scripts in `js/script.js` or `js/main.js`.

## Testing Guidelines
- Manual checks: load pages, verify navigation/footers, image links, and AJAX-powered sections (`/lms/*` tables on the home page).
- Responsive review: test at mobile, tablet, and desktop breakpoints.
- Accessibility basics: ensure link text is descriptive and images have `alt`.

## Commit & Pull Request Guidelines
- Commits: small, focused, imperative mood. Include path hints, e.g., `pages: update 206.html schedule`.
- PRs: include a clear summary, affected paths, before/after screenshots, and any linked issues. Note if both KR and EN pages were updated.
- Do not reformat vendor files or unrelated pages.

## Security & Configuration Tips
- Prefer `https` for external resources; avoid leaking test endpoints in production pages.
- When adding new sections to the home page, ensure both `nav.html`/`footer.html` and their `en/` counterparts remain in sync.

