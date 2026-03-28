# Nathan Bekenov — DevOps Portfolio

[![Deploy to GitHub Pages](https://github.com/nbekenov/nbekenov.github.io/actions/workflows/deploy.yml/badge.svg)](https://github.com/nbekenov/nbekenov.github.io/actions/workflows/deploy.yml)

Personal portfolio and resume site at [nbekenov.com](https://www.nbekenov.com).
Built with [Jekyll](https://jekyllrb.com/) + [Cayman theme](https://github.com/pages-themes/cayman), hosted on [GitHub Pages](https://pages.github.com/).

---

## Stack

| Layer | Technology |
|---|---|
| Static site generator | Jekyll 4.3 |
| Theme | Cayman (`pages-themes/cayman@v0.2.0`) via `jekyll-remote-theme` |
| Hosting | GitHub Pages |
| CI/CD | GitHub Actions (`actions/deploy-pages`) |
| Plugins | `jekyll-seo-tag`, `jekyll-sitemap`, `jekyll-feed` |

---

## Local Development

### Prerequisites

- Ruby 3.1+ ([install via Homebrew](https://brew.sh/): `brew install ruby`)
- Bundler 2.4+

### Setup

```bash
git clone https://github.com/nbekenov/nbekenov.github.io.git
cd nbekenov.github.io
bundle install
```

### Run locally

```bash
bundle exec jekyll serve --livereload
```

Site is available at `http://localhost:4000`.

> **Note:** On first run, `jekyll-remote-theme` fetches the Cayman theme from GitHub. Subsequent builds use the cache.

---

## Repository Structure

```
nbekenov.github.io/
├── _config.yml                  # Jekyll + Cayman configuration
├── Gemfile                      # Ruby dependencies
├── index.md                     # Landing / hero page
├── about.md                     # About + skills
├── projects.md                  # Project showcase (7 cards)
├── resume.md                    # Resume summary + LinkedIn link
├── contact.md                   # Contact information
├── _data/
│   └── skills.yml               # Skills grouped by domain
├── _includes/
│   └── head-custom.html         # Cayman CSS injection hook
├── assets/
│   ├── css/
│   │   └── custom.css           # Style overrides on top of Cayman
│   └── img/                     # Project screenshots / headshot
└── .github/
    └── workflows/
        └── deploy.yml           # GitHub Actions CI/CD
```

---

## Pages

| Page | URL | Description |
|---|---|---|
| Home | `/` | Hero intro, skills table, recent work |
| About | `/about/` | Bio, core skills by domain, certifications |
| Projects | `/projects/` | 7 project cards with Problem/Solution/Outcome/Stack |
| Resume | `/resume/` | Experience summary, PDF download link |
| Contact | `/contact/` | Email, LinkedIn, GitHub |

---

## Deployment

Pushes to `main` trigger the GitHub Actions workflow (`.github/workflows/deploy.yml`), which:

1. Builds the site with Jekyll
2. Uploads the build artifact
3. Deploys to GitHub Pages via `actions/deploy-pages`

**Requirement:** Repository Settings → Pages → Source must be set to **GitHub Actions**.

---

## Customization

| Task | How |
|---|---|
| Update content | Edit the relevant `.md` page |
| Change styles | Edit `assets/css/custom.css` |
| Add a project | Add a new `<div class="project-card">` block in `projects.md` |
| Add a blog post | Create `_posts/YYYY-MM-DD-title.md` |
| Add headshot | Place `assets/img/avatar.jpg` and reference in `about.md` |
| Add PDF resume | Place `assets/resume.pdf` and update link in `resume.md` |
| Add favicon | Place `favicon.ico` at repo root and reference in `_includes/head-custom.html` |
| Override Cayman colors | Add CSS variable overrides to `assets/css/custom.css` |
