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
3. Link each title to the official paper or arXiv page.
4. Show a compact `Code` action beneath the paper only when a public repository is available and verified.
5. Update related acceptance news in `index.html` when appropriate.

The homepage's selected publications section is reserved for papers where Sanghyeok Lee is the first author or is explicitly marked as an equal-contribution co-first author. Keep the same reverse chronological order and role labels when updating it.

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
