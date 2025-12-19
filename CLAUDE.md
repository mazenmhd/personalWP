# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a personal academic website built with Hugo using the HugoBlox (formerly Hugo Academic) theme. The site showcases research publications, professional experience, projects, and contact information for an academic researcher.

## Essential Commands

### Development
```bash
# Install/update Hugo modules
hugo mod get -u

# Run local development server
hugo server

# Run development server with drafts and future posts
hugo server -D -F

# Build site for production
hugo --gc --minify

# Build with specific base URL (for deployment)
hugo --gc --minify -b <URL>
```

### Content Management
```bash
# Import publications from BibTeX (requires academic CLI tool)
pip install academic==0.10.0
academic import publications.bib content/publication/ --compact
```

## Architecture

### Hugo Configuration
- **Main config**: `config/_default/hugo.yaml` - core Hugo settings, taxonomies, permalinks
- **Site params**: `config/_default/params.yaml` - theme configuration, appearance, features
- **Modules**: `config/_default/module.yaml` - Hugo module imports (Bootstrap, Netlify, Reveal plugins)
- **Languages**: `config/_default/languages.yaml` - i18n configuration
- **Menus**: `config/_default/menus.yaml` - navigation structure

### Content Structure
- **Homepage**: `content/_index.md` - uses Hugo Blox page builder with section blocks (biography, experience, projects, publications, contact)
- **Authors**: `content/authors/admin/` - author profile with photo, bio, social links
- **Publications**: `content/publication/` - research papers (auto-generated from BibTeX or manual)
- **Posts**: `content/post/` - blog posts supporting Jupyter notebooks, Markdown, technical content
- **Projects**: `content/project/` - project showcases
- **Events**: `content/event/` - talks and presentations
- **Slides**: `content/slides/` - reveal.js presentations

### Page Builder System
The homepage (`content/_index.md`) uses HugoBlox's block-based layout system:
- Each section is defined as a `block` with specific types (about.biography, experience, collection, contact, etc.)
- Content for blocks is either inline YAML data or filtered from content folders
- Blocks have configurable `design` settings (columns, view types)

### Publication Workflow
1. Add entries to `publications.bib` in root directory
2. GitHub Actions workflow automatically converts BibTeX to Markdown via the `academic` Python package
3. Creates PR with new publication pages in `content/publication/`
4. Each publication gets its own directory with `index.md` and optional `cite.bib`

### Deployment
- **Primary**: GitHub Pages via `.github/workflows/publish.yaml` (Hugo 0.124.1)
- **Alternative**: Netlify via `netlify.toml` (Hugo 0.123.3)
- Both use `hugo --gc --minify` with environment-specific flags

## Key Files and Directories

- `go.mod` / `go.sum` - Hugo module dependencies
- `assets/media/` - images, icons, gallery photos
- `resources/_gen/` - Hugo generated resources (cached images, etc.)
- `public/` - build output directory (gitignored in production)
- `static/uploads/` - static files like resume PDFs

## Theme Customization

The site uses HugoBlox v5 modules:
- `blox-bootstrap/v5` - core theme
- `blox-plugin-netlify` - Netlify integration
- `blox-plugin-reveal` - presentation slides support

Theme settings in `config/_default/params.yaml`:
- Appearance themes: `minimal` (day/night)
- Font size: `L`
- Syntax highlighting: github-light / dracula
- Search provider: wowchemy
- Map provider: mapnik

## Content Guidelines

### Author Profile
Edit `content/authors/admin/_index.md` to update:
- Personal info (name, role, organizations)
- Biography and interests
- Education and social links
- Profile photo at `content/authors/admin/avatar.jpg`

### Homepage Sections
Modify `content/_index.md` to:
- Add/remove section blocks
- Update experience timeline items
- Configure publication filters
- Customize contact information and coordinates

### Publications
Either manually create in `content/publication/` or use BibTeX import workflow. Each publication needs:
- `index.md` with front matter (title, authors, date, publication type, abstract)
- Optional: `cite.bib`, `featured.jpg`, presentation files

## Site Configuration Notes

- Base URL: `https://mazenm.com/`
- Site title: "Mazen Mohamad"
- Hugo version: 0.124.1 (GitHub Pages) / 0.123.3 (Netlify)
- Timeout: 600000ms (10 minutes) for long builds
- Ignored files: `.ipynb`, `.Rmd`, `.Rmarkdown`, `_cache`
