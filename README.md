# Thammarat Yawisit — Academic & Research Website

Source for <https://poundthammaratx.github.io/>, built with [Quarto](https://quarto.org) and deployed to GitHub Pages by GitHub Actions.

## Quick start

```bash
# Requires Quarto ≥ 1.8 (https://quarto.org/docs/get-started/)
quarto preview          # live preview at http://localhost:4200
quarto render           # full build into _site/
```

No R, Python or Jupyter is required: the site contains no executable code cells.

## Repository layout

| Path | Purpose |
|---|---|
| `_quarto.yml` | Site configuration: navigation, footer, theme, SEO, search, analytics (off) |
| `_variables.yml` | Single source for name, official title, affiliation, e-mail and profile URLs (`{{< var … >}}`) |
| `data/*.yml` | **Authoritative records**: publications, talks, teaching, service, appointments, education, recognition, memberships |
| `_templates/listings/*.ejs` | Presentation templates that render the YAML records (publications, timelines, talks, recognition, cards) |
| `_templates/{research,engineering,notes}/` | Copy-and-fill templates for new project pages and notes |
| `index.qmd` | Home page |
| `about/`, `research/`, `publications/`, `engineering/`, `activities/`, `recognition/`, `notes/`, `cv/` | Site sections |
| `research/<slug>/index.qmd`, `engineering/<slug>/index.qmd` | One folder per project (front matter drives the listing cards) |
| `notes/posts/<date-slug>/index.qmd` | Notes and updates (RSS at `/notes/index.xml`) |
| `styles/theme.scss`, `styles/site.css` | Design system: colour tokens, typography, components |
| `_includes/filters.html` | Small script for publication/talk filters and e-mail obfuscation |
| `assets/` | Portrait, social preview image, favicon, CV PDF |
| `.github/workflows/publish.yml` | Build on every PR; build and deploy on push to `main` |
| `docs/` | Maintenance guide and content verification checklist |

## Deployment

Pushing to `main` runs `.github/workflows/publish.yml`, which renders the site with Quarto and deploys `_site/` with the official `actions/deploy-pages` action. Pull requests are built (to catch errors) but not deployed.

One-time repository settings:

1. Repository name: `poundthammaratx.github.io` (a GitHub *user site*, served at the root URL).
2. **Settings → Pages → Build and deployment → Source: GitHub Actions.**
3. After the first successful run, open <https://poundthammaratx.github.io/> and check it.

See [`docs/MAINTENANCE.md`](docs/MAINTENANCE.md) for how to add publications, talks, projects and notes, and [`docs/CONTENT_VERIFICATION.md`](docs/CONTENT_VERIFICATION.md) for the accuracy checklist.

## Licence

Site content © Thammarat Yawisit, licensed under CC BY 4.0 unless noted. Code in this repository (templates, styles, scripts) may be reused under the MIT licence.
