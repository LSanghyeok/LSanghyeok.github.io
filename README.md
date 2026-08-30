# Sanghyeok Lee - Personal Homepage

Static academic homepage for `sanghyeoklee.com`, hosted with GitHub Pages.

## Structure

```text
index.html          About, research interests, and news
cv.html             Web CV and academic service
publications.html   Working papers and publications
css/styles.css      Shared responsive styles
assets/icons/       Interface icons
assets/images/      Portrait and news images
CNAME               GitHub Pages custom domain
```

The site intentionally uses plain HTML and CSS. There is no build step or runtime dependency.

## Local Preview

The pages can be opened directly, or served locally when testing links and browser behavior:

```powershell
python -m http.server 4173
```

Then open `http://127.0.0.1:4173/index.html`.

## Content Updates

### Publications

1. Add new items to `publications.html` in reverse chronological order.
2. Use `C`, `J`, `P`, or `U` for the publication type.
3. Keep action links in this order: `Paper` or `arXiv`, `Code`, `Project`, `BibTeX`.
4. Add only links that are publicly available and verified.
5. Update related acceptance news in `index.html` when appropriate.

### CV

Keep entries in reverse chronological order. Reviewer venues are separated into conferences and journals, and venue abbreviations should remain consistent.

### Shared Styles

All pages load `css/styles.css` with the same cache version. Increment the version in every HTML file whenever shared CSS changes.

## Pre-Publish Checklist

- Open About, CV, and Publications at desktop and mobile widths.
- Check that navigation, CV download, publication, profile, and email links work.
- Confirm that images have useful alternative text and no page scrolls horizontally.
- Run `git diff --check` before committing.
- After deployment, verify both `https://sanghyeoklee.com` and `https://www.sanghyeoklee.com`.

## Deployment

GitHub Pages publishes the `main` branch from the repository root. Pushing a commit to `main` triggers deployment. DNS is managed separately through Gabia; do not remove `CNAME` unless the custom domain is intentionally being disconnected.
