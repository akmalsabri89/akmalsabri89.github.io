# CLAUDE.md

This file provides guidance for AI assistants working on this repository.

## Repository Overview

This is the website for **Letus Brandworks** (`akmalsabri89.github.io`), a strategic branding agency. Built as a static multi-page site — pure HTML and CSS, no build system or dependencies.

**Live site**: https://akmalsabri89.github.io
**Brand site**: https://letusbrandworks.com
**Purpose**: Full agency website — Home, Works, Services, About, Journal, Contact

---

## Project Structure

```
akmalsabri89.github.io/
├── index.html          # Home page (current live page)
├── css/
│   └── style.css       # Design system + all styles (brand tokens)
└── images/
    └── profile-akmal.png  # Placeholder image (~1.4 MB, to be replaced)
```

**Planned pages** (to be added):
- `works.html` — Portfolio grid
- `services.html` — Service offerings
- `about.html` — Studio story
- `journal.html` — Blog/insights index
- `contact.html` — Contact form

No build tools, no package managers, no frameworks. All files are served directly by GitHub Pages.

---

## Design System

### Brand Colors (CSS Variables in `css/style.css`)

| Variable      | Value     | Usage                            |
|---------------|-----------|----------------------------------|
| `--orange`    | `#F26A29` | CTAs, category tags, accent only |
| `--purple`    | `#2D2B4C` | Primary text, nav, footer bg     |
| `--charcoal`  | `#3B3E3C` | Body text                        |
| `--cream`     | `#F3E9E3` | Page background                  |
| `--warm-gray` | `#969097` | Secondary/muted text             |

Always use CSS variables for colors — never hardcode hex values in rules.

### Typography

- **Font**: Unbounded (Google Fonts) — weights 400 (regular) and 700 (bold)
- H1–H3: Bold / 700
- Body: Regular / 400
- Category labels: Orange, uppercase, small size

### Layout Principles

- Max content width ~960px, centered
- Sections separated by whitespace, not dividers
- Images contained in cards; bleed full-width in case studies only

---

## Site Architecture (Planned)

| Page | File | Purpose |
|------|------|---------|
| Home | `index.html` | Hero → Expertise → Selected Works → About dark section → Testimonials → Form → Blog preview |
| Works | `works.html` | 2-col portfolio grid with orange category tags |
| Case Study | `case-[slug].html` | Hero image → meta → challenge/solution → results metrics |
| Services | `services.html` | Service cards with checklist + FAQ accordion |
| About | `about.html` | Studio story + process steps + testimonials |
| Journal | `journal.html` | 3-col blog card grid |
| Blog Post | `post-[slug].html` | Full article layout |
| Contact | `contact.html` | 2-col: studio info + form card |

---

## Development Workflow

### Making Changes

1. Edit `index.html` or `css/style.css` directly — there is no compilation step.
2. Test locally by opening `index.html` in a browser.
3. Commit and push to deploy (GitHub Pages auto-deploys from the `main` branch).

### Branch Naming Convention

Branches follow the pattern: `<tool>/<description>-<id>`
Example: `claude/add-claude-documentation-J46Fm`

### Deployment

Pushing to `main` (or merging a PR into `main`) automatically deploys via GitHub Pages. No CI/CD pipeline configured.

---

## Code Conventions

### HTML

- HTML5 doctype with `lang="en"`
- UTF-8 charset and responsive viewport meta tags
- Semantic structure; use comments to mark logical sections
- All pages share the same nav and footer markup

### CSS

- Always use CSS variables for colors — never hardcode hex values
- Always include units on numeric values (e.g. `24px`, not `24`)
- Class-based selectors for components (`.btn`, `.card`, `.service-card`)
- Element selectors only for global resets
- Comments may appear in Indonesian (developer's language)

### Images

- Stored in `images/` directory
- Referenced via relative path: `images/filename.ext`
- Avoid committing `.DS_Store` files (macOS artifact)

---

## Known Issues / History

- **PR #1**: Fixed missing `px` unit (`font-size: 24;` → `font-size: 24px;`) in `css/style.css`
- **Commit `4d6e6a0`**: Full redesign to Letus Brandworks brand guidelines, replacing previous personal portfolio
- `.DS_Store` files were committed early in project history and later deleted

---

## Key Files at a Glance

| File | Purpose |
|------|---------|
| `index.html` | Home page — main entry point |
| `css/style.css` | All styles + brand design tokens (CSS variables) |
| `images/profile-akmal.png` | Placeholder image (~1.4 MB) |
