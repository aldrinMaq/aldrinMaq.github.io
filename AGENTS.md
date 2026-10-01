# Agent instructions

Read this file and `.cursor/rules/` before writing code.

## Who this is for

Aldrin — software engineer. Prefer working directly in code: create, debug, iterate.

## Default stack

This repo is a **static personal portfolio** (GitHub Pages), not a Vue app scaffold:

- Single-page `index.html` (Tailwind CDN + Font Awesome)
- Resume PDF: `Maquiling-Aldrin-Resume.pdf`
- Hosted as `aldrinMaq.github.io`

Keep changes content-focused unless Aldrin asks for a redesign or a Vue rewrite.

## How to work

1. Fill **Project facts** if empty (infer from the repo).
2. When resume content changes, treat `Maquiling-Aldrin-Resume.pdf` as the source of truth for roles, bullets, skills, education, and project blurbs.
3. Implement in code. Do not stop at a plan unless asked.
4. Commits: see `.cursor/rules/git.mdc`. Never commit secrets.
5. Do not push or change git config unless asked.

## Project facts

- **Name:** Aldrin Maquiling portfolio (`aldrinMaq.github.io`)
- **What it does:** Personal portfolio site — experience, projects, skills, education, contact (source of truth: `docs/APP_CONCEPT.md`)
- **Stack:** Static HTML + Tailwind CDN + Font Awesome + Google Fonts (Plus Jakarta Sans, JetBrains Mono)
- **Package manager:** none
- **Dev:** open `index.html` locally or via a simple static server
- **Production:** GitHub Pages from this repo
- **Test command:** (none)
- **Lint / format command:** (none)
- **Important paths:** `index.html`, `Maquiling-Aldrin-Resume.pdf`, `docs/APP_CONCEPT.md`

## Do not

- Invent roles, employers, dates, or skills that are not on the resume or explicitly requested.
- Convert this site to Vue/Vite unless Aldrin asks.
- Run destructive git commands unless explicitly requested.
