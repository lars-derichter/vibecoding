# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A [Slidev](https://sli.dev/) presentation titled "Vibecoding with Claude Code (for Business students)" — a workshop given to Business Students at Thomas More University of Applied Sciences. Deployed to GitHub Pages at https://lars-derichter.github.io/vibecoding/.

## Commands

- `npm run dev` — Start dev server with live preview (opens browser)
- `npm run build` — Build static site to `dist/`
- `npm run export` — Export slides to PDF

## Architecture

This is a standard Slidev project. Slide content lives in Markdown files:

- `slides.md` — Main slide deck (frontmatter configures theme, transitions, metadata)
- `pages/*.md` — Additional slide pages imported into the main deck
- `components/` — Custom Vue components usable directly in slides
- `snippets/` — Code snippets referenced from slides
- `public/` — Static assets (images) served at root path

## Deployment

- **GitHub Pages**: Auto-deploys on push to `main` via `.github/workflows/deploy.yml`. Build uses `--base /<repo-name>/` for correct asset paths.
- Netlify and Vercel configs also exist (`netlify.toml`, `vercel.json`) as alternatives.

## Conventions

- All section pages (`pages/*.md`) use `transition: slide-left` in their frontmatter.

## Formatting

Prettier is configured with `prettier-plugin-slidev` to parse `slides.md` and `pages/*.md` using the Slidev parser (see `.prettierrc`).
