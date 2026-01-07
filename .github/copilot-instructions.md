## Purpose

Short, actionable guidance for AI coding agents working on this repository: a small static portfolio site built with vanilla HTML, CSS and JS. Focus on discoverable patterns, where to make edits, and how the site is deployed.

## Project snapshot

- Single-page static site. Main entry: `index.html` (lang="es").
- Static assets under `assets/` with `css/` and `js/` subfolders. Key files: `assets/css/index.css`, `assets/js/main.js`.
- Documentation and metadata in `docs/` (`project-brief.md`, `project.yaml`).
- README points to GitHub Pages deployment: https://aanaanimo.github.io/PortfolioAnaGarcia/

## How to run locally

- No build system or package.json—this is a plain static site. To preview, serve the directory over HTTP (some clients treat local file paths differently):
  - Use a simple server (recommended) or open `index.html` directly in a browser.

## Key patterns & conventions (concrete)

- Accessibility: there is a visible skip link (`<a href="#main" class="skip-link">`). Images include `alt` attributes and `loading="lazy"`.
- Typography: Google Font loaded in `index.html`; selective application is done via inline <style> in the head (e.g., `.hero-title` uses 'Monsieur La Doulaise'). Prefer editing `assets/css/index.css` for global rules, not the inline block if you need site-wide changes.
- Animation & reveal: the code uses `class="animate-on-scroll"` and `data-reveal-stagger` on containers. When adding new elements intended to animate, include those attributes/classes and update `assets/js/main.js` if timing/observer logic needs adjusting.
- Project cards / details: projects are markup-heavy within `index.html` (IDs like `#project-ecommerce`). To add a new project, replicate the article `.project-card` and corresponding `section` `.project-detail` pattern.
- Color variables: CSS uses custom properties such as `--color-accent`. Search `assets/css/*.css` to find definitions and use variables instead of hard-coded colors.

## Integration & external resources

- Images are currently placeholder images from `https://picsum.photos/`; replace with local or CDN assets in `assets/` when ready.
- Any external JS libraries (none currently tracked) should be added in `assets/js/` and referenced from `index.html`.

## Editing guidance (examples)

- To change hero subtitle font to use system fonts only: edit the `.hero-subtitle` rule in the inline <style> (or better: move the rule into `assets/css/index.css` and remove the inline override).
- To add a new navigation link: update the `<ul class="nav-links">` block in `index.html` and ensure the target section ID exists.

## Deployment notes

- Repository is intended for GitHub Pages. The README contains the published URL. There is no CI configured—push to the repo and enable GitHub Pages on the `main` branch (if not already enabled).

## What not to change without checking

- Avoid removing the `skip-link`, `aria-*` attributes or `alt` text—these are deliberate accessibility choices.
- Do not rename asset paths without updating references in `index.html` (images, CSS, JS) since this project has no bundler.

## Where to look for further context

- `index.html` — primary source of structure and content. Most changes to content are made here.
- `assets/css/index.css` (and other files in `assets/css/`) — styling and variables.
- `assets/js/main.js` — site behavior, scroll reveal and interactive bits.
- `docs/project-brief.md` and `docs/project.yaml` — project intent and metadata.

If anything here is unclear or you want the file to include additional examples (e.g., exact selectors, small code snippets, or local server commands for Windows PowerShell), tell me what to add and I will iterate.
