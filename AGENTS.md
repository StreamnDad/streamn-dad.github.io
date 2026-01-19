# Repository Guidelines

## Project Structure & Module Organization
- `index.html` is the entire site (markup + CSS + content). Keep related styles near the section they style.
- `CNAME` configures the GitHub Pages custom domain.
- Image assets live in `assets/images` (e.g., `assets/images/streamn-dad-logo-1.jpg`). Add new assets there and keep filenames lowercase with hyphens.

## Build, Test, and Development Commands
This is a static site with no build pipeline.
- Local preview (simple static server):
  - `python3 -m http.server` then open `http://localhost:8000`.
- Direct editing: open `index.html` in a browser and refresh after changes.
- When adding or removing pages, update `sitemap.xml` and keep `robots.txt` pointing to it. Refresh `<lastmod>` dates as needed.

## Coding Style & Naming Conventions
- Indentation: 2 spaces in HTML and CSS, no tabs.
- HTML: semantic tags (`header`, `section`, `article`, `footer`) and accessible attributes (`alt`, `aria-*`) where relevant.
- CSS: class names in kebab-case (e.g., `.cta-banner`), custom properties in `:root` using `--kebab-case` names.
- Keep typography choices consistent with the current Google Fonts stack (Oswald + Shippori Mincho) unless intentionally updating the visual system.

## Testing Guidelines
- No automated tests are configured. Validate changes by loading the page in a browser and checking desktop + mobile layouts.
- When editing the hero, stats, or panels, verify that the layout still works at ~720px width (see the existing media query).

## Commit & Pull Request Guidelines
- There is no established commit message convention yet. Use clear, imperative messages such as `Update hero copy` or `Adjust CTA styling`.
- PRs should describe what changed, why it changed, and include screenshots when layout or visual styles are modified.

## Security & Configuration Tips
- Do not commit secrets; this repo is public by default (GitHub Pages). The only configuration file expected is `CNAME`.
- If you change image filenames, update the references in `index.html` to avoid broken assets.
