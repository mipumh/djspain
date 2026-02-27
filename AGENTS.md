# Repository Guidelines

## Project Structure & Module Organization
This repository is a Jekyll-powered static site for `periodistasdedatos.com`.
- Content pages: root-level Markdown files such as `acerca.md`, `analisis.md`, and `contacto.md`.
- Collection content: `_entrevistas/` (one Markdown file per interview/profile).
- Shared templates: `_layouts/` and `_includes/`.
- Data files: `_data/` (CSV used by templates/pages).
- Styles: `css/main.scss` with partials in `_sass/`.
- Static assets: `img/`, `public/`, favicon/manifest files at repo root.
- Generated output: `_site/` (build artifact; do not edit by hand).

## Build, Test, and Development Commands
Dependency manifests are not committed (`Gemfile`, `package.json`, and `gulpfile.js` are absent), so use direct Jekyll commands.
- `jekyll serve --livereload`: run locally and preview changes.
- `jekyll build`: generate static output into `_site/`.
- `jekyll clean`: remove generated files before a fresh build.

Run commands from the repository root (`/Users/mcarvajal/dev/peridatos`).

## Coding Style & Naming Conventions
- Use 2-space indentation in YAML, HTML/Liquid, and SCSS.
- Keep front matter minimal and valid YAML in every content file.
- Use lowercase, hyphen-free descriptive filenames for top-level pages (existing pattern: `proyectos.md`, `transparencia.md`).
- In `_entrevistas/`, keep one profile per file and preserve the current human-readable naming pattern.
- Prefer updating `_sass/` partials and `css/main.scss` over inline styles.

## Testing Guidelines
There is no automated test suite configured in this repository.
- Before opening a PR, run `jekyll build` and fix any Liquid/YAML errors.
- Manually validate changed pages with `jekyll serve --livereload`.
- If you change data-driven templates, verify at least one affected entry from `_data/` and one from `_entrevistas/`.

## Commit & Pull Request Guidelines
Recent history uses short, lowercase commit messages (for example: `new yml`, `new jag`). Keep messages concise and specific.
- Recommended format: `<area>: <change>` (example: `entrevistas: add Adrian Blanco profile`).
- PRs should include: purpose, files/sections changed, and screenshots for visible UI/content updates.
- Link related issue/task when available, and note any follow-up content updates.
