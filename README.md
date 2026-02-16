# Hugo Lemonnier - Portfolio (Hugo + PaperMod)

This repository contains the source of my personal portfolio built with Hugo and the PaperMod theme.

Live site: `https://hlemonnier.github.io`

## Requirements (for local development)
- Hugo Extended (latest)
- Optional: Node.js/npm if you want custom scripts (not required)

Verify your setup:

```bash
hugo version
```

## Local development
Initialize submodules:

```bash
git submodule update --init --recursive
```

Start a local dev server:

```bash
hugo server -D --renderToMemory
# open http://localhost:1313
```

Build the site:

```bash
hugo --cleanDestinationDir --gc --minify -d docs
# Output goes to docs/
```

## Deployment (GitHub Pages via Actions)
This repo uses GitHub Actions to build and publish the site to GitHub Pages on every push to `main` (and `hugo-rebuild`).

- Workflow: `.github/workflows/deploy.yml`
- Pages setting: Repository -> Settings -> Pages -> Build and deployment -> GitHub Actions

To trigger a deployment:

```bash
git add -A && git commit -m "content: update" && git push
```

Then wait for the "Deploy Hugo to GitHub Pages" job to finish and open `https://hlemonnier.github.io`.

## Internationalization (i18n)
- Default language: English
- `defaultContentLanguageInSubdir: true` -> English lives under `/en`, French under `/fr`.
- Menus and profile buttons are defined per language in `config.yaml` under `languages.en` and `languages.fr`.

Content structure:
- English: `content/en/...`
- French: `content/fr/...`

## Customize
Edit `config.yaml`:
- `baseURL`: `https://hlemonnier.github.io/`
- `title`, `params.profileMode` (title, subtitle, buttons)
- Menu entries per language under `languages.*.menu.main`

Static assets:
- Put images and documents (e.g., `cv.pdf`) in `static/` -> available at `/cv.pdf`, `/Linkedin PP.jpg`, etc.

## Theme (PaperMod)
The theme is tracked as a submodule in `themes/PaperMod`.

## Project layout
- `config.yaml` - Hugo configuration (including i18n, menus, publishDir)
- `content/` - pages and sections (`en/`, `fr/`)
- `static/` - static files copied as-is (images, PDFs)
- `themes/` - PaperMod (git submodule)
- `docs/` - build output used by GitHub Pages

## License
Content © Hugo Lemonnier. The code and configuration in this repository are provided as-is for personal site usage.
