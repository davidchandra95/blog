# ~/blog

Personal blog built with [Hugo](https://gohugo.io) and a custom **neon** terminal-aesthetic theme.

## Quick start

```bash
# Create a new post
hugo new posts/my-post.md

# Preview locally with drafts
hugo server -D

# Build for production
hugo --minify
```

## Theme

The **neon** theme (`themes/neon/`) is a custom developer-aesthetic theme built on:

- **Dark background** (`#0d1117`)
- **Monospace fonts** (JetBrains Mono / Fira Code)
- **Blue-green neon** accents (`#00e5ff`) for links and interactive elements
- **Pink neon** accents (`#ff2d95`) for highlights and hover states

### Customize

Edit `hugo.yaml` to change accent colors, fonts, and site metadata:

```yaml
params:
  accent: "#00e5ff"      # cyan neon
  accentAlt: "#ff2d95"   # pink neon
  bg: "#0d1117"
  fg: "#c9d1d9"
```

## Deployment

Push to `main` — GitHub Actions builds and deploys to `https://davidchandra95.github.io/blog/` automatically.

The workflow is in `.github/workflows/hugo-deploy.yml`. It uses:

- `peaceiris/actions-hugo` to install Hugo
- `actions/deploy-pages` for GitHub Pages deployment

### Setup

1. Create the repo `davidchandra95.github.io` (or configure Pages for this repo)
2. In repo Settings → Pages → Source: **GitHub Actions**
3. Push to `main`

## Project structure

```
.
├── archetypes/          # Post templates
│   └── posts.md         #   Frontmatter for new posts
├── content/
│   └── posts/           # Markdown blog posts
├── themes/neon/         # Custom theme
│   ├── assets/css/      #   CSS source (piped through Hugo)
│   ├── layouts/         #   HTML templates
│   └── static/          #   Static assets
├── hugo.yaml            # Hugo configuration
└── .github/workflows/   # CI/CD
    └── hugo-deploy.yml
```

## Features

- [x] Terminal / neon developer aesthetic
- [x] Tags and categories with taxonomy pages
- [x] Archive grouped by year
- [x] Code syntax highlighting (Chroma)
- [x] Mobile responsive
- [x] Sitemap and robots.txt
- [x] GitHub Actions deploy
- [x] Draft support (`draft: true`)
- [x] Reading time and word count
