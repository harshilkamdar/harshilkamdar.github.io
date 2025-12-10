# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a personal website/portfolio built with Jekyll and hosted on GitHub Pages. The site uses Jekyll's static site generation with GitHub Pages gem for hosting compatibility.

## Development Commands

### Local Development
```bash
# Install dependencies
bundle install

# Serve the site locally with auto-reload
bundle exec jekyll serve

# Serve with drafts included
bundle exec jekyll serve --drafts

# Build the site (output to _site/)
bundle exec jekyll build

# Clean generated files
bundle exec jekyll clean
```

### GitHub Pages Deployment
- The site automatically deploys when changes are pushed to the `master` branch
- GitHub Pages uses the `github-pages` gem which includes Jekyll and required plugins
- No manual deployment commands needed

## Architecture

### Site Structure
- **_layouts/**: HTML templates for pages and posts
  - `default.html`: Main page template with header, content area, and footer
  - `post.html`: Template for blog posts
- **_includes/**: Reusable HTML components
  - `head.html`: HTML head section with meta tags and CSS
  - `header.html`: Navigation and site header
  - `footer.html`: Site footer
  - `scripts.html`: JavaScript includes
  - `analytics.html`: Analytics tracking code
  - `disqus.html`: Comments integration
  - `post-list.html`: Blog post listing component
- **_posts/**: Blog posts in Markdown format (YYYY-MM-DD-title.md)
- **css/**: Stylesheets and assets
- **js/**: JavaScript files
- **files/**: Static files and documents
- **cv/**: CV/resume related content
- **contact/**: Contact page content
- **notes/**: Notes section content

### Content Management
- Posts use Markdown with YAML front matter
- Pages use Jekyll's layout system with Liquid templating
- Static assets are served directly from their directories

### Configuration
- `_config.yml`: Jekyll site configuration
  - Site metadata and GitHub Pages settings
  - Markdown processor: kramdown
  - Plugins: jekyll-sitemap
- `Gemfile`: Ruby dependencies (github-pages gem)

## Key Files for Editing

### Adding Blog Posts
- Create new `.md` files in `_posts/` with format: `YYYY-MM-DD-title.md`
- Include YAML front matter with layout, title, and date
- Use Markdown for content

### Modifying Layout/Design
- Edit HTML templates in `_layouts/` and `_includes/`
- Modify CSS in `css/` directory
- Update JavaScript in `js/` directory

### Site Configuration
- Modify `_config.yml` for site-wide settings
- Update `index.html` for homepage content