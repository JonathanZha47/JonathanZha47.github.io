# Yiwei Zha Personal Website

Academic Pages-style personal website for Yiwei Zha, a first-year PhD student at Vrije Universiteit Amsterdam working on trustworthy AI and safety for agentic systems.

## Local Development

Install Ruby dependencies:

```bash
bundle install
```

Build the site:

```bash
bundle exec jekyll build
```

Serve locally:

```bash
bundle exec jekyll serve --host 127.0.0.1 --port 4000
```

Then open:

```text
http://127.0.0.1:4000/
```

## Content Files

- `_pages/about.md`: homepage
- `_pages/research.md`: research themes
- `_pages/publications.html`: publication listing page
- `_publications/`: individual publication entries
- `_pages/projects.md`: project summaries
- `_pages/interests.md`: personal interests and photo gallery
- `_pages/cv.md`: CV summary
- `_pages/contact.md`: contact links
- `_data/navigation.yml`: top navigation
- `_config.yml`: site metadata and sidebar profile

## Deployment

The intended GitHub Pages repository is:

```text
JonathanZha47/JonathanZha47.github.io
```

When pushed to the `main` branch and GitHub Pages is enabled from the repository root, the site should be available at:

```text
https://JonathanZha47.github.io/
```
