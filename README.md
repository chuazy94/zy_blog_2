# DataManiac

A personal blog by Zhi Yuan Chua covering football analytics, data science, and the occasional drone video.

**Live site:** https://chuazy94.github.io/zy_blog_2

---

## About

DataManiac was started during the COVID-19 pandemic out of a mix of boredom and curiosity. Posts explore:

- Football analytics (xG models, tournament simulators, match predictions)
- Data science methods (Poisson modelling, GEE, Elo ratings)
- Drone videography

---

## Tech Stack

| Layer | Technology |
|---|---|
| Static site generator | [Jekyll](https://jekyllrb.com/) 4.3+ |
| Theme | [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) 4.26.2 (remote theme) |
| Hosting | GitHub Pages |
| CI/CD | GitHub Actions (auto-deploy on push to `main`) |
| Markdown processor | kramdown + Rouge syntax highlighting |

---

## Local Development

**Requirements:** Ruby 3.x, Bundler

```bash
# Install dependencies
bundle install

# Serve locally with live reload
bundle exec jekyll serve

# Visit the site
open http://localhost:4000/zy_blog_2
```

Changes to `_posts/`, `_config.yml`, and layout files are picked up automatically. A full restart is required after editing `_config.yml`.

---

## Writing a New Post

Create a file in `_posts/` following the naming convention `YYYY-MM-DD-slug.md`.

Frontmatter template:

```yaml
---
layout: single
title: "Your Post Title"
date: YYYY-MM-DD
description: "A one-sentence summary for SEO and social sharing."
tags: [football-analytics, data-science]
categories: [football]
author_profile: true
read_time: true
---
```

The `layout: single` and `author_profile: true` fields are set as defaults in `_config.yml`, so they can be omitted if you do not need to override them.

---

## Deployment

Pushing to the `main` branch triggers a GitHub Actions workflow that builds the Jekyll site and deploys it to GitHub Pages automatically. No manual steps are required.

---

## License

Blog content (posts and images) is copyright Zhi Yuan Chua. The underlying Jekyll theme ([Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes)) is MIT licensed.
