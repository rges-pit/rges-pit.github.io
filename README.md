![Website status](https://img.shields.io/website-up-down/https/rges-pit.org.svg)    [![Open PRs](https://img.shields.io/github/issues-pr/rges-pit/rges-pit.github.io?label=open%20PRs)](https://github.com/rges-pit/rges-pit.github.io/pulls)   [![Open Issues](https://img.shields.io/github/issues/rges-pit/rges-pit.github.io?label=open%20issues)](https://github.com/rges-pit/rges-pit.github.io/issues)

<p align="center">
  <a href="https://rges-pit.org">
    <img src="./docs/assets/images/rges-pit_logo.png" alt="logo" width="300"/>
  </a>
</p>

<h1 align="center">RGES PIT Public Website</h1>

*Roman Galactic Exoplanet Survey – Project Infrastructure Team (PIT) public website.*

## Table of Contents
[1. Overview](#1-overview)
[2. Tech Stack](#2-tech-stack)
[3. Repository Layout](#3-repository-layout)
[4. Prerequisites](#4-prerequisites)
[5. Quick Start (Local Development)](#5-quick-start-local-development)
[6. Authoring Content](#6-authoring-content)
[7. Navigation & Menus](#7-navigation--menus)
[8. Assets (Images, Data, Video, Notebooks)](#8-assets-images-data-video-notebooks)
[9. Styling & Theme Customization](#9-styling--theme-customization)
[10. Deployment](#10-deployment)
[11. Contribution Workflow](#11-contribution-workflow)
[12. Quality & Style Guidelines](#12-quality--style-guidelines)
[13. Upgrading Dependencies](#13-upgrading-dependencies)
[14. Troubleshooting](#14-troubleshooting)
[15. FAQ](#15-faq)

## 1. Overview
This repository hosts the outreach and documentation site for the RGES PIT collaboration. It is a [GitHub Pages] site built with [Jekyll] using the remote theme **Minimal Mistakes**. All source content lives under `docs/` so GitHub Pages can publish directly from `main` → `docs/`.

## 2. Tech Stack
- **Platform:** GitHub Pages (builds Jekyll for us)
- **Static Site Generator:** Jekyll (pinned via `github-pages` gem → Jekyll 3.10.x at time of writing)
- **Theme:** [`mmistakes/minimal-mistakes`](https://github.com/mmistakes/minimal-mistakes)
- **Ruby Dependencies:** Declared in `docs/Gemfile` (managed by Bundler)
- **Plugins (subset):** paginate, sitemap, gist, feed, jemoji, include-cache, remote-theme
- **Markdown Engine:** Kramdown (with GFM)

## 3. Repository Layout
```
README.md
/docs
  |_config.yml            # Jekyll configuration
  |Gemfile / Gemfile.lock # Ruby dependencies (pinned to GitHub Pages set)
  |_data/                 # YAML data files (e.g. navigation.yml)
  |_includes/             # Reusable partials (theme overrides/custom additions)
  |_pages/                # Stand‑alone pages (served without date prefix)
  |_posts/                # Blog/news posts (YYYY-MM-DD-title.md)
  |assets/                # Images, css, animations, notebooks, etc.
  |index.md               # Landing page (can be splash / front matter driven)
```
Additional collections can be added by configuring them in `_config.yml`.

## 4. Prerequisites
Install a recent Ruby + Bundler. Don't do this in a conda environment; it confuses the ruby compiler.

macOS (recommended with Homebrew):
```bash
brew install ruby
# Ensure your PATH includes Homebrew ruby (often /usr/local/opt or /opt/homebrew/opt depending on chipset)
export PATH="$(brew --prefix ruby)/bin:$PATH"
gem install bundler
```
Check versions:
```bash
ruby -v
bundler -v
```
(Anything Ruby 3.x is fine; GitHub Pages presently builds on a current stable Ruby.)

## 5. Quick Start (Local Development)
All commands run from repository root unless noted.
```bash
cd docs
bundle install        # Install gems (first time or after Gemfile changes)
bundle exec jekyll serve --livereload --drafts --future --source . --baseurl "" 
```
Then open: http://127.0.0.1:4000

Common flags:
- `--livereload` auto-refresh browser
- `--drafts` builds unpublished drafts (files in `_posts` without date or in `_drafts` if you create that folder)
- `--future` includes future-dated posts
- `--incremental` faster rebuilds (sometimes causes stale includes; clear with `jekyll clean`)

Clean build cache (after includes/theme changes):
```bash
bundle exec jekyll clean && bundle exec jekyll serve
```

## 6. Authoring Content
### 6.1 Pages (`docs/_pages/`)
Create a new file: `docs/_pages/my-topic.md`
```markdown
---
layout: single
title: "My Topic"
permalink: /my-topic/
# optional sidebar/nav overrides
# sidebar:
#   nav: "docs"
---
Page body in Markdown.
```
The `permalink` controls the final URL.

### 6.2 Posts (`docs/_posts/`)
Filename format: `YYYY-MM-DD-title.md`
```markdown
---
layout: single
title: "Outreach Update"
categories: [news]
tags: [outreach, events]
author_profile: false
excerpt: Short summary for cards and meta.
---
Full post content.
```
Categories influence URL structure (see `_config.yml` permalink pattern).

### 6.3 Drafts
Not yet in repo; you may create `docs/_drafts/` and add `my-post.md` without a date. Served only with `--drafts` flag.

### 6.4 Front Matter Tips
- `layout: single` is standard (theme-provided)
- `sidebar.nav` chooses a navigation set defined under `_data/navigation.yml`
- `toc: true` to enable table of contents (if wanted; ensure theme supports)
- `last_modified_at:` can be added for SEO freshness

Note: The project defaults defined in `docs/_config.yml` automatically inject `layout: single` and `sidebar.nav: "docs"` for pages in `docs/_pages/`, so explicit declarations are only needed when overriding.

### 6.5 Includes
Custom partials live in `docs/_includes/`. Use inside pages/posts:
```liquid
{% include feature_row id="outreach_features" %}
```
If you alter an include heavily and caching interferes, run `bundle exec jekyll clean`.

### 6.6 Data Files
Store structured YAML/JSON in `docs/_data/` (e.g., `navigation.yml`) and access in Liquid:
```liquid
{% for item in site.data.navigation.main %}
  {{ item.title }}
{% endfor %}
```

### 6.7 Adding Outreach Modules
For multi-part outreach chapters (existing pattern: `outreach_mini_chapter*.html|md`):
1. Name files consistently (`outreach_mini_chapter6.md`)
2. Add appropriate front matter with a unique permalink (e.g. `/outreach/mini/ch6/`)
3. Insert navigation links (see section 7) or inline previous/next links using an include or manual markdown.

## 7. Navigation & Menus
Primary navigation is defined in `docs/_data/navigation.yml`. After editing, rebuild locally to verify.
Example entry:
```yaml
main:
  - title: "About"
    url: /about/
  - title: "Outreach"
    url: /outreach/
```
Sidebars: The Minimal Mistakes theme supports nav collections. Pages set `sidebar.nav: "docs"` to use the `docs` list defined in the same YAML file.

## 8. Assets (Images, Data, Video, Notebooks)
- Place images under `docs/assets/images/` and reference with absolute path `/assets/images/<file>`.
- Animations/video: `docs/assets/animations/` or a dedicated folder; optimize (gif → mp4/webm preferred).
- Data (CSV/JSON) supporting visualizations: `docs/assets/data/`.
- Notebooks: `docs/assets/notebooks/` (rendered as downloads unless converted to markdown via nbconvert).
- Large binaries: avoid committing > 10 MB; consider external hosting or Git LFS (not currently configured).

## 9. Styling & Theme Customization
The site uses the remote Minimal Mistakes theme (see `_config.yml: remote_theme`). To override:
1. Copy the file from the theme into `docs/_includes/` or `docs/_layouts/` preserving relative path/name.
2. Edit locally; Jekyll will prefer the local copy.
3. Add custom CSS in `docs/assets/css/` and reference via front matter (`custom_css:`) or include a manifest file imported by the theme if already configured.

## 10. Deployment
GitHub Pages auto-builds from `main` → `docs/`. No manual step required once changes are merged.
Propagation can take a couple of minutes. Purge local cache if you suspect stale assets (hard reload in browser).

## 11. Contribution Workflow
1. Create a branch: `feature/outreach-ch6` (kebab-case or slashes fine)
2. Commit logically (use present tense): `Add chapter 6 outreach page`
3. Run locally: ensure `bundle exec jekyll serve` shows no build errors
4. Open Pull Request → request review
5. After approval, squash or merge; GitHub Pages redeploys automatically.

### Typical Commit Message Conventions
- Start with verb: Add / Update / Fix / Remove
- Limit subject line to ~72 chars

### Issue Tracking
(If using GitHub Issues) Tag with: `content`, `bug`, `infra`, `design`.

## 12. Quality & Style Guidelines
- **Markdown:** Use standard GitHub-flavored; one sentence per line improves diffs.
- **Links:** Use relative links within site (`/outreach/` not full domain) so they work in previews.
- **Images:** Provide alt text.
- **Accessibility:** Use headings in order (no jumping from h2 → h4), meaningful link text.
- **Code Snippets:** Use fenced code blocks with language.
- **Front Matter Consistency:** Keep ordering: layout, title, permalink, categories, tags, (then custom fields).

## 13. Upgrading Dependencies
GitHub Pages constrains versions. To check for updates:
```bash
cd docs
bundle update
```
But do NOT remove the `github-pages` gem unless you intend to self-build (not recommended). The remote theme fetch is automatic; theme updates propagate when GitHub Pages updates the dependency set.

If you must pin a newer plugin not in the official Pages whitelist you would need to build the site elsewhere (CI) and deploy static output—out of scope for now.

## 14. Troubleshooting
| Symptom | Fix |
|---------|-----|
| Build fails locally with missing gems | Run `bundle install` inside `docs/`. Remove `Gemfile.lock` only if corrupted then reinstall. |
| Layout changes not appearing | Run `bundle exec jekyll clean` then serve again. Hard refresh browser. |
| 404 on new page after deploy | Wait 2–3 min; verify `permalink` starts and ends with `/`; ensure file in `_pages/` and included via `include: - _pages` (already set). |
| CSS not loading locally | Ensure you did not set `baseurl` in `_config.yml` for local testing; we pass `--baseurl ""` in serve command. |
| Emoji not rendering | Ensure `:emoji:` syntax; jemoji plugin included. |
| Navigation item missing | Check YAML indentation and that list key matches what layout expects (`main`, `docs`, etc.). |

## 15. FAQ
**Q: Why is `minima` in the Gemfile if we use Minimal Mistakes?**  
Because the `github-pages` meta-gem bundles `minima` by default. The active theme is set by `remote_theme` in `_config.yml`; `minima` is unused.

**Q: Can we add custom JavaScript?**  
Yes, add a file under `docs/assets/js/` and include it via an override of `head.html` or `scripts.html` include.

**Q: How do I add Google Analytics or similar?**  
See `docs/_includes/analytics.html` (and provider-specific partials). Configure tracking IDs there or in `_config.yml` if using theme options.

**Q: Where do I change the logo?**  
Update `logo:` path in `_config.yml` and place new asset in `assets/images/`.

---

## Contact
For questions, open an issue or contact the RGES-PIT admins.
* Sean Terry<!--: sterry4261@gmail.com -->
* Greg Olmschenk<!--: greg@olmschenk.com -->

---