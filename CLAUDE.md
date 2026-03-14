# CLAUDE.md

This file provides guidance for AI assistants working on this repository.

## Repository Overview

This is a personal GitHub Pages portfolio website for Akmal Sabri (`akmalsabri89.github.io`). It is a minimal static site with no build system or dependencies — pure HTML and CSS.

**Live site**: https://akmalsabri89.github.io
**Purpose**: Personal portfolio landing page directing visitors to [Akreates Studio](https://akreates.studio)

---

## Project Structure

```
akmalsabri89.github.io/
├── index.html          # Main (and only) page
├── css/
│   └── style.css       # Stylesheet
└── images/
    └── profile-akmal.png  # Profile photo
```

No build tools, no package managers, no frameworks. All files are served directly by GitHub Pages.

---

## Development Workflow

### Making Changes

1. Edit `index.html` or `css/style.css` directly — there is no compilation step.
2. Test locally by opening `index.html` in a browser.
3. Commit and push to deploy (GitHub Pages auto-deploys from the `main` branch).

### Branch Naming Convention

Branches follow the pattern: `<tool>/<description>-<id>`
Example: `codex/locate-and-fix-a-bug-in-codebase`, `claude/add-claude-documentation-J46Fm`

### Deployment

Pushing to `main` (or merging a PR into `main`) automatically deploys via GitHub Pages. There is no CI/CD pipeline configured.

---

## Code Conventions

### HTML (`index.html`)
- HTML5 doctype with `lang="en"`
- `UTF-8` charset and responsive viewport meta tags
- Semantic structure: single `<h1>`, `<p>`, `<img>`, `<a>`
- Comments mark logical sections (e.g., `<!-- header tag -->`, `<!-- link page 1 -->`)

### CSS (`css/style.css`)
- Class-based selectors for custom/named elements (`.akmal`, `.neko`)
- Element selectors for generic styling (`p`, `img`)
- Always include units on numeric values (e.g., `24px`, not `24`) — a missing `px` unit was the bug fixed in PR #1
- Comments may appear in Indonesian (the developer's language)
- Unused classes (`.neko`) may exist; do not remove without confirming they are not needed

### Images
- Stored in `images/` directory
- Referenced via relative path: `images/filename.png`
- Avoid committing `.DS_Store` files (macOS artifact)

---

## Known Issues / History

- **PR #1**: Fixed missing `px` unit in `font-size: 24;` → `font-size: 24px;` in `css/style.css`
- `.DS_Store` files were committed early in the project history and later deleted

---

## Key Files at a Glance

| File | Lines | Purpose |
|------|-------|---------|
| `index.html` | 29 | Portfolio landing page |
| `css/style.css` | 24 | All site styling |
| `images/profile-akmal.png` | — | Profile photo (~1.4 MB) |
