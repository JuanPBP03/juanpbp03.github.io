# Into My Mind

This is the source code for my personal website: [Into My Mind](https://juanpbp03.github.io/).  
It's built using [Jekyll](https://jekyllrb.com/) with a locally customized version of the [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) theme. The site is deployed using GitHub Actions.

The site serves as a portfolio of my engineering projects, a place to share thoughts through blog posts, and a hands-on way to practice version control, GitHub workflows, and web development.

## Features
- Custom layouts and styles with Sass overrides
- Tag and category archives using `jekyll-archives` and `jekyll-tagories`
- Portfolio project pages with galleries and metadata
- Blog posts with clean navigation and breadcrumb support
- Fully automated deployment through GitHub Actions

## Folder Structure

```
├── _posts/           # Blog entries
├── _portfolio/       # Portfolio project pages
├── _pages/           # Static pages like About, Contact
├── assets/           # Custom images, CSS, and videos
├── _sass/            # Local Sass overrides and skin selection
├── _layouts/         # Layout templates (forked from Minimal Mistakes)

```

## Local Development

To build and preview the site locally:

```bash
bundle install
bundle exec jekyll serve
```

Then open `http://localhost:4000` in your browser.

## Deployment

This site is automatically built and deployed to GitHub Pages using GitHub Actions whenever changes are pushed to the `main` branch.
