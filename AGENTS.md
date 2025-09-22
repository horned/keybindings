# Repository Guidelines

## Project Structure & Module Organization
The project is a single-page Neovim key binding reference served from `index.html`. The page is composed of semantic `<section>` blocks (movement, editing, visual, windows, search, misc) wrapped in DaisyUI cards and Tailwind utility classes loaded from CDN. Add new categories by duplicating an existing `section` block, updating the `id`, navbar links, and anchor badges so in-page navigation stays intact.

## Build, Test, and Development Commands
- `open index.html` (macOS) — launch the static page directly in the default browser for quick visual checks.
- `python3 -m http.server 4173` — serve the site locally and test interactions such as the theme toggle; stop with `Ctrl+C`.
- `npx serve@latest .` — optional zero-config static server that mimics production caching headers.

## Coding Style & Naming Conventions
Use two-space indentation and keep HTML attributes on the same line unless the attribute list harms readability. Group Tailwind utility classes by layout → spacing → color to mirror existing sections. Favor semantic headings (`<h1>`–`<h3>`) and DaisyUI components over bespoke classes. Inline tips or shortcuts belong in `<ul>` lists to preserve consistent spacing.

## Testing Guidelines
There is no automated test suite; rely on manual verification. After changes, reload the local server in Chrome and Firefox (or Safari) to confirm layout, theme toggle persistence, and anchor scrolling. Use browser devtools’ responsive mode to ensure cards wrap cleanly at 640px and 1024px breakpoints. Validate markup with `npx htmlhint index.html` if you install the tool locally.

## Commit & Pull Request Guidelines
Follow Conventional Commits (e.g., `feat: add visual mode cheatsheet`) to keep history scannable. Commits should isolate logical changes—content edits separate from structural refactors. Pull requests must include a concise summary, before/after screenshots or screen recordings for visual updates, and references to any discussion or issue IDs. Highlight any new utilities or CDN dependencies in the description so reviewers can verify licensing and caching considerations.

## Accessibility & Content Quality
Check color contrast when adjusting themes, ensuring DaisyUI token selections pass WCAG AA. Provide descriptive link text and avoid keyboard traps; confirm every interactive element is reachable via `Tab`. When adding shortcuts, prefer phrasing that spells out the action (`Ctrl+Shift+R — refresh buffers`) to aid new users and screen reader announcements.
