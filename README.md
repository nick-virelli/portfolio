# Nick Virelli — Portfolio Site

A single-page personal portfolio built with plain HTML, CSS, and JavaScript. No frameworks, no build step — opens directly in a browser and deploys to GitHub Pages by dragging the folder in.

---

## Purpose

Built in two contexts simultaneously:

1. **Live workshop demo** for IU's Technology Management Club professional development session on AI-assisted coding and GitHub Pages deployment. The goal was to show that a complete, deployable project can be built in under an hour using Claude as the primary coding tool.

2. **Real portfolio artifact** for ERP consulting and enterprise technology job applications ahead of May 2026 graduation.

---

## How It Was Built

Entirely AI-assisted using **Claude Code** (claude.ai). The workflow:

1. Attached resume and LinkedIn profile PDF as source material
2. Answered a series of clarifying questions (style, color scheme, which experiences to include, contact preferences, tagline)
3. Claude generated all three files in one pass
4. Images were dropped into `images/` and filenames were updated

No manual CSS or HTML was written. The full session — from first prompt to final image wiring — took under an hour.

---

## Tech Stack

| Layer | Choice | Why |
|-------|--------|-----|
| Markup | HTML5 | No framework needed for a static portfolio |
| Styling | CSS (custom properties) | Native CSS variables handle light/dark theming cleanly |
| Behavior | Vanilla JS | Dark mode toggle + scroll-based nav highlighting — no library needed |
| Fonts | Google Fonts (Inter) | Single `<link>` tag, no build step |
| Hosting | GitHub Pages | Free, instant, no server required |

---

## File Structure

```
portfolio/
├── index.html           # Full single-page site
├── style.css            # All styles — light/dark theme, responsive layout
├── script.js            # Dark mode toggle + active nav highlighting
├── images/
│   ├── Screenshot 2024-07-18 202103.png   # Headshot
│   ├── task_home.jpg                      # TaskNoter input screen
│   └── task_result.jpg                    # TaskNoter parsed output screen
└── README.md
```

---

## Page Sections

| Section | Notes |
|---------|-------|
| Hero | Name, tagline, LinkedIn CTA, headshot |
| About | Bio written for ERP consulting audience |
| Skills & Certifications | Chip-style tags for technical skills and four certifications |
| Technical Experience | Full cards: US Foods, Kelley TA, TMC Club, Mad Cakes |
| Projects | TaskNoter — both home and result screenshots shown stacked |
| Other Experience | Compact timeline: Grubhub, Jersey Mike's, USSF Referee |
| Footer | LinkedIn link only (no email exposed publicly) |

---

## Design Decisions

- **IU color scheme by default** — Cream (`#F2EFDE`) background, Crimson (`#990000`) accents
- **Dark mode toggle** — switches to near-black (`#1a1a1a`) with crimson accents; preference saved to `localStorage`
- **Two-tier experience layout** — Technical Experience in prominent cards, Other Experience in a compact timeline so nothing is omitted but priority is clear visually
- **No contact form** — LinkedIn is the only contact surface to avoid exposing email publicly
- **Both TaskNoter screenshots** — input screen and parsed output stacked in the project card to show the before/after without needing a live demo link

---

## Live URL

**https://nick-virelli.github.io/portfolio/**

GitHub repo: `nick-virelli/portfolio`

---

## Deploying to GitHub Pages

1. Create a new repository at github.com (can be named `portfolio` or `nickvirelli.github.io`)
2. Upload the contents of this folder (or drag in via the GitHub UI)
3. Go to **Settings → Pages → Source** and select the `main` branch, `/ (root)`
4. GitHub gives you a live URL in ~60 seconds

---

## Swapping Content

- **Headshot** — replace `images/Screenshot 2024-07-18 202103.png` with any image and update the `src` in the `<img>` tag in the hero section of `index.html`
- **Project screenshots** — replace `task_home.jpg` / `task_result.jpg` and update `src` attributes in the Projects section
- **Text content** — all copy lives directly in `index.html`; search for the section you want to edit
- **Colors** — all colors are CSS variables at the top of `style.css` under `:root` and `[data-theme="dark"]`
