# CLAUDE.md — Project Context for AI Assistants

## What is this

Personal website for Eugene Koran — an AI/ML Engineer. Built with the Dasein Astro template, deploying to Cloudflare Pages at `eugenekoran.dev`.

## Commands

```bash
bun install        # install dependencies
bun run dev        # local dev server at localhost:4321
bun run build      # production build → dist/
bun run preview    # preview production build locally
```

## Architecture

- **Framework:** Astro 5 (static site generator) with MDX, Tailwind CSS v4, Pagefind search
- **Package manager:** Bun (not npm/yarn)
- **Template origin:** [roicort/dasein](https://github.com/roicort/dasein) — heavily customized

## Content System (Astro Content Collections)

All content schemas are defined in `src/content.config.ts`. There are 4 collections:

### Projects (`src/content/projects/*.md`)
Markdown files with frontmatter:
```yaml
title: string
description: string
pubDate: date
tags: string[]
category: "research" | "personal"  # default: "personal"
heroImage: image (optional)
```
- `category: research` projects appear in a separate "Research" group on `/projects/` with visual distinction (SPAR badge, subtle ring border)
- `category: personal` (default) projects appear under "Personal Projects"

### Blog (`src/content/blog/*.md`)
Same schema as projects minus `category`. **Currently empty** — blog page exists structurally but has no posts. The "blog collection does not exist" warnings during build are expected and harmless.

### CV (`src/content/cv.yml`)
YAML array of sections rendered on the homepage via `SectionList` component. Each entry has `id`, `heading`, and `items[]` with `title`, `description`, `datetime`. Currently has "Research" and "Industry Experience" sections.

### Site Config (`src/site-config.yml`)
Author info (name, role, bio, location) and social links. Consumed by `src/utils/consts.ts` → `getSite()`.

## Key Files

| File | Purpose |
|------|---------|
| `src/site-config.yml` | Name, role, bio, location, social links |
| `src/content/cv.yml` | Homepage timeline sections (Research, Industry Experience) |
| `src/content.config.ts` | Content collection schemas (blog, projects, cv, site) |
| `astro.config.mjs` | Site URL (`https://eugenekoran.dev`), integrations |
| `src/pages/index.astro` | Homepage: Hero → Projects → CV sections → Blog |
| `src/pages/about.astro` | About page — 6 sections using 3-column grid layout |
| `src/pages/projects/index.astro` | Projects listing with Research/Personal separation |
| `src/components/SectionList.astro` | Reusable 3-col grid section (heading left, content right) |
| `src/components/Hero.astro` | Large-text hero with role, bio, location, CTA buttons |
| `src/components/Footer.astro` | Copyright, San Francisco clock, theme credit |
| `src/components/Header.astro` | Nav: Home, Blog, Projects, About, Search, GitHub, Theme toggle |
| `src/styles/global.css` | Theme variables (--color-ink, --color-paper, etc.), dark mode |

## Design Patterns

- **Layout:** 3-column grid with sticky left heading, content spanning right 2 cols, `border-b border-base-200` between sections. This is the dominant pattern across homepage, about page, and section lists.
- **Typography classes:** `text-base-900` for headings, `text-base-600` for body, `text-muted` for secondary. Headings use `text-sm font-bold uppercase`.
- **Dark mode:** Controlled via `data-theme="dark"` on `:root`. Theme variables swap in `src/styles/global.css`.
- **Tags system:** `/tags/[tag].astro` generates pages from tags in BOTH blog and projects collections. `/tags/index.astro` aggregates counts from both. If you add tags to new content, tag pages are auto-generated at build time.

## Deployment

- **Hosting:** Cloudflare Pages (git-push deploys from `main` branch)
- **Domain:** `eugenekoran.dev` (purchased via Cloudflare Registrar)
- **Build settings:** Framework preset Astro, build command `bun run build`, output dir `dist`

## Development

- **Concise commit messages:** Keep commit messages concise and focused

## Important Context

- The role title ("Researcher · Engineer · Builder") is intentionally generic
- Blog is ready but intentionally empty. Build warnings about empty blog collection are expected.
- Template originally had Spanish locale strings (`es-MX` dates, Spanish tag page labels) — these have been translated to English but watch for any remaining ones.
