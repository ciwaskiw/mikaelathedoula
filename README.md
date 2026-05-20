# Sarah Merritt — Doula Portfolio Site

A static Jekyll site for GitHub Pages. Single-page layout with smooth scroll navigation.

## Quick Start

```bash
bundle install
bundle exec jekyll serve
# → http://localhost:4000
```

## Customization Checklist

### 1. `_config.yml`
- Update `title`, `description`, `author` fields with real info.
- Set `url` to your GitHub Pages URL or custom domain.
- Set `baseurl` to `""` for a root domain, or `"/repo-name"` for project pages.

### 2. Your Information
- **`_data/services.yml`** — Edit service descriptions and included items.
- **`_data/testimonials.yml`** — Add real testimonials (get client permission first).
- **`index.html`** — Personalize the About section bio text.

### 3. Photos (high priority)
Replace both placeholder divs in `index.html` with real `<img>` tags.
Place images in `assets/images/`.

```html
<!-- Hero -->
<img src="/assets/images/hero.jpg" alt="Sarah Merritt, doula, with a new family">

<!-- About -->
<img src="/assets/images/sarah-about.jpg" alt="Sarah Merritt">
```

**Photo tips:**
- Hero: candid, warm, ideally with a family or in a birth/postpartum setting (with permission). Vertical orientation works best.
- About: approachable headshot or natural candid. Not a formal studio shot.
- Optimize images before committing — aim for < 300KB each. Use [Squoosh](https://squoosh.app/).

### 4. Colors & Fonts
All design tokens are CSS variables in `assets/css/main.scss`. Swap values at the top of the file to re-theme without touching layout code.

### 5. Agency Link
Update `site.author.agency_url` in `_config.yml` to the actual booking page, not just the agency homepage if possible.

## Deployment (GitHub Pages)

1. Push repo to GitHub.
2. Go to **Settings → Pages → Source** → select `main` branch, `/ (root)`.
3. GitHub builds and deploys automatically on each push.
4. For a custom domain: add a `CNAME` file at the repo root containing your domain (e.g. `www.sarahmerritt.com`), then configure DNS per GitHub's docs.

## File Structure

```
.
├── _config.yml          ← Site settings
├── _data/
│   ├── services.yml     ← Service cards content
│   └── testimonials.yml ← Testimonial content
├── _includes/
│   ├── header.html
│   └── footer.html
├── _layouts/
│   └── default.html
├── assets/
│   ├── css/main.scss    ← All styles + design tokens
│   ├── js/main.js       ← Scroll behavior
│   └── images/          ← Add photos here
├── index.html           ← Main page content
└── Gemfile
```
